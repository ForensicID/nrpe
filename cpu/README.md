# nrpe-check_cpu
### Package
sudo apt install sysstat

### Installation
cd /usr/local/nagios/libexec/

git clone git@github.com:ForensicID/nrpe-check_cpu.git

cp -R nrpe-check_cpu/check_cpu.sh .

chmod +x check_cpu.sh

### Example
/usr/local/nagios/libexec/check_cpu.sh -w 80 -c 90
