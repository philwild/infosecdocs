#Welcome to the InfoSec app for Splunk!

The [InfoSec App for Splunk](https://splunkbase.splunk.com/app/4240/) is a free app for the Splunk platform which can be downloaded and installed into your Splunk environment. It is available from [Splunkbase](https://splunkbase.splunk.com/).

The InfoSec App for Splunk should not to be confused with [Enterprise Security](https://www.splunk.com/en_us/software/enterprise-security.html), Splunk's premium security solution. Although both solutions are security solutions, the features and capabilities of Enterprise Security are significantly deeper than what is available within the InfoSec app.

InfoSec app for Splunk is an entry, or starter level security solution powered by the Splunk platform. It is
designed to address the most common security use cases, including continuous monitoring and security investigations. The InfoSec app also includes a number of advanced threat detection use cases that can be further expanded using security resources available for Splunk like the [Security Essentials app for Splunk](https://splunkbase.splunk.com/app/3435/) from [Splunkbase](https://splunkbase.splunk.com). The Security Essentials app includes hundreds of additional security controls that can be easily integrated into the InfoSec app. Splunk's [Machine Learning Toolkit](https://splunkbase.splunk.com/app/2890/) can be used to enable advanced ML based correlation searches within the InfoSec app to detect and alert on threats.

The Splunkbase library has 1000+ apps and add-ons from Splunk, our partners, and our community. They can be directly downloaded, installed and configured within your Splunk environment. Splunk Apps provide solutions for many common use cases. They provide specialised insight into your data and systems with pre-configured dashboards, reports, data inputs, and saved searches which can supplement or be integrated with the InfoSec app.

Please visit [Splunkbase](https://splunkbase.splunk.com/) to see what is available.

Cyber Security is a journey, not a destination. The InfoSec app configuration steps and integrations with Security Essentials, the Common Information Model, and other Splunk apps and add-ons, are foundational steps towards the adoption of Splunk's Premium security platform, including [Enterprise Security](https://www.splunk.com/en_us/software/enterprise-security.html) and [Phantom](https://www.splunk.com/en_us/software/splunk-security-orchestration-and-automation.html).

##Product Goals

The InfoSec app for Splunk aims to achieve the following:

* Provide an entry level security solution to new and existing Splunk customers that are not yet ready or able to invest in Splunk's Enterprise Security platform.
* Make it easy to direct Splunk's powerful features towards security.
* Provide a single pane view of your security events and posture.
* Allow the user to easily investigate security alerts and incidents.
* Provide a base security platform that can be customised and expanded to meet your security needs using the additional apps and add-ons from Splunkbase.

##Before we start

This documentation is not designed to replace formal training or Splunk's own documentation. It focusses on the introductory steps and knowledge required to get the InfoSec app up and running in a short amount of time. It assumes the user is fairly new to Splunk and may not have yet grasped many of Splunk's fundamental concepts. Consider this documentation as a fast-start guide to getting the InfoSec app up and running within your environment. This documentation will introduce you to key Splunk concepts, lightly touching on each. Links will be provided to Splunk's documentation so you can delve further into Splunk's capabilities, as required. Although this document focuses on the InfoSec App for Splunk, the topics covered may be applied to other apps and configurations within Splunk.

##Introduction to the InfoSec app

![Security Posture](./Images/SecurityPosture.png)

The InfoSec app provides the user with a number of pre-configured and customisable security focussed dashboards and alerts. The InfoSec app focuses on the most common security focused technology components within your typical corporate environment, being:


* Firewall (including next-generation firewalls)
* Authentication (e.g. Active Directory and/or LDAP)
* Antivirus (including next-generation antivirus)

Focussing on these three security domains, the InfoSec app provides a comprehensive series of dashboards to help protect your network, users and intellectual property from external adversaries and malicious insider threats. It will help you investigate incidents and automate compliance tasks.

The InfoSec app also provides executive level reporting metrics, trends and summaries. The app can assist with meeting compliance requirements and completing audits faster through the use of customisable reports mapped to common compliance frameworks such as NIST HIPPA PCI and ISO.

A short introductory video is available [here](https://youtu.be/8Qx56cl24dw).

##Training

If you are new to Splunk or need to brush up on your Splunk skills, there are a number of free resources available to help you with your learning journey:

* Splunk [Fundamentals 1](https://www.splunk.com/en_us/training/free-courses/splunk-fundamentals-1.html)

  This is a free Splunk training cource. It will teach you how to search and navigate in Splunk, use fields, get statistics, create reports, dashboards, lookups, alerts, and more. Scenario-based examples and hands-on challenges will enable you to create robust searches, reports, and charts. It will also introduce you to Splunk's datasets features and Pivot interface. It is important to note that once registered, you have 28 days to complete this training. There is a cost associated with signing up for the course a second time.
  
* Splunk [Infrastructure Overview eLearning](https://www.splunk.com/en_us/training/free-courses/splunk-infastructure-overview.html)

  This self-paced course gives users an overview of the Splunk Enterprise infrastructure. Users get a high-level look at how to grow a Splunk deployment from a single instance to a distributed environment. With tips and best practices for deploying, extending and integrating Splunk while showing the user what is happening behind the scenes.
  
Splunk also provides formal training covering a number of learning paths. Information can be found on Splunk's [training website](https://www.splunk.com/en_us/training.html).

Splunk provides a [Quick Reference Guide](https://www.splunk.com/pdfs/solution-guides/splunk-quick-reference-guide.pdf) in PDF format that covers Splunk concepts and commands.

There's also a bunch of [how-to and other videos](https://www.splunk.com/en_us/resources/videos.html) available on the Splunk website to entertain and help you.

Splunk also maintains a [Youtube channel](https://www.youtube.com/user/splunkvideos) that you may want to subscribe to.