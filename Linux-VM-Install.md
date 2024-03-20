# Install VM with Linux. 

## Way1. Easy and fast!😘 (Arm version of Ubuntu)

**Step 1**

Install Multipass
```
brew install multipass
```

**Step 2** 

Find version of Ubuntu
``` 
multipass find
```

Prepare VM
```
multipass launch 22.04 -n myvm -c 4 -m 4G -d 50G
```

if need:
```
multipass shell myvm
```

**Step 3**
Set up your VM environment :

```
sudo apt update && sudo apt upgrade
sudo apt-get install ubuntukylin-desktop xrdp -y
```

Configure user:

```
sudo adduser diamond
sudo usermod -aG sudo diamond
```

**Check you current multipass list of instances**:

```
multipass list
```

**To start VM**:

```
multipass shell myvm
```

**IF YOU WANT TO DELETE AN INSTANCE**:
```
multipass delete keen-yak
```
```
multipass purge
```
```
multipass list
```


## Way 2. If you need X86 version. (Takes a lot of time... And probably won't work...😭😭😭)

**Step 1**

[Install iso file with Debian](https://www.debian.org)

**Step 2**

[Install Qemu](https://github.com/NorthCapDiamond/Mac-users-life/blob/main/Install-Qemu.md)

**Step 3**

Create directory for comfortable work with this:

```
mkdir QEMU
cd QEMU
mkdir qemu-emulate_x86_debian
cd qemu-emulate_x86_debian
```

put there your ISO file!!!

**Step 4**

Configure qemu:

```
qemu-img create -f qcow2 debian.qcow2 30G
```

Start:

```
qemu-system-x86_64 -hda debian.qcow2 -boot d -cdrom debian-12.4.0-amd64-netinst.iso	debian.qcow2 -m 2G -usb -machine pc
```

Now you'll have to set up your system. (Dont Install visual environment ) Interface of Debian is going to help you )))
Finally you will reboot the system. 
After that thing TURN OFF QEMU.

...💀☠️ 2000 year Later ☠️💀 ...

**Step 5**

Launch you Debian with better hardware options :

```
qemu-system-x86_64 -hda debian.qcow2 -boot d -m 2G -usb -machine q35 -cpu max -smp cores=8,threads=1,sockets=1  &
```



That's it for today)
