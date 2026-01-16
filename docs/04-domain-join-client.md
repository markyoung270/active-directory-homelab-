Joining a client to the domain allows Active Directory to apply centralized authentication, policies, and management controls directly to the workstation.
This step validates that DNS, Active Directory Domain Services, and network connectivity are functioning correctly, confirming that the foundational domain infrastructure is operational.

I began by creating a separate Windows 11 Pro client virtual machine using Hyper-V with Generation 2 settings.
This client VM was configured independently from DC01 and intended to function as a domain-joined workstation rather than a server.

I then configured networking on the client to ensure it could communicate with the domain controller.
The domain controller was set as the client’s DNS server, and both the server and client were connected to the same internal virtual switch to allow communication on a shared subnet.
After observing that the client was assigned an APIPA address, indicating that no DHCP service was available, I manually assigned a static IP address to the client so it could communicate reliably with the server.

Once networking was confirmed, I joined the client to the domain by specifying the homelab.local domain and authenticating with domain administrator credentials.
The domain join completed successfully, and the system was restarted to apply the changes.

I verified the join from the server by confirming that the client computer object appeared in Active Directory Users and Computers, indicating that the domain recognized the workstation.
I also performed client-side verification by logging in as a domain user and confirming the authentication context using the "whoami" command.

With successful verification from both the client and server perspectives, the client was fully integrated into the domain and ready for Group Policy application and centralized management.
