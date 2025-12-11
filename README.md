# 🔍 NRPE Custom Plugins

Kumpulan *custom script* (plugin) untuk **NRPE (Nagios Remote Plugin Executor)**. Script ini digunakan untuk memonitor metrik spesifik pada server klien yang kemudian datanya dikirim ke server monitoring utama (Nagios/Icinga2/Zabbix).

---
## RAM

```bash
cd /usr/local/nagios/libexec/
wget https://raw.githubusercontent.com/ForensicID/nrpe-plugin/refs/heads/main/check_mem
chmod +x check_mem
```

## CPU

```bash
cd /usr/local/nagios/libexec/
wget https://raw.githubusercontent.com/ForensicID/nrpe-plugin/refs/heads/main/check_cpusage.sh
chmod +x check_cpusage.sh
```

## NETWORK

```bash
cd /usr/local/nagios/libexec/
wget https://raw.githubusercontent.com/ForensicID/nrpe-plugin/refs/heads/main/check_bandwidth
chmod +x check_bandwidth
```

## DATABASE

```bash
cd /usr/local/nagios/libexec/
wget https://raw.githubusercontent.com/ForensicID/nrpe-plugin/refs/heads/main/check_mysql_query.pl
chmod +x check_mysql_query.pl
```

## Command and Parameter

```bash
command[check_mem]=/usr/local/nagios/libexec/check_mem -f -w 20 -c 10
command[check_netstat]=/usr/local/nagios/libexec/check_bandwidth 100 500 100 500
command[check_cpusage]=/usr/local/nagios/libexec/check_cpusage.sh -w 80 -c 90
command[check_database]=/usr/local/nagios/libexec/check_mysql_query.pl -H 127.0.0.1 -u username -p password
```
---

## 🛠️ Requirements

* **OS:** Linux (Debian/Ubuntu/CentOS).
* **Package:** `nagios-nrpe-server`, `nagios-plugins`.
* **Dependencies:** Beberapa script mungkin membutuhkan paket tambahan seperti `bc`, `jq`, atau `sysstat` (pastikan cek header script masing-masing).

---

## 🤝 Kontribusi
Jika Anda memiliki ide script monitoring baru, silakan buat *Pull Request* atau taruh di folder kategori yang sesuai.
