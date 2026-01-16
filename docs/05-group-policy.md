I first created an Organizational Unit (OU) structure consisting of Users, Groups, and Workstations.
This allowed me to logically organize directory objects, apply Group Policy settings selectively at the OU level,
and prepare the environment for scalable administration.

I then created Global Security Groups within the Groups OU, including groups for IT, HR, and Finance.
Global Security Groups are well-suited for representing user roles within a single domain and provide
a clean way to manage access through group membership rather than individual user configuration.
This approach simplifies onboarding and offboarding by allowing permissions to be adjusted centrally at the group level.

Next, I created user accounts within the Users OU. During this process, I encountered password restrictions enforced by the domain’s password policy.
For the purpose of this lab, I temporarily relaxed password complexity and length requirements to allow account creation and testing,
while understanding that stronger password policies should remain enforced in production environments.

Finally, I assigned users to their appropriate security groups to implement Role-Based Access Control (RBAC).
This ensures that access management scales efficiently,as permissions can be modified by changing group membership rather than updating individual user accounts.
