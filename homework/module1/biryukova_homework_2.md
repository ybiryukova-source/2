#Завдання 1
1. ubuntu@ubuntu:~$ cd /
ubuntu@ubuntu:/$ pwd
/
ubuntu@ubuntu:/$ ls
bin   cdrom  etc   lib    lib64   media  opt   rofs  run   snap  sys  usr
boot  dev    home  lib32  libx32  mnt    proc  root  sbin  srv   tmp  var

2. ubuntu@ubuntu:/$ cd /etc
ubuntu@ubuntu:/etc$ pwd
/etc
ubuntu@ubuntu:/etc$ ls
acpi                           host.conf            polkit-1
adduser.conf                   hostid               ppp
alsa                           hostname             profile
alternatives                   hosts                profile.d
anacrontab                     hosts.allow          protocols
apg.conf                       hosts.deny           pulse
apm                            hp                   python3
apparmor                       ifplugd              python3.10
apparmor.d                     init                 rc0.d
apport                         init.d               rc1.d
appstream.conf                 initramfs-tools      rc2.d
apt                            inputrc              rc3.d
avahi                          insserv.conf.d       rc4.d
bash.bashrc                    ipp-usb              rc5.d
bash_completion                iproute2             rc6.d
bash_completion.d              issue                rcS.d
bindresvport.blacklist         issue.net            request-key.conf
binfmt.d                       kernel               request-key.d
bluetooth                      kernel-img.conf      resolv.conf
brlapi.key                     kerneloops.conf      rmt
brltty                         keyutils             rpc
brltty.conf                    ldap                 rsyslog.conf
ca-certificates                ld.so.cache          rsyslog.d
ca-certificates.conf           ld.so.conf           rygel.conf
ca-certificates.conf.dpkg-old  ld.so.conf.d         sane.d
casper.conf                    legal                security
chatscripts                    libao.conf           selinux
cifs-utils                     libaudit.conf        sensors3.conf
console-setup                  libblockdev          sensors.d
cracklib                       libnl-3              services
cron.d                         libpaper.d           sgml
cron.daily                     libreoffice          shadow
cron.hourly                    locale.alias         shadow-
cron.monthly                   locale.gen           shells
crontab                        localtime            skel
cron.weekly                    logcheck             snmp
cryptsetup-initramfs           login.defs           speech-dispatcher
crypttab                       logrotate.conf       ssh
cups                           logrotate.d          ssl
cupshelpers                    lsb-release          sssd
dbus-1                         lvm                  subgid
dconf                          machine-id           subuid
debconf.conf                   magic                sudo.conf
debian_version                 magic.mime           sudoers
default                        mailcap              sudoers.d
deluser.conf                   mailcap.order        sudo_logsrvd.conf
depmod.d                       manpath.config       sysctl.conf
dhcp                           mime.types           sysctl.d
dictionaries-common            mke2fs.conf          systemd
dpkg                           ModemManager         terminfo
e2scrub.conf                   modprobe.d           thermald
emacs                          modules              thunderbird
environment                    modules-load.d       timezone
environment.d                  mtab                 tmpfiles.d
ethertypes                     nanorc               ubuntu-advantage
firefox                        netconfig            ucf.conf
fonts                          netplan              udev
fprintd.conf                   network              udisks2
fstab                          networkd-dispatcher  ufw
fuse.conf                      NetworkManager       update-manager
fwupd                          networks             update-motd.d
gai.conf                       newt                 update-notifier
gdb                            nftables.conf        UPower
gdm3                           nsswitch.conf        usb_modeswitch.conf
geoclue                        openvpn              usb_modeswitch.d
ghostscript                    opt                  vim
glvnd                          os-release           vtrgb
gnome                          PackageKit           vulkan
groff                          pam.conf             wgetrc
group                          pam.d                wpa_supplicant
group-                         papersize            X11
grub.d                         passwd               xattr.conf
gshadow                        passwd-              xdg
gshadow-                       pcmcia               xml
gss                            perl                 zfs
gtk-2.0                        pki                  zsh_command_not_found
gtk-3.0                        pm
hdparm.conf                    pnm2ppa.conf

