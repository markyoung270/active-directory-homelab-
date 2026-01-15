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


