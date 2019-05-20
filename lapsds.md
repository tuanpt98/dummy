# How to join a computer in LAB SDS Team.

The first, we need to check whether the CPU supports Hypervisor or not.

```sh
$ sudo grep -E '(vmx|svm)' /proc/cpuinfo
```

## Step 1: Install packets of KVM 
```sh
$ sudo yum install qemu-kvm qemu-img virt-manager libvirt libvirt-python libvirt-client virt-install virt-viewer bridge-utils
```

Start and enable service KVM.
```sh
$ sudo systemctl start libvirtd
$ sudo systemctl enable libvirtd
```

Check KVM modules.
```sh
$ sudo lsmod | grep kvm
kvm_intel             162153  0
kvm                   525409  1 kvm_intel
```

Run the command below to allow starting GUI.
```sh
$ sudo yum install "@X Window System" xorg-x11-xauth xorg-x11-fonts-* xorg-x11-utils -y
```

## Step 2 : Configure Network. 
```sh
$ sudo cd /etc/sysconfig/network-scripts/
$ sudo cp ifcfg-eno49 ifcfg-br0
```
Replace ifcfg-eno49 to your ethernet interface.

### Configure Bridge Interface
```sh
$ sudo vim ifcfg-br0
```
Add content below inside to the ifcfg-br0 file.
```sh
TYPE=Bridge
BOOTPROTO=static
DEVICE=br0
ONBOOT=yes
IPADDR=172.27.100.157
NETMASK=255.255.255.0
GATEWAY=172.27.100.1
DNS1=8.8.8.8
DNS2=8.8.4.4
```
Replace IPADDR, NETMASK, GATEWAY with your information.

### Configure Ethernet Interface
Configure ifcfg-eno49 file. 
```sh
$ sudo vim ifcfg-eno49
```
Add content to the file.
```sh
TYPE="Ethernet"
BOOTPROTO="dhcp"
DEVICE="ifcfg-eno49"
ONBOOT="yes"
BRIDGE="br0"
```

Restart network service.
```sh
$ sudo systemctl restart network
```

## Step 3: Configure libvirt.
Configure libvirtd.conf file.

```sh
$ vim /etc/libvirt/libvirtd.conf
```
Find and correct the following values.
```sh
listen_tls = 0
listen_tcp = 1
auth_tcp="none"
tcp_port = "16509"
```

Configure libvirtd file.
```sh
$ sudo vim  /etc/sysconfig/libvirtd
```

Remove the command and change the following value.
```sh
LIBVIRTD_ARGS="--listen"
```

Restart libvirtd service.
```sh
$ sudo systemctl restart libvirtd
```

## Step 4: Join computer in Lab.
Disable Firewall.
```sh
$ systemctl stop firewalld
```

Use Chrome Browser to access IP: 172.27.100.152. Then, click at Add Connection button. Fill in the appropriate information to edit text.
    * Username: root
    * Password: DevOps@Lab2019

Visit the newly installed lab in WebVirtMgr.
* Tab **Storages**: Click New Storage Button -> 
      * Name:                default. 
    -> Click Create button.

* Tab **Network**: 
    **Create Bridge network:** Click New Network Button -> 
      * Type forwarding:    BRIDGE 
      * Name:               Bridge
      * Bridge Name:        br0
    -> Click Create button.

    **Create br0 network:** Click New Network Button -> 
      * Type forwarding:    BRIDGE 
      * Name:               br0
      * Bridge Name:        br0
    -> Click Create button.
