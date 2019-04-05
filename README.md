DNS (Domain Name System)

DNS is a hierarchical naming system that serves as a directory of networked hosts and resources. Information in the directory maps network names to data and is maintained in logical entries known as resource records (RR). The DNS hierarchy begins with the root domain (.) At the top and branches downward to multiple next-level domains. DNS is a hierarchical, distributed database. It stores information for mapping Internet host names to IP addresses and vice versa, mail routing information, and other data used by Internet applications.

Clients look up information in the DNS by calling a resolver library, which sends queries to one or more Name servers and interprets the responses. The BIND 9 software distribution contains a name server, named, and a resolver library, liblwres.







DOMAIN

It is a Collection of Resource Records that ends in a common Name and represents an entire sub tree of the DNS Name Space. A domain name is a label that identifies a network domain: a distinct group of computers under a central administration or authority. Within the Internet, domain names are formed by the rules and procedures of the Domain Name System. Any name registered in the DNS is a domain name.

          SUBDOMAIN is a Domain that is a sub tree of another Domain.








ZONES

A zone is a point of delegation in the DNS tree. A zone consists of those contiguous parts of the domain tree for which a name server has complete information and over which it has authority. It contains all domain names from a certain point downward in the domain tree except those which are delegated to other zones. A delegation point is marked by one or more NS records in the parent zone, which should be matched by equivalent NS records at the root of the delegated zone.




LOCAL INFRASTRUCTURE USED


MACHINE: DELL Inspiron 14   Laptop

CONFIG:  Co re I3 2.00GHZ CPU, 4GB RAM, 1TB HDD

OS:  REDHAT Linux el7.0.



Package & Conf files


Package: Bind 9.9.4

Configuration File:  /etc/named.conf

Service & Daemon: named.service

Port:  53/TCP, 53/UDP

Configuration Check utility: named-checkconf

Zone file check utility: named-checkzone


Basic Scenario: configure server.example.com as DNS server. It should resolve host names for other clients.


Domain = example.com

IP = 10.0.2.12

Hostname = server.example.com 


