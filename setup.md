1) Configure ssh keys for access + new key for GitHub commits from RPi

2) OS updates and packages
```
sudo apt-get update
sudo apt-get install docker-compose
sudo apt-get install qemu-user-static
sudo apt-get install vim
sudo apt-get upgrade
```
3) Configure time
```
# Link timezone
sudo ln -sf /usr/share/zoneinfo/America/Los_Angeles /etc/localtime

# Install NTP
sudo apt-get install ntp

# Backup conf
sudo mv /etc/ntp.conf /etc/ntp.conf.orig

# Set custom ntp.conf
echo "driftfile /var/lib/ntp/ntp.drift
statistics loopstats peerstats clockstats
filegen loopstats file loopstats type day enable
filegen peerstats file peerstats type day enable
filegen clockstats file clockstats type day enable
server 0.debian.pool.ntp.org iburst
server 1.debian.pool.ntp.org iburst
server 2.debian.pool.ntp.org iburst
server 3.debian.pool.ntp.org iburst
restrict -4 default kod notrap nomodify nopeer noquery
restrict -6 default kod notrap nomodify nopeer noquery
restrict 127.0.0.1
restrict ::1" | sudo tee /etc/ntp.conf

# Start NTP daemon
sudo service ntp start
```
