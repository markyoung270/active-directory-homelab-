The first issue I encountered occurred when I attempted to start the virtual machine without attaching an ISO.
This resulted in a standard “no operating system found” error and a UEFI boot summary screen. After identifying the cause,
I downloaded the Windows Server 2022 ISO and attached it to the VM’s virtual DVD drive.
I also adjusted the boot order to ensure the system attempted to boot from the DVD first.
This reinforced the importance of having proper installation media available and verifying boot configuration when provisioning virtual machines.

The second issue involved keyboard input not being recognized within Hyper-V.
Initially, pressing keys had no effect even when prompted to “press any key” to continue the boot process.
I attempted several troubleshooting steps, including clicking inside the VM window, resizing the window,
and restarting the virtual machine multiple times. Eventually, the VM successfully captured keyboard input.
This highlighted how virtualization layers can introduce interaction issues between host and guest systems.

The third issue occurred while documenting my work on GitHub.
I encountered a 503 error when attempting to access my repository, indicating a possible service outage.
Since my internet connection was functioning normally, I suspected the issue was server-side.
I checked GitHub’s official status page, which showed normal operations,
and then verified the issue using DownDetector, where multiple users reported similar problems.
I continued documenting my work locally with the intention of uploading it once GitHub services stabilized.

I experienced a client VM boot failure related to network adapter configuration during initial setup.
The VM was attached to the default virtual switch, which introduced inconsistent behavior during early Windows installation
due to network boot attempts and external connectivity dependencies. To ensure a clean and deterministic installation, I temporarily
removed network connectivity so the system would boot strictly from the installation media. After the operating system initialized successfully,
I reattached the VM to the appropriate virtual switch to restore connectivity.

The Windows 11 installation was initially blocked by TPM requirements.
When prompted, I closed the VM, opened its settings, and enabled virtual TPM and Secure Boot capabilities.
After restarting the VM, the installation proceeded without further issue.
This demonstrated the importance of aligning virtualization security settings with modern operating system requirements.

During Windows 11 setup, the installer required an internet connection with no visible option to bypass this requirement.
To continue setup in an isolated lab environment, I used the OOBE\BYPASSNRO command to restart the out-of-box experience and create a local account without requiring external connectivity.

After initialization, the client system was unable to locate the domain controller during the domain join process due to incorrect DNS settings.
I corrected this by manually configuring the client’s DNS server to point to the static IP address of the domain controller,
which was hosting DNS services for the domain. Once updated, domain name resolution functioned as expected.

Following the DNS correction, the client system was assigned an APIPA address, indicating the absence of a DHCP service.
I verified that both the client and server were not using the same virtual switch and corrected this by creating an internal virtual switch and attaching both systems to it.
I then manually assigned a static IP address to the client to ensure it operated on the same subnet as the domain controller.
This static configuration was implemented specifically for lab purposes rather than deploying a DHCP server.

Finally, while testing account lockout behavior, I attempted to enforce a password change requirement following an account unlock.
This initially prevented successful login because the existing password had expired and no replacement password had been provided.
I resolved this by performing a proper password reset, unlocking the account, and verifying successful login and password change from the client system.



