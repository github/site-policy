---
title: GitHub Sensitive Data Removal Policy
---
If you believe that content on GitHub infringes rights you hold in it, please see our [DMCA Takedown Policy](/articles/dmca-takedown-policy/) and our [Guide to Submitting a DMCA Takedown Notice](/articles/guide-to-submitting-a-dmca-takedown-notice/). We rely on the DMCA notice and takedown process for the majority of our removal actions.

However, we understand that sensitive, security-related content may get published on GitHub – whether accidentally or on purpose – from time to time. We provide our Sensitive Data Removal process to remove this Sensitive Data in certain exceptional circumstances where the DMCA process would not be applicable, such as when your security is at risk from exposed passwords and you do not own the copyright to the specific content that you need removed, or the content is not protectable by copyright. This guide describes the information GitHub needs from you in order to process a request to remove Sensitive Data from a repository.

### What is Sensitive Data?

For the purposes of this document, “Sensitive Data” refers to content that should have been kept confidential and whose public availability poses a specific or targeted security risk to you or your organization.

#### Sensitive Data removal requests are appropriate for:
- Access credentials, such as user names along with passwords, access tokens, or other sensitive secrets that can grant access to your organization's server, network, or domain.
- AWS tokens and other similar access credentials that grant access to a third party on your behalf. You must be able to show that the token does belong to you.
- Documentation (such as network diagrams) that pose a specific security risk for an organization. As discussed below, internal server names, on their own, are not sufficiently sensitive; you must be able to show that the internal server name's use in a particular file or piece of code poses a security threat.

#### Sensitive Data removal requests are _not_ appropriate for:
-  Requests to remove content that may infringe your or your organization's copyright rights. If you have questions about how GitHub handles copyright-related matters or would like us to remove potentially infringing content, please review our [DMCA Takedown Policy](/articles/dmca-takedown-policy/).
- Trademark disputes. If you have questions about how GitHub handles trademark-related matters or would like us to remove content containing your organization's trade or service marks, please review our [Trademark Policy](/articles/github-trademark-policy/).
- Privacy complaints. If you have concerns about your own privacy or you are contacting us on behalf of your employees due to a privacy concern, please contact us via [our Privacy contact form](https://github.com/contact/privacy).
- Entire files or repositories that do not pose a specific security risk, but you believe are otherwise objectionable. This process is not generally intended for the removal of copyrightable content, such as full files or repositories – only for the specific pieces of Sensitive Data in those files. If you believe a full file is infringing, please follow our [DMCA process](/articles/dmca-takedown-policy/). While there may be cases where files are filled entirely with sensitive information, you must justify the security risk for the removal of such files, and this may increase the time required to process your request.
- Content governed by our [Community Guidelines](/articles/github-community-guidelines/), such as malware or general-purpose tools. If you have questions about our Community Guidelines or believe that content on GitHub might violate our guidelines, please [contact our Support Team](https://github.com/contact/).
- Mere mentions of your company's identity, name, brand, domain name, or other reference to your company in files on GitHub. You must be able to articulate why a use of your company's identity is a threat to your company's security posture before we will take action under this policy.

### Things to Know

**Investigate.** It is up to the requesting party to conduct their own investigation and to provide us with the details we require. GitHub is not in a position to search for or make determinations about Sensitive Data on any indvidual's or organization's behalf.

**Ask Nicely First.** A great first step before sending us a request to remove data is to try contacting the user directly. They may have listed contact information on their public profile page or in the repository's README or Support file, or you could get in touch by opening an issue or pull request on the repository. This is not strictly required, but it is appreciated.

**No Bots.** You should have a trained professional evaluate the facts of every request you send. If you're outsourcing your efforts to a third party, make sure you know how they operate, and make sure they are not using automated bots to submit complaints in bulk. These complaints are often invalid and the extra back-and-forth required when we receive such reports results in delays, even when the complaint is valid.

**The Repository Owner(s) May Dispute Your Request.** Any user affected by your request may decide to dispute your request. If they do, we will generally leave it up to you to contact the user and work things out with them directly, within reason.

**Send In The Correct Request.** We offer this Sensitive Data Removal process as an exceptional service only for high-risk content. We are not able to use this process to remove other kinds of content, such as potentially infringing content, and we are not able to process any other kinds of removal requests simultaneously while processing sensitive removal requests. We will be able to help you more quickly if you send in your Sensitive Data removal requests separately from any requests to remove potentially infringing content. If you are unsure whether your request involves only Sensitive Data or also involves other legal matters, please consult legal counsel.

**Processing Time.** While we do process Sensitive Data Removal Requests as quickly as possible, due to the volume of requests we process, it may take three to four business days for your request to be reviewed. Additional requests, or multiple requests from additional points of contact, may result in delays.

#### What About Forks? (or What's a Fork?)
One of the best features of GitHub is the ability for users to "fork" one another's repositories. What does that mean? In essence, it means that users can make a copy of a project on GitHub into their own repositories. As the license or the law allows, users can then make changes to that fork to either push back to the main project or just keep as their own variation of a project. Each of these copies is a "[fork](/articles/github-glossary/#fork)" of the original repository, which in turn may also be called the "parent" of the fork.

GitHub will not automatically disable forks when disabling a parent repository. This is because forks belong to different users and may have been altered in significant ways. GitHub does not conduct any independent investigation into forks. We expect those sending sensitive data removal requests to conduct that investigation and, if they believe that the forks also contain sensitive data, expressly include forks in their request.

### Sending A Sensitive Data Removal Request

Due to the type of content GitHub hosts (mostly software code) and the way that content is managed (with Git), we need complaints to be as specific as possible. In most situations, when we receive a complete and actionable request to remove Sensitive Data, we pass that request (with any personally identifying information redacted) along to the repository owner. In order for us to verify that the owner has removed the data completely, we need to know exactly where to look.

These guidelines are designed to make the processing of requests to remove Sensitive Data as straightforward as possible.

#### Your Request Must Include:

1. A working link to each file containing Sensitive Data.
2. Specific line numbers within each file containing the Sensitive Data OR a clear indication that an entire file contains Sensitive Data.
3. A brief description of how each item you've identified poses a security risk to you or your organization.
4. If you are a third party acting as an agent for an organization facing a security risk, include a statement that you have a legal right to act on behalf of that organization.
5. OPTIONAL: Let us know if your request is particularly urgent, and why. We respond to all Sensitive Data Removal Requests as quickly as possible. However, if this request is especially time-sensitive, such as a very recent credential exposure, please explain why.

### How to Submit Your Request

You can email your request to remove Sensitive Data to <a href="mailto:support@github.com" data-proofer-ignore>support&#64;github.com</a> or submit your request via our [Contact form](https://github.com/contact/). Please include a plain-text version of your request in the body of your message. Sending your request in an attachment may result in processing delays.