3. ubuntu@ubuntu:/etc$ cd /home
ubuntu@ubuntu:/home$ pwd
/home
ubuntu@ubuntu:/home$ ls
ubuntu

#Завдання 2
1. ubuntu@ubuntu:~$ mkdir lab2
 
2. ubuntu@ubuntu:~/lab2$ touch file.txt

3. ubuntu@ubuntu:~/lab2$ cp file.txt copy.txt

4. ubuntu@ubuntu:~/lab2$ mv copy.txt renamed.txt

5. ubuntu@ubuntu:~/lab2$ ln file.txt hardlink.txt
ubuntu@ubuntu:~/lab2$ ls -l
total 0
-rw-rw-r-- 2 ubuntu ubuntu 0 тра 22 06:01 file.txt
-rw-rw-r-- 2 ubuntu ubuntu 0 тра 22 06:01 hardlink.txt
-rw-rw-r-- 1 ubuntu ubuntu 0 тра 22 06:03 renamed.txt

6. ubuntu@ubuntu:~/lab2$ ln -s file.txt symlink.txt
ubuntu@ubuntu:~/lab2$ ls -l
total 0
-rw-rw-r-- 2 ubuntu ubuntu 0 тра 22 06:01 file.txt
-rw-rw-r-- 2 ubuntu ubuntu 0 тра 22 06:01 hardlink.txt
-rw-rw-r-- 1 ubuntu ubuntu 0 тра 22 06:03 renamed.txt
lrwxrwxrwx 1 ubuntu ubuntu 8 тра 22 11:33 symlink.txt -> file.txt

7. ubuntu@ubuntu:~/lab2$ find ~ -name file.txt
/home/ubuntu/lab2/file.txt

#Завдання 3
1. ubuntu@ubuntu:~/lab2$ ls -l file.txt
-rw-rw-r-- 2 ubuntu ubuntu 0 тра 22 06:01 file.txt

2. ubuntu@ubuntu:~/lab2$ chmod 444 file.txt
ubuntu@ubuntu:~/lab2$ ls -l file.txt
-r--r--r-- 2 ubuntu ubuntu 0 тра 22 06:01 file.txt

3. ubuntu@ubuntu:~/lab2$ chmod u+w file.txt
ubuntu@ubuntu:~/lab2$ ls -l file.txt
-rw-r--r-- 2 ubuntu ubuntu 0 тра 22 06:01 file.txt

4. ubuntu@ubuntu:~/lab2$ umask
0002

5. ubuntu@ubuntu:~/lab2$ umask 022
ubuntu@ubuntu:~/lab2$ umask
0022


#Завдання 4
1. ubuntu@ubuntu:~/lab2$ sudo adduser liza
Adding user `liza' ...
Adding new group `liza' (1000) ...
Adding new user `liza' (1000) with group `liza' ...
Creating home directory `/home/liza' ...
Copying files from `/etc/skel' ...
New password: 
Retype new password: 
Sorry, passwords do not match.
New password: 
BAD PASSWORD: The password is shorter than 8 characters
Retype new password: 
passwd: password updated successfully
Changing the user information for liza
Enter the new value, or press ENTER for the default
	Full Name []: liza212
	Room Number []: 
	Work Phone []: 
	Home Phone []: 
	Other []: 
Is the information correct? [Y/n] 

2. ubuntu@ubuntu:~/lab2$ sudo usermod -aG sudo liza

3. ubuntu@ubuntu:~/lab2$ getent passwd liza
liza:x:1000:1000:liza212,,,:/home/liza:/bin/bash
ubuntu@ubuntu:~/lab2$ groups liza
liza : liza sudo
