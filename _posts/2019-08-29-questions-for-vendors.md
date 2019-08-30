---
layout: post
title: "Vendor Vanity & Value"
author: "trevor"
categories: blog
tags: [blog]
---

After thinking about a [thread I posted to Twitter](https://twitter.com/apporima/status/1108740025989189633?s=20) I had decided to write more about this subject of product selection in the U.S. Government. It's difficult for organizations to meet their modernization needs when the industry provides a lack of trust in suitable solutions. There's a lot of competitors to choose from, and Federal acquisitions enforces fair awarding, yet most vendors today have difficulty keeping up to the new solutions that they're offering. I've had to participate in very many vendor demonstrations where the sales person, sometimes without the engineer, has been able to successfully sell a solution that ultimately doesn't work as advertised.

The framework is simple. A call is made to or from various sales representatives, demonstrations are scheduled and performed from corporate laptops or cloud instances, then potential customer makes a selection based on the best presentation and begins the process with Acquisitions Management. This isn't always the case, but it's always the case. The customer just needs something that works, and when that thing deviates from the designed solutions architecture it then become the next problem for engineering teams to implement and integrate. If the customer happens to be the organization's business unit and they have a mission need to fulfill, then the purchase has probably already been made.

After much frustration, here is the strategy that I was able to implement.

## 1) Organizational Assessment

Know the objectives of your organization. Understand the services it provides and the capabilities needed to support those services. What is the problem that needs to be solved? Can it be resolved with existing solutions? How does this help the business? If these can't be answered before seeking outside support then there isn't a good enough reason to be looking. Sometimes the justification to move forward is the decision to abuse [funds](https://www.nber.org/digest/mar14/w19481.html).

It's important to ask these questions and receive the answers before scheduling any vendor demonstration. These will aid the selection process considerably.

## 2) Certified

What certifies the vendor's solution for use in Government? Do they meet [Common Criteria](https://www.us-cert.gov/bsi/articles/best-practices/requirements-engineering/the-common-criteria)? Is the solution subject to [Section 508](https://www.section508.gov/sell) or does it need to be [FIPS 140](https://csrc.nist.gov/publications/detail/fips/140/2/final) compliant?

Common Criteria allows vendors to select their security requirements and, with that, follow rigorous assessment ensuring that the product _actually_ meets the selected assurance requirements. This stage gate is the minimum to be able to begin to do business with the Government. A product that hasn't passed Common Criteria is a product that hasn't met the secure design, build, and implementation that is compulsory by the Government. The product will instead introduce weaknesses to the information system it's designed for and ultimately hurt the organization.

However, there can be some reasonable exceptions to consider when weighing the pros and cons of accepting a risk. In 2014, Microsoft shared that they [no longer recommended](https://blogs.technet.microsoft.com/secguide/2014/04/07/why-were-not-recommending-fips-mode-anymore/) enabling FIPS mode for their products for that time, which met end-of-life several years ago. This is because it's either too difficult to implement into the complex environment, or the resources needed to engineer may not be worth the longer haul. A lot of the time FIPS mode won't be enabled because it breaks the application's functionality. This can be in part to the Acquisition's Management team selecting products bypassing requirements by conflicting interest, dishonesty amongst the selection process, or unwilling and pass the accountability to somebody else. More often than not, the business doesn't actually know the risks that they accept and they are forced to approve a product for use, effectively bypassing requirements.

There is nothing wrong with asking the vendor to provide the certifications to you. In fact, I encourage you. If they say that they are [NIAP](https://www.niap-ccevs.org/) approved, ask them to show proof of that. Merely having a badge on a website doesn't have to be sufficient. They will provide you the ID to verify with the certifying authority.

## 3) Development Teams

### Closed Source

Ask the vendor if the development team(s) are internal or external. The answer for this question may tell you more about the company wanting to sell you their products. The company may have been acquired one or more times and has different external organizations, or it's just beginning and can't afford to have an internal development team. The company may not even have the solution yet and are attempting to secure a contract to garner the funds to begin creating the product. It's become one of the most popular strategies for doing business.

The answer that you want is internal. An external development team can show where the state of the company is in its growth and if it was recently acquired. Knowing this is important because this often leads to challenges with regular and emergency releases being slow and infrequent. Not having mature enough SDLC and ITSM processes in product development doesn't enable growth. The major updates, bug fixes, or general support are something left to be desired. We found this the hard way and discovered the vendor was unknowingly shipping different and faulty product releases across their customer base.

The goal is to work hard with design the first year, and implement the second year. Even better if that can be done in a shorter time frame. Otherwise, if it's longer then it may have been by agreeing to a contract disadvantaged to you, or not having the resources to _actually_ implement. This often leads to a solution that sits shelved and unused.

### Open Source

If the solution being reviewed is part of the Free and Open Source Software (FOSS) community then the placement of development teams doesn't factor as much as a concern. In FOSS, most teams are dispersed and that's how they succeed. Instead, looking for a project that's actively maintained and has support is what will be important here. The selected solution still needs to meet regulatory compliance, and if the supporting vendor chooses to keep parts of the software restricted then that can be the show stopper. We once had designed a compliance monitoring solution as part of our automated provisioning stack. The selected vendor ran CentOS under the hood, and because that wasn't NIAP approved, we needed to access and harden to produce a risk acceptance memorandum to the Authorizing Authority (AO). The vendor chose not to work with us and that ended our engagement with them. 

## 4) Quality Assurance

Does the vendor beta test its releases on its customers? If you have a security detection and response solution implemented on 100,000 endpoints and a new release leaves 10% unusable, what does that impact do to your organization? Is your organization part of 10% of the _entire_ customer base with a failed release? That's financial damage to your organization and a trap to avoid.

This question is important. I've found that companies will perform its capacity planning, performance testing, or general enterprise-wide deployments testing on its customers. Small companies won't have the internal resources to be able to perform these types of tests compared to large organizations. It's a risk that needs to be understood before moving forward. Sometimes it has to be accepted. Ensure there will be immediate support received. An enterprise-wide deployment that has a 10% failure rate could mean a lot of things, and that it can hurt the business and those who support it.

## 5) Support Cases

How many support tickets or cases go back to the development team(s)? I almost always prefer trusted vendors or open source these days because of the trauma I have from most suggestively simple support tickets becoming development tasks. In the past I had worked on a solution that was full of development bugs, possibly due to multiple company acquisitions and dispersed development teams. It was to the point where we had to have security cleared developers on-site to assess the bugs and send the fixes upstream to have resolved immediately. It was one of the most painful and cost accruing solutions I've had to endure. In fact, it was so bad that we received specialized hot fixes, then other customers would receive different hot fixes. The company ended up with a product of poorly managed software configuration versioning and major development updates would fail, amongst other issues discovered.

After the previous experience, we had accepted the risk to be able to test a major development release of a separate vendor product. We negotiated the contract to have on-site support so that the anticipated issues would be discovered and sent upstream quickly via employee back channels. This worked out very well because we wanted to pilot a solution early, which lead eventually lead to success at an enterprise scale.

## Moving forward

If the responses to the above questions are satisfied it's then time to schedule the demonstration. However, this should be continued under your conditions. Rather than having the vendor use their laptop or their own cloud instance, have the vendor demonstrate on your environment.

Request a trial license to the product, an engineering resource to be available, and begin implementing in the organization's existing (or a sandbox) testing environment that already meets security compliance requirements. If there are any challenges during product set up, that resource should be there to assist. Document what causes the set up to fail to install. Is the product not working with SELinux, or requires SYSTEM user to function? Does that deviate from the documentation? Does your team have to lax security configurations and introduce weaknesses to have a working product? Your effort will determine if the vendor tested their product in a STIG'd environment. Your Information Assurance teams may appreciate this and even work with you on documenting the risks. Any assistance towards resolution with certifying and authorizing can be helpful.

This approach has helped my teams navigate through the pains and establish great relationships with vendors supporting the Government. The approach eliminated low quality tool selection along with low quality decision making. People don't want their name tied to failed projects, and people don't want to deal with failed integrations. This helps them and you.
