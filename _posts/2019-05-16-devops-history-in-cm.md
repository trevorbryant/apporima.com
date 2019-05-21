---
layout: post
title: "DevOps: A History in Configuration Management"
author: "trevor"
categories: blog
tags: [blog]
---

Earlier this week I shared the history of the engineering practice of Configuration Management (CM) at our local [DevOps DC](https://www.meetup.com/DevOpsDC/events/jkpfmlyzhbsb/) Meetup. I was pleasantly surprised to find that most of the attendees didn't seem to be aware of CM and what it has to do with their personal or professional lives.

In my slides located [here](/assets/slides/devops_history_config_mgmt.pdf), I had began my talk and asked what CM meant to everyone. I was met with explanations such as a tool solution, a process within DevOps, or activities that would typically be under Software Configuration Management (SCM). I had explained that the phrase is defined in the Military Handbook: Configuration Management Guidance (or MIL-HDBK-61 for short). In short, CM is defined as:

**_The practice of handling changes systematically so that a system maintains its integrity over time._**

I was surprised to find that this isn't commonly known. When I first began working professionally, I was given a book about Carnegie Mellon's _Capability Maturity Model Integration_ (CMMI) which was my introduction into the fast-paced world of Systems Development Lifecycle (SDLC). As it turned out, the Department of Defense (DOD) contracted research institutions back in the late '80s, and by the end of the 90s the first Military Handbook dedicated to CM is drafted in 1997. However, the lost art of CM is mentioned [even earlier](https://apps.dtic.mil/dtic/tr/fulltext/u2/a047308.pdf) when a program document is prepared for the United States Air Force (USAF) as early as 1977. This teaches us a few things:

  1. All the cool things started in Hanscom Air Force Base
  2. The USAF is pretty damn smart and really cool
  3. All the cool things died in Hanscom Air Force Base 

And, all of this makes a whole lot of sense. Post World War II (WWII), the United States Military needed ways to build repeatable weapons systems be it naval warships, fighter jets, or reconnaissance aircrafts. These are all life and limb systems and having superb, risk-managed for engineering, auditing, and verification was the way forward. I started to really nerd out about this and learned about Clarence "Kelly" Johnson, who ran Lockheed's Skunk Works program was a lot of this was fruitioned.

I know, what does this have to do with DevOps? Well, in the book [_Skunk Works: A Personal Memoir of My Years of Lockheed_](https://books.google.com/books/about/Skunk_Works.html?id=L-zAQgAACAAJ&source=kp_book_description) by Ben Rich it's explained that Johnson ran his programs under extremely strict circumstances, being top secret and all. He developed [14 rules](https://www.lockheedmartin.com/en-us/who-we-are/business-areas/aeronautics/skunkworks/kelly-14-rules.html) that he used to run all of his programs and teams. Once I saw these I immediately began to wonder if this set the foundation of how Federal contracting is performed today. But, Ben Rich expounds upon Johnson's rules and talks about how he required all of his staff to work within closed yet close quarters. He wanted his engineers next to his physicists, next to his designers and architects, and also the quality assurers, auditors and verifiers. He needed his staff close together so that they could communicate and solve problems faster. If they were beyond arm's length, they were too far to be efficient. That alone is what organizations strive for today; breaking down team barriers for fast and efficient service delivery.

Humorously, there was an unwritten 15th rule.

**_Starve before doing business with the damned Navy. They don't know what the hell they want and will drive you up a wall before they break either your heart or a more exposed part of your anatomy._**

The Air Force rools and the Navy drools. Got it.

Going back to the basics: CMMI and MIL-HDBK-61. They aren't actually so basic. The long reads goes on to explain implementation of systems engineering processes organizations can adopt. It even has a scoring system! But, they are complex and complicated process implementations. There wasn't any room for error because that resulted in a failed mission and potential loss of life.

So, when I began working professionally and I had just finished the massive book of CMMI, the United States Government (USG) had heard of the Information Technology Infrastructure Library (ITIL). I was pretty mad about that, but whatever -- I had a paying job. When I began reading the ITIL Foundation's I quickly learned that most of the information in there doesn't apply to the USG because it doesn't comply with our Federal laws and requirements. But you know what? It's a framework, and we can work with that. The real beauty of frameworks is that no matter which methodology is chosen, the organization can apply the areas it needs in order to improve. This worked out great for me because I was 22 and explaining this to people that were much older and weren't seeing the correlations of their existing processes and able to map that to new terminologies and vocabularies.

A bit of background for you, Reader. If you don't know me too well, you may not know that I _really_ complain about the things that I don't like. I'll explain this one to you now. As I was helping this particular Federal agency modernize their processes, I was introduced to the third party consultant. I first experienced the toxic consultant that would coach an organization on a methodology and, after however many years, they would leave and that organization hurt from it. My Superman slides represent that and it should make sense now. I've since seen this happen many more times, and now commonly with Agile methodologies. Organizations will hire external consultants to come in and coach Agile for two or three years, and then the coach leaves. The organization still won't know that Agile has 12 different disciplines that exist, and the organization will think they're "Agile" but it's really still waterfall.

The take aways that I wanted to share in my talk is that no matter the methodologies that come and go, it's still about the _people, process, tools_ that came from much earlier. DOD figured that out and they still know that today, but I see our civilian side losing sight of that overall mission. Focusing on what tool chains are going to rescue their organization. It's no wonder when I asked what CM was, people were responding with tool solutions and not knowing that it's the foundation of every organization with service deliveries. People have forgotten about people, and the processes that people create and follow for efficiency and repeatability.

Hopefully I've left you, Reader, with a burning passion to learn more about Configuration Management. It won't be going anywhere because it is so damned good in its design that all methodologies rely on it in order to succeed. DevOps tool chains implemented utilize each of its requirements from design planning to inventory to monitoring. And more importantly, you will see that none of this is originally any security team's responsibility. The focus was lost and most security teams had to make up for that when they be stakeholders, not owners.
