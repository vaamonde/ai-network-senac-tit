     Online state: online
    DNS Addresses: 127.0.0.53 (stub)
       DNS Search: .

●  1: lo ethernet UNKNOWN/UP (unmanaged)
      MAC Address: 00:00:00:00:00:00
        Addresses: 127.0.0.1/8
                   ::1/128

●  2: enp0s3 ethernet UP (networkd: enp0s3)
      MAC Address: 08:00:27:f7:9b:90 (Intel Corporation)
        Addresses: 10.24.82.201/24
                   fe80::a00:27ff:fef7:9b90/64 (link)
    DNS Addresses: 8.8.8.8
                   8.8.4.4
           Routes: default via 10.24.82.1 (static)
                   10.24.82.0/24 from 10.24.82.201 (link)
                   fe80::/64 metric 256

●  3: docker0 bridge UP (unmanaged)
      MAC Address: 0a:5e:55:9c:aa:65
        Addresses: 172.17.0.1/16
                   fe80::85e:55ff:fe9c:aa65/64 (link)
           Routes: 172.17.0.0/16 from 172.17.0.1 (link)
                   fe80::/64 metric 256
       Interfaces: veth8e4ad55

●  4: veth8e4ad55 virtual-ethernet UP (unmanaged)
      MAC Address: 96:b4:85:44:e8:c7
        Addresses: fe80::94b4:85ff:fe44:e8c7/64 (link)
           Routes: fe80::/64 metric 256
           Bridge: docker0

No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 24.04.4 LTS
Release:        24.04
Codename:       noble

