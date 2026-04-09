  UNIT                        LOAD   ACTIVE SUB     DESCRIPTION                                   
  apache2.service             loaded active running The Apache HTTP Server
  cron.service                loaded active running Regular background program processing daemon
  dbus.service                loaded active running D-Bus System Message Bus
  fwupd.service               loaded active running Firmware update daemon
  getty@tty1.service          loaded active running Getty on tty1
  grafana-server.service      loaded active running Grafana instance
  ModemManager.service        loaded active running Modem Manager
  multipathd.service          loaded active running Device-Mapper Multipath Device Controller
  mysql.service               loaded active running MySQL Community Server
  node_exporter.service       loaded active running Node Exporter
  polkit.service              loaded active running Authorization Manager
  prometheus.service          loaded active running Prometheus
  rsyslog.service             loaded active running System Logging Service
  ssh.service                 loaded active running OpenBSD Secure Shell server
  systemd-journald.service    loaded active running Journal Service
  systemd-logind.service      loaded active running User Login Management
  systemd-networkd.service    loaded active running Network Configuration
  systemd-resolved.service    loaded active running Network Name Resolution
  systemd-timesyncd.service   loaded active running Network Time Synchronization
  systemd-udevd.service       loaded active running Rule-based Manager for Device Events and Files
  tomcat11.service            loaded active running Apache Tomcat11

   users:(("sshd",pid=1636,fd=3),("systemd",pid=1,fd=203))
LISTEN        0             100                              *:8080                             *:*            users:(("java",pid=751,fd=44))
LISTEN        0             4096                             *:9100                             *:*            users:(("node_exporter",pid=793,fd=3))
LISTEN        0             4096                             *:9091                             *:*            users:(("prometheus",pid=798,fd=6))
LISTEN        0             4096                             *:3000  '                           *:*            users:(("grafana",pid=1029,fd=11))
LISTEN        0             511                              *:8888                             *:*            users:(("apache2",pid=3562,fd=6),("apache2",pid=3561,fd=6),("apache2",pid=3560,fd=6),("apache2",pid=3559,fd=6),("apache2",pid=3558,fd=6),("apache2",pid=886,fd=6))
LISTEN        0             70                               *:33060                            *:*            users:(("mysqld",pid=879,fd=21))
LISTEN        0             511                              *:80                               *:*            users:(("apache2",pid=3562,fd=4),("apache2",pid=3561,fd=4),("apache2",pid=3560,fd=4),("apache2",pid=3559,fd=4),("apache2",pid=3558,fd=4),("apache2",pid=886,fd=4))
