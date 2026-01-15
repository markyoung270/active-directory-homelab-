The first task I completed was renaming the server to "DC01" (Domain Controller 01)
for clarity, ability to identify during troubleshooting, as well as appropriate logs
and auditing.

I established a static IP address for this Domain Controller for reliability and
pointed DNS to the same Domain Controller due to it's hosting DNS for the domain.

I then installed AD DS and DNS server roles. AD DS preforms the storage of users, groups,
computers, polices and provides the domain structure. DNS allow devices to locate what
they need. (--Is it necessary to spell out what AD DS and DNS do for recruiters?--)

I followed this up by promoting the server to domain controller and created a new forest.
The new domain is labeled "homelab.local". (--is this last sentence necessary?--)

I verified that my configuration was successful in ADUC (Active Directory Users and Computers). (--is this text in parethesis necessary?--)
Upon seeing "DC01" in the directory I understood that the promotion to domain controller was
successful.

I further verified DNS Manager to contain the necessary SRV records and structures to inform
clients where to find Kerberos, LDAP, as well as domain controller and replication services.
With this I ensured my domain controller registered itself correctly, clients are able to find
it, and I have a functioning active directory + DNS integration.
