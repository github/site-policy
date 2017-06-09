---
title: GitHub Security
redirect_from:
  - /security/
---
We know your code is extremely important to you and your business, and we're very protective of it. After all, GitHub's code is hosted on GitHub, too!

### Need to report a security vulnerability?

Please visit our [security bug bounty site](https://bounty.github.com) for information about our responsible disclosure process and to submit a vulnerability report.

### Physical Security

* Data center access limited to data center technicians and approved GitHub staff
* Biometric scanning for controlled data center access
* Security camera monitoring at all data center locations
* 24x7 onsite staff provides additional protection against unauthorized entry
* Unmarked facilities to help maintain low profile
* Physical security audited by an independent firm

### System Security

* System installation using hardened, patched OS
* Dedicated firewall and VPN services to help block unauthorized system access
* Distributed Denial of Service (DDoS) mitigation services powered by industry-leading solutions

### Operational Security

* Our primary data center operations are regularly audited by independent firms against an ISAE 3000/AT 101 Type 2 Examination standard
* Systems access logged and tracked for auditing purposes
* Secure document-destruction policies for all sensitive information
* Fully documented change-management procedures

### Software Security

We employ a team of 24/7/365 server specialists at GitHub to keep our software and its dependencies up to date eliminating potential security vulnerabilities. We employ a wide range of monitoring solutions for preventing and eliminating attacks to the site.

### Communications

All private data exchanged with GitHub is always transmitted over SSL (which is why your dashboard is served over HTTPS, for instance). All pushing and pulling of private data is done over SSH authenticated with keys, or over HTTPS using your GitHub username and password.

The SSH login credentials used to push and pull can not be used to access a shell or the filesystem. All users are virtual and have no user account on our machines.

### File system and backups

Every piece of hardware we use has an identical copy ready and waiting for an immediate hot-swap in case of hardware or software failure. Every line of code we store is saved on a minimum of three different servers, including an off-site backup. We do not retroactively remove repositories from backups when deleted by the user, as we may need to restore the repository for the user if it was removed accidentally.

We do not encrypt repositories on disk because it would not be any more secure: the website and git back-end would need to decrypt the repositories on demand, slowing down response times.  Any user with shell access to the file system would have access to the decryption routine, thus negating any security it provides. Therefore, we focus on making our machines and network as secure as possible.

### Employee access

No GitHub employees ever access private repositories unless required to for support reasons.  Staff working directly in the file store access the compressed Git database, your code is never present as plaintext files like it would be in a local clone.  Support staff may sign into your account to access settings related to your support issue.  In rare cases staff may need to pull a clone of your code, this will only be done with your consent.  Support staff does not have direct access to clone any repository, they will need to temporarily attach their SSH key to your account to pull a clone.  When working a support issue we do our best to respect your privacy as much as possible, we only access the files and settings needed to resolve your issue.  All cloned repositories are deleted as soon as the support issue has been resolved.

### Maintaining security

We protect your login from brute force attacks with rate limiting.  All passwords are filtered from all our logs and are one-way encrypted in the database using `bcrypt`.  Login information is always sent over SSL.

We also allow you to use [two-factor authentication](/articles/securing-your-account-with-two-factor-authentication-2fa), or 2FA, as an additional security measure when accessing your GitHub account. Enabling 2FA adds security to your account by requiring both your password as well as access to a security code on your phone to access your account.

We have full time security staff to help identify and prevent new attack vectors. We always test new features in order to rule out potential attacks, such as XSS-protecting wikis, and ensuring that Pages cannot access cookies.

We also maintain relationships with reputable security firms to perform regular penetration tests and ongoing audits of GitHub and its code.

We're extremely concerned and active about security, but we're aware that many companies are not comfortable hosting code outside their firewall. For these companies we offer [GitHub Enterprise](https://enterprise.github.com/), a version of GitHub that can be installed to a server within the company's network.

### Credit card safety

When you sign up for a paid account on GitHub, we do not store any of your card information on our servers. It's handed off to [Braintree Payment Solutions](https://braintreepaymentsolutions.com), a company dedicated to storing your sensitive data on [PCI-Compliant](http://en.wikipedia.org/wiki/Payment_Card_Industry_Data_Security_Standard) servers.

### Contact Us

Have a question, concern, or comment about GitHub security? Please contact {{ site.data.variables.contact.contact_support }}.
