# jekyll-base

Answers to exercise questions for Netlify job interview

1) Rank your 5 favorite, and 5 least favorite, activities from this list:

First of all, this list is a perfect description of most of the tasks I do, or have done at my current job. And I like to doing most of them. But with that said, Here is a ranking of my 5 favorite activities:

Engage multiple users at once via chat to answer their questions and troubleshoot problems
Receive occasional phone calls requesting support from our highest-value customers
Deliver a talk to many people you don't know at a conference or meetup
Create video tutorials to help teach users a specific feature or use case
Help train and onboard new support teammates

And here are my least favorite activities (but I still like doing them :) )

Set up your own copy of several static site frameworks for debugging
Debug a customer's build using a programming language and framework that you've never seen before
Work with prospective customers to explain our service and the pricing model
Submit bug reports and potentially bug fixes to closed and open source projects that Netlify maintains on GitHub
Suggest and champion improvements to the Support team's workflow to your colleagues in and out of Support

2) What is your favorite thing about providing technical support?

The primary thing about providing support to customers for me is to first of all, listen to the customer's issue, ask questions that are pertinant, and then take steps to resolve the issue. As I am working thru the issue with the customer, I like to not only troubleshoot, but provide explanations of what steps I am taking, so that they can learn from the experience, and know what to do the next time a similar issue occurs. I like to see the lightbulb come on in their mind, and thus provide them with a memorable support experience. Hopefully, they will remember that experience, and this will help to build trust in the support relationship with Nelify moving forward. That way, it becomes a teachable moment as well as a successful resolution the the customer's issue.

3) What did you think of our service during the time you used it?  Provide either some constructive criticism or some points that impressed you.  Be honest!  “It sucked” isn’t a wrong answer unless you don’t elaborate and provide some constructive criticism ;)

I was actually quite impressed. I had never used an automatic site deployment service before (Call me Mr. Static!). I like how easy it was to setup an account, link it to my repository, then just a few clicks to specify my build settings, and I am up and running.

The only suggestion I would make is to add a simple "Getting started" video link for newbies that are using your service for the first time.

4) Talk about how you made your site and why you chose the tools you did.  Briefly explain a challenge you experienced in setting up this site and how you solved it.

I had some experience with using Ruby, so when I went on staticgen.com, I did a search on Ruby, and immediately chose Jekyll as my static generator. I was also happy to see that it was already directly usable on Nelify. So once I was on Netlify, I just clicked on "Connect to GitHub", I was given the the repository name, and then I immediately got my new site on Netlify. I clicked on the link to see what the initial site looked like. Verrry Cool!

I did want to see what another static generator that used Ruby to compare, so I went back to staticgen.com, and deployed a middleman, connected it to my repository as well, just to see what the differences were, and which one was best for me. I decided to stick with jekyll.

5) Provide a link to documentation for a technical/developer-focused product, which you think are well done, and briefly explain why you think they are well done.

Here is a link that I found that I think is very well done. It is webflow.com. I like it because it is a visual content management system, so even if you are not a strong coder, you can build and maintain a pretty nice web presence. Some of the features that they mention on their website, are that you can create the content structure you need, add content by hand, import it from a CSV, or via the API, and then design it visually. I think the reason that I like it is that I am a visual person, and think visually as well.

6) Why do you think SSL/HTTPS is important?

I think that if you are accessing web sites in this age of "web-anywhere" world, you need to protect yourself, your data, and your sites from hackers and their many methods of attack. HTTPS sites equipped with SSL is the only way to protect your data streams, and thus your data. SSL is needed so that all of your data is encrypted, especially in a wireless environment, where your data is moving through the air. This way, even if a hacker captures your data on the fly, the encryption will prevent the data from being usable.

7) Explain, in a couple of paragraphs, what you think 2 major challenges around DNS configuration are for less-technical internet end-users.

Let's look at this in the order that a customer will typically see as a DNS issue. I think the first challenge is "why am I getting a DNS Server not responding error". This is tough for less-technical users, as there are multiple points where this can happen; problems with your internet provider, malfuntioning TCP/IP or DHCP services, router connection issues, or even aggressive antivirus software. In order to troubleshoot this, you need to have a good understanding of the network connectivity between the client and the server, and all points in-between. And you need to know which commands or tools will help you to find the culprit.

The second challenge is having an understanding of which OS you are dealing with, and then understanding the proper syntax for commands, and the correct tools that are available for that OS. In these days of multiple OS's such MS Windows, MacOS, Linux, and others, it can be hard enough for a technical person to figure out, and almost impossible for a non-technical user.

8) A customer writes in saying their “site won’t build”.  Compose:
your best short (2-paragraph) customer-facing answer, 
without any additional data, 
that could be useful in the generic case, 
but would also lead to a customer providing a more actionable response.

Here would be my short customer-facing answer:

"I'm sorry Mr. customer that your website is not building. In order to help you resolve your issue, let me ask you a few questions first:
Has this site been working before, or is this a new site that you are testing?
Are you seeing the same problem on multiple types of browsers?
Does this just happen on one system, or are multiple systems or users seeing the same issue?"

Based on the answers to these basic questions, I would then be able to explain my suspicians of the cause, and then I could explain to to the customer what steps I would like to take to troublshoot this issue. Having a plan in mind, I would use a tool like webex, or similar to login to the customer's server or repository if it is still a site being tested.

Opt1) Can you set up a redirect from “/netlify/anything” to https://www.google.com/search?q=anything ?

I am assuming that you asking how to force particular folders to load in HTTPS mode. Is that correct?

Let me give this a shot: I would try redirecting to HTTPS on a /netlify/anything, by adding the following to the .htaccess file:

RewriteEngine On

RewriteCond %{SERVER_PORT} 80

RewriteCond %{REQUEST_URI} /netlify

RewriteRule ^(.*)$ https://www.google.com/netlify/$1 [R,L]

Opt2) Could you give us a suggestion to improve this test or the job posting?

It might be an interesting idea to make a second optional request asking the applicant to explain how they used github to place this answer sheet into their Netlify website for viewiing.
