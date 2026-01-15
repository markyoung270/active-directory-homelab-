The first task I completed was renaming the server to DC01 (Domain Controller 01) to follow a clear naming convention.
This makes the system easier to identify during troubleshooting, logging, and auditing activities.

I then configured a static IP address for the domain controller to ensure consistent network identification and reliability.
I also pointed the DNS settings to the same server, since it is hosting DNS services for the domain.
This prevents connectivity issues and ensures clients can reliably locate the domain controller.

Next, I installed the Active Directory Domain Services (AD DS) and DNS Server roles.
AD DS stores and manages domain objects such as users, groups, computers, and policies, while DNS enables devices to locate domain services across the network.

After installing these roles, I promoted the server to a domain controller and created a new forest. The domain was named homelab.local.

I verified that the configuration was successful by using Active Directory Users and Computers (ADUC).
Seeing the DC01 computer object within the directory confirmed that the promotion process completed successfully.

I further validated the setup by reviewing DNS Manager and confirming the presence of the required SRV records and domain
structures. These records inform client devices where to locate Kerberos authentication, LDAP directory services, and domain controller replication endpoints.
This verification confirmed that the domain controller registered correctly and that Active Directory and DNS are functioning together as expected.
