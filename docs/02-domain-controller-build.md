Initially, I attempted to boot the virtual machine without attaching an ISO, which resulted in a boot error indicating that no operating system was present.
After identifying the issue, I downloaded the Windows Server 2022 ISO and attached it as DVD media in Hyper-V,
ensuring the DVD drive was first in the boot order so the system would load the installer correctly.

I selected Windows Server 2022 Standard (Desktop Experience) in order to gain hands-on experience with the graphical interface used to manage
Active Directory and related services. This also allowed me to properly document my configuration steps with screenshots for my repository.

I performed a custom installation rather than an upgrade to ensure a clean and predictable server deployment, which is standard practice when provisioning new systems.

After installation, I logged in and explored Server Manager, familiarizing myself with the interface used to install server roles,
manage features, and review system events and services.
