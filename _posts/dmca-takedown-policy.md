---
title: DMCA Takedown Policy
redirect_from:
  - /dmca/
  - /dmca-takedown/
  - /dmca-takedown-policy/
  - /articles/dmca-takedown/
---

Welcome to GitHub's Guide to the Digital Millennium Copyright Act, commonly known as the "DMCA." This page is not meant as a comprehensive primer to the statute. However, if you've received a DMCA takedown notice targeting content you've posted on GitHub or if you're a rights-holder looking to issue such a notice, this page will hopefully help to demystify the law a bit as well as our policies for complying with it.

(If you just want to submit a notice, you can [skip to the end](#f-submitting-notices).)

As with all legal matters, it is always best to consult with a professional about your specific questions or situation. We strongly encourage you to do so before taking any action that might impact your rights. This guide isn't legal advice and shouldn't be taken as such.

### What Is the DMCA?

In order to understand the DMCA and some of the policy lines it draws, it's perhaps helpful to consider life before it was enacted.

Before the DMCA, an Internet-based service provider like GitHub could be liable for copyright infringement in the United States just for hosting its users' pictures, music, videos or code. This was true even if it had no actual knowledge of any infringing content. This was a problem, since even a single claim of copyright infringement can carry statutory damages of up to $150,000. With potential damages that high multiplied across millions of users, cloud-computing and user-generated content sites like YouTube, Facebook or GitHub probably [never would have existed](http://arstechnica.com/tech-policy/2015/04/how-the-dmca-made-youtube/) (or at least not without passing some of that cost downstream to their users).

The DMCA attempted to fix this problem by creating a so-called copyright liability "safe harbor" for internet service providers hosting allegedly infringing user-generated content. (*See* [U.S. Code, Title 17, Section 512](http://www.copyright.gov/title17/92chap5.html#512).) Essentially, so long as a service provider follows the DMCA's notice-and-takedown rules, it won't be liable for copyright infringement based on user-generated content. Because of this it is important for GitHub to maintain its DMCA safe-harbor status.

### DMCA Notices In a Nutshell

The DMCA provides two simple, straightforward procedures that all GitHub users should know about: (i) a [takedown-notice](/articles/guide-to-submitting-a-dmca-takedown-notice) procedure for copyright holders to request that content be removed; and (ii) a [counter-notice](/articles/guide-to-submitting-a-dmca-counter-notice) procedure for users to get content reenabled when content is taken down by mistake.

DMCA [takedown notices](/articles/guide-to-submitting-a-dmca-takedown-notice) are used by copyright owners to ask GitHub to take down infringing content. If you are a software designer or developer, you create copyrighted content every day. If someone else is using your copyrighted content in an unauthorized manner on GitHub you can send us a DMCA takedown notice to request that the infringing content be changed or removed.

On the other hand, [counter notices](/articles/guide-to-submitting-a-dmca-counter-notice) can be used to correct mistakes. Maybe the person sending the takedown notice does not hold the copyright or did not realize that you have a license or  made some other mistake in their takedown notice. Since GitHub usually cannot know if there has been a mistake, the DMCA counter notice allows you to let us know and ask that we put the content back up.

### A. How Does This Actually Work?

The DMCA framework is a bit like passing notes in class. The copyright owner hands GitHub a complaint about a user. If it's written correctly, we pass the complaint along to the user. If the user disputes the complaint, they can pass a note back saying so. GitHub exercises little discretion in the process other than determining whether the notices meet the minimum requirements of the DMCA. It is up to the parties (and their lawyers) to evaluate the merit of their claims, bearing in mind that notices must be made under penalty of perjury.

Here are the basic steps in the process.

1. **Copyright Owner Investigates.** A copyright owner should always conduct an initial investigation to confirm both (a) that they own the copyright to an original work and (b) that the content on GitHub is unauthorized and infringing.
> **Example:** An employee of Acme Web Company finds some of the company's code in a GitHub repository. Acme Web Company licenses its source code out to several trusted partners. Before sending in a take-down notice, Acme should review those licenses and its agreements to confirm that the code on GitHub is not authorized under any of them.

2. **Copyright Owner Sends A Notice.** After conducting an investigation, a copyright owner prepares and sends a [takedown notice](/articles/guide-to-submitting-a-dmca-takedown-notice) to GitHub. Assuming the takedown notice is sufficiently detailed according to the statutory requirements (as explained in the [how-to guide](/articles/guide-to-submitting-a-dmca-takedown-notice)), we will [post the notice](#d-transparency) to our [public repository](https://github.com/github/dmca) and pass the link along to the affected user.

3. **GitHub Asks User to Make Changes.** If the notice alleges that the entire contents of a repository infringe, we will skip to Step 6 and disable the entire repository expeditiously. Otherwise, because GitHub cannot disable access to specific files within a repository, we will contact the user who created the repository and give them approximately 24 hours to delete or modify the content specified in the notice. We'll notify the copyright owner if and when we give the user a chance to make changes.

4. **User Notifies GitHub of Changes.** If the user chooses to make the specified changes, they *must* tell us so within the approximately 24-hour window. If they don't, we will disable the repository (as described in Step 6). If the user notifies us that they made changes, we will verify that the changes have been made and then notify the copyright owner.

5. **Copyright Owner Revises or Retracts the Notice.** If the user makes changes, the copyright owner must review them and renew or revise their takedown notice if the changes are insufficient. GitHub will not take any further action unless the copyright owner contacts us to either renew the original takedown notice or submit a revised one. If the copyright owner is satisfied with the changes, they may either submit a formal retraction or else do nothing. GitHub will interpret silence longer than two weeks as an implied retraction of the takedown notice.

6. **GitHub May Disable Access to the Content.** GitHub will disable a user's content if: (i) the copyright owner has alleged copyright over the user's entire repository (as noted in Step 3); (ii) the user has not made any changes after being given an opportunity to do so (as noted in Step 4); or (iii) the copyright owner has renewed their takedown notice after the user had a chance to make changes. If the copyright owner chooses instead to *revise* the notice, we will go back to Step 2 and repeat the process as if the revised notice were a new notice.

7. **User May Send A Counter Notice.** We encourage users who have had content disabled to consult with a lawyer about their options. If a user believes that their content was disabled as a result of a mistake or misidentification, they may send us a [counter notice](/articles/guide-to-submitting-a-dmca-counter-notice). As with the original notice, we will make sure that the counter notice is sufficiently detailed (as explained in the [how-to guide](/articles/guide-to-submitting-a-dmca-counter-notice)). If it is, we will [post it](#d-transparency) to our [public repository](https://github.com/github/dmca) and pass the notice back to the copyright owner by sending them the link.

8. **Copyright Owner May File a Legal Action.** If a copyright owner wishes to keep the content disabled after receiving a counter notice, they will need to initiate a legal action seeking a court order to restrain the user from engaging in infringing activity relating to the content on GitHub. In other words, you might get sued. If the copyright owner does not give GitHub notice within 10-14 days, by sending a copy of a valid legal complaint filed in a court of competent jurisdiction, GitHub will reenable the disabled content.

### B. What About Forks? (or What's a Fork?)

One of the best features of [Git](https://git-scm.com/book/en/Getting-Started-Git-Basics) is the ability for users to "fork" one another's repositories. What does that mean? In essence, it means that users can make a copy of a project and then make changes to that copy to either push back to the main project or just keep as their own variation of a project. We call each of these copies a "[fork](/articles/github-glossary#fork)" of the original repository, which in turn may also be called the "parent" of the fork.

GitHub *will not* automatically disable forks when disabling a parent repository. This is because forks belong to different users, may have been altered in significant ways, and may be licensed or used in a different way that is protected by the fair-use doctrine. GitHub does not conduct any independent investigation into forks. We expect copyright owners to conduct that investigation and, if they believe that the forks are also infringing, expressly include forks in their takedown notice.

### C. What If I Inadvertently Missed the Window to Make Changes?

We recognize that there are many valid reasons that you may not be able to make changes within the approximate 24-hour window we provide before your repository gets disabled. Maybe our message got flagged as spam, maybe you were on vacation, maybe you don't check that email account regularly, or maybe you were just busy. We get it. If you respond to let us know that you would have liked to make the changes, but somehow missed the first opportunity, we will re-enable the repository one additional time for approximately 24 hours to allow you to make the changes. Again, you must notify us that you have made the changes in order to keep the repository enabled after that 24-hour window, as noted above in [Step A.4](#a-how-does-this-actually-work). Please note that we will only provide this one additional chance.

### D. Transparency

We believe that transparency is a virtue. The public should know what content is being removed from GitHub and why. An informed public can notice and surface potential issues that would otherwise go unnoticed in an opaque system. We post redacted copies of any legal notices we receive (including original notices, counter notices or retractions) at <https://github.com/github/dmca>. We will not publicly publish your personal contact information; we will remove personal information (except for usernames in URLs) before publishing notices. We will not, however, redact any other information from your notice unless you specifically ask us to. Here are some examples of a published [notice](https://github.com/github/dmca/blob/master/2014/2014-05-28-Delicious-Brains.md) and [counter notice](https://github.com/github/dmca/blob/master/2014/2014-05-01-Pushwoosh-SDK-counternotice.md) for you to see what they look like. When we remove content, we will post a link to the related notice in its place.

Please also note that, although we will not publicly publish unredacted notices, we may provide a complete unredacted copy of any notices we receive directly to any party whose rights would be affected by it.  

### E. Repeated Infringement

It is the policy of GitHub, in appropriate circumstances and in its sole discretion, to disable and/or terminate the accounts of users who may infringe upon the copyrights or other intellectual property rights of GitHub and/or others.

### F. Submitting Notices

If you are ready to submit a notice or a counter notice:
- [How to Submit a DMCA Notice](/articles/guide-to-submitting-a-dmca-takedown-notice)
- [How to Submit a DMCA Counter Notice](/articles/guide-to-submitting-a-dmca-counter-notice)

### Learn More and Speak Up

If you poke around the Internet, it is not too hard to find commentary and criticism about the copyright system in general and the DMCA in particular. While GitHub acknowledges and appreciates the important role that the DMCA has played in promoting innovation online, we believe that the copyright laws could probably use a patch or two—if not a whole new release. In software, we are constantly improving and updating our code. Think about how much technology has changed since 1998 when the DMCA was written. Doesn't it just make sense to update these laws that apply to software?

We don't presume to have all the answers. But if you are curious, here are a few links to scholarly articles and blog posts we have found with opinions and proposals for reform:

- [Unintended Consequences: Twelve Years Under the DMCA](https://www.eff.org/wp/unintended-consequences-under-dmca) (Electronic Frontier Foundation)
- [Statutory Damages in Copyright Law: A Remedy in Need of Reform](http://papers.ssrn.com/sol3/papers.cfm?abstract_id=1375604) (William & Mary Law Review)
- [Is the Term of Protection of Copyright Too Long?](http://the1709blog.blogspot.com/2012/11/is-term-of-protection-of-copyright-too.html) (The 1709 Blog)
- [If We're Going to Change DMCA's 'Notice & Takedown,' Let's Focus on How Widely It's Abused](https://www.techdirt.com/articles/20140314/11350426579/if-were-going-to-change-dmcas-notice-takedown-lets-focus-how-widely-its-abused.shtml) (TechDirt)
- [Opportunities for Copyright Reform](http://www.cato-unbound.org/issues/january-2013/opportunities-copyright-reform) (Cato Unbound)
- [Fair Use Doctrine and the Digital Millennium Copyright Act: Does Fair Use Exist on the Internet Under the DMCA?](http://digitalcommons.law.scu.edu/lawreview/vol42/iss1/6/) (Santa Clara Law Review)

GitHub doesn't necessarily endorse any of the viewpoints in those articles. We provide the links to encourage you to learn more, form your own opinions, and then reach out to your elected representative(s) (e.g, in the [U.S. Congress](http://whoismyrepresentative.com/) or [E.U. Parliament](http://www.europarl.europa.eu/meps/en/map.html)) to seek whatever changes you think should be made.
