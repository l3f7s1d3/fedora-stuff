# fedora-stuff
* install virtualbox fedora32
* curl -sSl https://raw.githubusercontent.com/leftside97/fedora-stuff/master/fedora-virtualbox.sh | /bin/bash
* install docker
* curl -sSl https://raw.githubusercontent.com/leftside97/fedora-stuff/master/fedora32-docker.sh | /bin/bash




### CoreCtrl
```
sudo nano /boot/loader/entries/xxxxxxxxxxxxx-5.11.9-200.fc33.x86_64.conf
```
```
options root=UUID=xxxx ro rootflags=subvol=root rhgb quiet amdgpu.ppfeaturemask=0xffffffff
```



### free and nonfree repository
```
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

### NTFS FIX
```
sudo ntfsfix /dev/sdX
```
```
sudo mount -t ntfs-3g /dev/sdX /...
```

### Discord
```
sudo dnf install snapd
```
```
sudo ln -s /var/lib/snapd/snap /snap
```
```
sudo snap install discord
```
```
snap run discord
```

### VBOX FEDORA33
```
dnf install rpmrebuild
```
```
cd /tmp
```
```
wget https://download.virtualbox.org/virtualbox/6.1.18/VirtualBox-6.1-6.1.18_142142_fedora32-1.x86_64.rpm
```
```
rpmrebuild --change-spec-preamble='sed -e "s/6.1.18_142142_fedora32/6.1.18_142142_fedora33/"' --change-spec-requires='sed -e "s/python(abi) = 3.8/python(abi) >= 3.8/"' --package VirtualBox-6.1-6.1.18_142142_fedora32-1.x86_64.rpm
```
```
dnf install binutils gcc make patch libgomp glibc-headers glibc-devel kernel-headers kernel-devel dkms qt5-qtx11extras libxkbcommon
```
```
dnf install ~/rpmrebuild/RPMS/x86_64/VirtualBox-6.1-6.1.18_142142_fedora33-1.x86_64.rpm
```

### VBOX 
```
sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
```
```
sudo dnf install VirtualBox
```






