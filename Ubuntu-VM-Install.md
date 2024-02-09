# Install VM with Ubuntu. 

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


## Way 2. If you need X86 version. (Takes a lot of time...😭😭😭)

**Step 1**

[Install iso file with Ubuntu](https://ubuntu.com/download/desktop)

**Step 2**

[Install Qemu](https://github.com/NorthCapDiamond/Mac-users-life/blob/main/Install-Qemu.md)

**Step 3**

Create directory for comfortable work with this:

```
mkdir QEMU
cd QEMU
mkdir qemu-emulate_x86_ubuntu
cd qemu-emulate_x86_ubuntu
mkdir 22.04.3-desktop
cd 22.04.3-desktop
```

put there your ISO file!!!

**Step 4**

Configure qemu:

```
qemu-img create -f qcow2 ubuntu.qcow2 30G
```

Start:

```
qemu-system-x86_64 -hda ubuntu.qcow2 -boot d -cdrom ubuntu-22.04.3-desktop-amd64.iso  -m 2G -usb -machine pc
```

Now you'll have to set up your system. Interface of Ubuntu is going to help you )))

...💀☠️ 2000 year Later ☠️💀 ...

**Step 5**

to be continued !



That's it for today)
