Group Policy is a feature of Windows that facilitates a wide variety of advanced settings that network administrators can use to control the working environment of users and computer accounts in Active Directory. Provides a centralized place for administrators to manage and configure operating systems, applications and user's settings. 

Group Policies, when used correctly, can enable you to increase the security of user's computers and help defend against both insider threats and external attacks.

Group Policy Object is a group of settings that are created using the Microsoft Management Console (MMC) Group Policy Editor. GPOs can be associated with a single or numerous Active Directory containers, including sites, domains, or organizational units(OUs). Active Directory applies GRPs in the same , logical order; local policies, site policies, domain policies and OU policies. 

## Examples of GPOs

Group Policy Objects can be used in a number of ways that benefit security. A few specific examples: 
* A Group Policy Object could be used to determine the home page that a user sees when they launch their internet browser after logging onto the domain. 
* Administrators can use GPOs to define which network connected printers appear on the list of available printers after a user in a specific Active Directory OU logs onto the domain. 
* Admins can also use GPOs to tweak a number of security protocols and practices such as restricting internet connection options, programs and even screen time.

## Benefits of Group Policy for Data Security

* Password Policy: Many organizations are operating with relaxed password policies, with many users often having passwords set to never expire. Passwords that aren't regularly rotated, are too simple of use common passphrases are at risk of being hacked through brute force. GPOs can be used to establish password length, complexity and other requirements. 
* System Management: GPOs can be used to simplify tasks that are at best mundane and at worst critically time consuming. You can save yourself hours and hours of time configuring the environment of new users and computers joining your domain by using GPOs to apply a standardized universal one.
* Health Checking: GPOs can be used to deploy software updates and system patches to ensure your environment is healthy and up to date against the latest security threats.

## Limitations of Group Policy

* GPO editor isn't the most user-friendly console that you're likely to come across. A deep understanding of PowerShell will help make it easier to do all the GPO updates.
* GPOs are not immune to cyberattacks. If an attacker wanted to change local GPOs on a computer in order to move laterally across the network, it would be very difficult to detect this without a Group Policy auditing and monitoring solution in place.