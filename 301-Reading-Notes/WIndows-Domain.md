Windows domains are typically used on large networks – corporate networks, school networks, and government networks. They are not something you will encounter at home unless you have a laptop provided by your employer or school.

## What is a Domain?
Windows domains provide network administrators with a way to manage many PCs and control them from one place. One or more servers – known as domain controllers – have control over the domain and the computers on it. Domains are generally made up of computers on the same local network. However, computers joined to a domain can continue communicating with their domain controller over VPN or Internet connection. This allows businesses and schools to remotely manage laptops they provide to their employees and students.

When a computer is joined to a domain, it does not use its own local user accounts. User accounts and passwords are managed on the domain controller. When you log into a computer on that domain, the computer authenticates your user account name and password with the domain controller. This means you can log in with the same username and password on any computer joined to the domain.

Network administrators can change group policy settings on the domain controller. All the settings are controlled from a single place. This “locks down” the computers and will not allow basic users the ability to change many system settings on a computer joined to a domain.

## My Computer Part of a Domain?
Home computers are almost certainly not part of a domain. If your computer is at work or at school, there is a good chance your computer is part of a domain.

## Quick Check whether your computer is part of a domain
1. Open Control Panel
2. System and Security category
3. System
4. Under “Computer Name”
5. If you see “Domain:” then your computer is joined to a domain
6. If you see “Workgroup:” then your computer is joined to a workgroup instead of a domain.

## Workgroup vs Domains
A workgroup is a group of computers on the same local network. Unlike on a domain, no computer on a workgroup has control over any other computer – they are all joined together as equals. A workgroup does not require a password, either.


Domain’s limit what you can do on your PC. When your computer is part of a domain, the domain controller oversees what you can do. Therefore, they are used on large corporate and educational networks – they provide a way for the institution that provides the computers to lock them down and centrally administer them. 