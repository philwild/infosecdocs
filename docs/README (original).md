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

##Concepts and Definitions

The InfoSec app relies on accelerated data models and the Common Information model (CIM) to provide a consistent and normalised view into the event data that you'll bring into Splunk. Understanding how to configure and use the CIM and data models may require an understanding of indexes, source types, sources, fields, event types, tags, macros and a few other concepts, depending on the data sources that you're feeding into Splunk.

Splunk provides a [Splexicon](https://docs.splunk.com/Splexicon), which is a glossary of technical terminology that is specific to Splunk software. Definitions within the Splexicon include links to related information in the Splunk documentation. It is a good place to start if you come across a Splunk word or term that you want to understand further.

A high-level overview of some of some of this terminology is provided below to assist with understanding how to configure, manage and troubleshoot the installation and ongoing use of the InfoSec app. If you are familiar with these Splunk concepts, skip to [Configuration](##configuration).

###Forwarder

A Forwarder is Splunk's data collection worker bee. It provides reliable, secure data collection from remote sources and forwards that data into your Splunk environment for indexing and consolidation. The forwarder can scale to tens of thousands of remote systems, collecting terabytes of data, if required. Splunk's Universal Forwarder is available for installation on diverse computing platforms and architectures. There are two forms of forwarder for the Splunk platform.

* Universal forwarder (UF) - A lightweight, dedicated, streamlined forwarder designed to efficiently send data to your Splunk environment. The Universal forwarder does not have a user interface and is typically managed by a [Deployment Server](##deployment-server).

  In most situations, the universal forwarder is the best way to forward data into Splunk.
  
* Heavy Forwarder (HF) - A more capable forwarder platform with the ability to integrate with additional APIs and services. A heavy forwarder is a full Splunk installation, configured to assume the role of just collecting and forwarding data. A heavy forwarder can route data to additional destinations, including non-splunk platforms. It can also parse/filter data within the pipeline and can index data locally, if required.

In most cases, data collection should be performed by the universal forwarder.

See [About forwarding and receiving](http://docs.splunk.com/Documentation/Forwarder/latest/Forwarder/Aboutforwardingandreceiving) in Splunk's documentation for further information.

You will most likely use a forwarder to collect and index data within Splunk to feed the InfoSec app. Understanding how a forwarder collects and forwards data is important in ensuring the data is correctly typed within your Splunk environment.


###Inputs Data Manager (IDM)

The Splunk Inputs Data Manager (IDM) is a Splunk managed Heavy Forwarder that is bundled with your Splunk Cloud subscription. It is provided to you to assist with onboard cloud-native data sources like AWS, Azure, GCP, Salesforce, and others. Using the IDM removes the need to pass these cloud-native API based data sources though a self-provisioned forwarder either on-premises or within a cloud tenancy. The IDM does not support all the inputs that a traditional Heavy Forwarder can. It will not support UDP or TCP inputs such as syslog. Installing Add-ons onto the IDM requires the creation of a support request.

For further information, please see [here](https://docs.splunk.com/Splexicon:IDM).

If you have plans to bring data sources such as Microsoft 365 into Splunk Cloud and the InfoSec app, you will want to use your IDM to collect this data.

###Deployment server

The Splunk Deployment Server is used to manage a fleet of forwarders within your environment. The deployment server acts as a centralised configuration manager, grouping and collectively managing any number of Splunk forwarder instances. Remotely managed forwarders under the control of the deployment server are called deployment clients. These clients poll the deployment server for new configurations and apps (deployment apps), downloading and enabling them as they become available.

Any full installation of Splunk can function as a deployment server although for larger deployments, it is recommended that a separate server perform this task (i.e. not one of your indexers or your search head(s)).

If you are using Splunk Cloud, you will still an on-premises deployment server to manage your forwarder fleet.

Further information can be found [here](https://docs.splunk.com/Splexicon:Deploymentserver).

Spending some time understanding how to configure and manage a deployment server will simplify the management of your deployers and simplify the process of onboarding data for use within the InfoSec and other Splunk apps.

If you are only ever going to onboard a small number of data sources (e.g. just Microsoft 365) then a deployment server might not be warranted.

### HTTP Event Collector (HEC)

The HTTP event collector is a Splunk service that can run on Splunk indexers or heavy forwarders. The http event collector can efficiently receive data over HTTP (or HTTPS) directly from applications or services.

Further information can be found [here](https://dev.splunk.com/enterprise/docs/devtools/httpeventcollector/).

You may need to configure HEC to collect certain data sources for use with the InfoSec app.

### Other Input Methods

There are many input methods available to assist with getting data in. This goes beyond the scope of this document and the InfoSec app. Splunk maintains very detailed documentation to assist with onboarding data. Please look at Splunk's documentation on [Getting Data In](https://docs.splunk.com/Documentation/SplunkCloud/latest/Admin/IntroGDI)

### Apps and Add-ons

Apps and Add-ons extend Splunk's out-of-the-box capabilities and enable a much faster time-to-value than other solutions as you are taking advantage of existing efforts to onboard and visualise data, or interface with third-party systems.

An App is a collection Splunk configurations designed to address a use-case with Splunk. The [InfoSec App for Splunk](https://splunkbase.splunk.com/app/4240/) is an example of a Splunk app. An app may contain combinations of dashboards, reports, alerts, knowledge objects, lookups, scripted inputs, menus and other components. Together, these components form a functioning application within the Splunk platform. In the same way that roles are given permissions to access and use knowledge objects, Splunk users can only access the apps (and the included knowledge objects) that they have been given permission to use. You can create your own apps in Splunk or download and install apps from [Splunkbase](https://splunkbase.splunk.com).

When browsing Splunkbase, you may notice that there are two types of apps and that the app contents can include Inputs, Alert Actions and Visualisations.

   <img src="./Images/Apps&Addons.png" width=50% height=50%>

All these are considered to be Splunk apps. An Add-on is just an app designed to provide additional capabilities to the Splunk platform, such as getting data in, or providing saved searches or macros. A Splunk app is a packaged-up directory of Splunk configuration files and any required supporting objects. The configurations might include dashboards and alerts, they may include javascript or something else that enables an additional visualisation type within Splunk, or code that enables communications with an external alerting framework or third-party application. Regardless of the content of the app, installation and configuration of the app in Splunk is usually handled in the same way.

####Installing Apps and Add-ons

Not all Apps and Add-ons are supported by Splunk. Most have been created by Splunk's partners and customers and the level of documentation and support will often vary. All apps and Add-ons will have some level of community support through [Splunk Answers](https://answers.splunk.com). The App or Add-on overview page on Splunkbase will show if the app is CIM compliant.

 <img src="./Images/CIMCompliant.png" width=30% height=30%>
 
 The overview page will also indicate where to go to get help and where to find support, if available.

**Splunk supported Add-ons**

Apps and Add-ons built by Splunk are usually Splunk supported. Documentation for Splunk supported Apps and Add-ons is usually contained within Splunk's documentation website. See the [documentation](https://docs.splunk.com/Documentation/AddOns) for the Splunk supported apps and add-ons.


###Knowledge Objects

A knowledge object is a user-defined entity that enriches the existing event data within Splunk. Knowledge objects include saved searches, event types, tags, field extractions, lookups, reports, alerts, data models and workflow actions. The term knowledge object refers to these objects within Splunk's language and documentation. Further information can be found [here](https://docs.splunk.com/Splexicon:Knowledgeobject).

Splunk's documentation will also refer to a knowledge manager, who is someone with administrative, or power user, privileges who can share and manage the permissions of knowledge objects. 
 
###Common Information Model (CIM)

The Splunk Common Information Model (CIM) is a shared semantic model focused on extracting value from data. The CIM is implemented as an add-on that contains a collection of data models (we'll get to what that means soon), documentation, and tools that support the consistent, normalised treatment of data for maximum efficiency at search time.

The InfoSec app relies on the CIM to function properly. If you have not yet installed the CIM to support the InfoSec app. Please look at the [Installation Instructions](#Installation).

Splunk Education has published a short video explaining the value and use of the CIM on YouTube [here](https://www.youtube.com/watch?v=QTklD7OiN74) (8:30 mins). The video also covers installation and configuration of the CIM.

The CIM add-on contains a collection of preconfigured data models that you can apply to your data at search time. Each data model in the CIM consists of a set of field names and tags that define the least common denominator of a domain of interest. You can use these data models to normalise and validate data at search time, accelerate key data in searches and dashboards, or create new reports and visualisations with Pivot.

The add-on also contains several tools that are intended to make analysis, validation, and alerting easier and more consistent. These tools include a custom command for CIM validation and a common action model, which is the common information model for custom alert actions. See [Approaches to using the CIM](https://docs.splunk.com/Documentation/CIM/latest/User/HowtouseCIM) for more information about the tools available in the CIM add-on.

For the InfoSec app to correctly report on the data that you have in Splunk, that data must be present within the supporting data models which means the data must be CIM compliant.

###Index

Splunk stores your data in indexes as events. The default index in Splunk is called "main". Splunk will store your event data in this main index if you don't tell Splunk to put it anywhere else. You can create and specify other indexes for different data inputs. There are several key reasons for having multiple indexes:

* To control user access.
* To accommodate varying retention policies.
* To speed searches in certain situations.

When configuring data models in Splunk, in most cases, you would restrict each data model to just the indexes that contain the data that populates the data model.

Further information on using, creating and managing indexes in Splunk can be found [here](https://docs.splunk.com/Documentation/Splunk/latest/Indexer/Setupmultipleindexes).

###Source type

A source type is used to name or identify each different type of data in Splunk. The definition of a source type will define how the timestamp is interpreted, what defines the break between different events and how Splunk might decipher and understand the structure of events. A source type could be considered the fingerprint or DNA of the event data entering Splunk. When configuring Splunk to receive or index data, you will always define a source type, or a source type may be pre-defined within an Add-on that you've chosen to use to help you onboard data into Splunk. As an example, the source types defined within the Splunk Add-on for Windows are listed within Splunk's documentation [here](https://docs.splunk.com/Documentation/WindowsAddOn/latest/User/SourcetypesandCIMdatamodelinfo).

Some source types may be structured, such as json, XML or CSV whereas others may have no structure.

This [blog post](https://www.splunk.com/en_us/blog/tips-and-tricks/sourcetypes-whats-in-name.html) provides a good introduction to source types with Splunk.

Splunk software ships with a set of built-in source types that are known as [pretrained source types](https://docs.splunk.com/Documentation/Splunk/latest/Data/Listofpretrainedsourcetypes).

###Source

A source in Splunk is not to be confused with source type. Where a source type identifies the structure of events or data within Splunk, the source identifies where that event data has come from. The source is the name of the file, stream or other input from which a particular event has come from. The below is an example of the difference between source and source type

`source=/var/log/messages and sourcetype=linux_syslog`

Every event in Splunk will have a pre-defined index, host, source, source type and _time field. For more information, see [default fields](https://docs.splunk.com/Splexicon:Defaultfield).

###Host

Within Splunk, all event data will be assigned to a host. The host identifies the network device that collected the data for Splunk. It may be a hostname or IP address. Further information can be found in the [Splunk documentation](https://docs.splunk.com/Documentation/Splunk/8.0.5/Data/Abouthosts). The host field is considered a [default fields](https://docs.splunk.com/Splexicon:Defaultfield).

###Field

Fields appear in event data as searchable name-value pairings such as `user_name=fred`. Fields are the building blocks of Splunk searches, reports and data models.

Splunk will attempt to auto-extract values into fields from within the event data that is being indexed. This is normally performed at search time.

Fields will often be defined within event data as key value pairs such as `user=fred` or `src:192.168.10.5` or may simply be a number or text within the structure of the event with no defined key. Splunk can still identify these fields using a custom [field extraction](https://docs.splunk.com/Splexicon:Fieldextraction) through Splunk web. A field extraction is defined against a source type, a source or a host.

Further information on fields in Splunk can be found [here](https://docs.splunk.com/Documentation/Splunk/latest/Knowledge/Aboutfields).

The values from fields within event data are used populate enabled data models within Splunk. 

Often, fields defined as key value pairs within event data may not align with the naming standard defined within the CIM and data models. In order to work with this event data, the names of these fields needs to be changed to conform with the CIM naming standard. This can be done using Aliases.

###Alias

An alias (or field alias) in Splunk is an alternate name assigned to a field that has been extracted from the event data within a Splunk index. Field aliases for fields can be defined against a source type, a source or a host. They can be defined within Splunk web by going into the Settings -> Fields menu. If you are working with a data source that is not yet CIM compliant, you may need to create field aliases to map existing fields within your data source to the [CIM naming convention](https://docs.splunk.com/Documentation/CIM/latest/User/CIMfields).

See Splunk's [documentation on Fields](https://docs.splunk.com/Documentation/Splunk/latest/Knowledge/Abouttagsandaliases) for further information.

###Event type

An event type in Splunk is a category of events united by the same search. Event types are useful for categorising a subset of event data from within one source type, or uniting events of a certain type across multiple source types. Event types and tags go hand-in-hand in assisting with preparing data for use in data models.

This is an older Splunk [video](https://www.youtube.com/watch?v=KhdMgT9VbHs) that covers the subject of event types.

See Splunk's [documentation on event types](https://docs.splunk.com/Documentation/Splunk/latest/Knowledge/Abouteventtypes) for further information.

###Tags

Tags enable you to assign names to specific field and value combinations. This includes event type, host, source and source type field value combinations. Tags tend to work hand-in-hand with event types.
An example of the use of tags might be to create an `authentication` tag that matches:

	eventtype=windows_successful_login
	eventtype=windows_failed_login
	eventtype=vpn_successful_login
	eventtype=vpn_failed_login
	
A search within Splunk for `tag = authentication` will return all events that match any of the above event types.

See Splunk's [documentation on tags](https://docs.splunk.com/Documentation/Splunk/latest/Knowledge/Abouttagsandaliases) for further information.

###Permissions, users and roles

Permissions within Splunk define who has access to data and knowledge objects. Roles within Splunk are given permission to access data within indexes and access apps and knowledge objects. Splunk users inherit the permissions granted to the roles that have been assigned to the user.

When first created within Splunk web, knowledge objects are private and only accessible to the user that created them. A Splunk knowledge manager can share these objects with other Splunk users by adjusting the permissions of the objects. Knowledge objects can be shared with individual roles, or everyone. Knowledge objects can also be restricted to be available within a single app, or globally.

Permissions for knowledge objects can be managed through the Settings menu within Splunk web. It is important to understand that permissions related to knowledge objects can impact data models. Fields and Tags that are private cannot feed a data model. Private data models cannot be accelerated, etc. Wen troubleshooting, checking the permissions on knowledge objects can often identify the cause of an issue.

Further information can be found in Spunk's [documentation](https://docs.splunk.com/Splexicon:Permissions).

###Macros

Search macros contain snippets of searches for re-use in other Splunk searches. A search macro is referenced in other searches through its name. You enclose the name of a search macro within the back-tick character to reference it in another search. As an example, you could create a search macro named `iis_logs` with the following definition:

    (index=windows OR index=dmz sourcetype=iis)

When searching for events within Splunk, you can reference the macro within your search

    `iis_logs` cs_username="fred"
    
Splunk will expand the macro when performing the search resulting the following search being run

    (index=windows OR index=dmz sourcetype=iis) cs_username="fred"

data models make use of search macros to define what data should be included within the data model.

Further information can be found in Splunk's [documentation](https://docs.splunk.com/Splexicon:Searchmacro).


###Data models and acceleration

A data model is a form of knowledge object that applies structure to the event data within Splunk. each data model within Splunk represents a category of event data (e.g. authentication data). Data models are powered by root searches that define what data is represented and available within the data model. The data model overlays a schema onto the event data identified by the base search and presents the data to the user as columns of fields over rows of data. Splunk's pivot and datasets interface can be used to query data models to build visualisations and reports.

The schema that is applied to the event data in the form of a data model can be accelerated in Splunk. This is called an accelerated data model. Accelerated data models power apps such as Enterprise Security and the InfoSec app. A data model that has been accelerated cannot be edited. If you need to edit an accelerated data model, you must disable acceleration.

Splunk accelerates data models by running regular scheduled searches (every 5 minutes) across the underlying event data, building data summaries behind the scene with the help of Splunk's high performance analytics store functionality.

Data models can only be accelerated if they are shared and not private.

Further information can be found in Splunk's [documentation](https://docs.splunk.com/.Splexicon:Datamodel).

###Configuration Files

All configuration settings within Splunk are stored within configuration files that can be manually edited. Interacting and managing Splunk through the Splunk web interface simplifies the management of the underlying configuration files. If you are using Splunk Cloud, you actually don't have access to the underlying configurations files within Splunk and must perform all management tasks through Splunk web.

Whether you are using Splunk Cloud or Splunk Enterprise, there will still be times where you will need to modify a configuration file to perform some task within Splunk. Modifying configuration files is most often associated with [getting data in](https://docs.splunk.com/Documentation/SplunkCloud/8.0.2007/Admin/IntroGDI).

Splunk configuration files are stored within the `etc` directory within the Splunk installation directory. Under Linux, this defaults to `/opt/splunk`. Under Windows, this defaults to `C:\Program Files\Splunk`. Modifying configuration files within the Splunk directory often requires the Splunk service to be restarted so that Splunk adopts the changes that you have made.

Splunk configuration files are disbursed within the `etc` directory structure. Configuration files could be private to the user, or located within an installed or deployed app. 

Splunk applies an [order of precedence](https://docs.splunk.com/Documentation/Splunk/latest/Admin/Wheretofindtheconfigurationfiles) to configuration files to allow `default` configurations to be overridden by `local` configurations. It is Splunk best-practice to never modify a `default` configuration. A Splunk administrator should always copy the settings into a `local` copy of the configuration file.

Further information can be found [here](https://docs.splunk.com/Splexicon:Configurationfile#:~:text=A%20file%20(also%20referred%20to,SPLUNK_HOME%2Fetc%2Fsystem%2Fdefault).

###The data pipeline

The Splunk data pipeline describes the route that data takes moving from its original source to its transformation into searchable events that encapsulate valuable knowledge. The data pipeline includes these segments:

* [Input](https://docs.splunk.com/Splexicon:Input)
* [Parsing](https://docs.splunk.com/Splexicon:Parsing)
* [Indexing](https://docs.splunk.com/Splexicon:Index)
* [Search](https://docs.splunk.com/Splexicon:Search)

![Splunk Data Pipeline](https://docs.splunk.com/images/5/5e/Datapipeline1_60.png)

###Alerts

Alerts in Splunk are used to monitor and respond to specific events that are detected by a saved search that is run at a scheduled time. An alert will initiate one or more alert actions when the alert triggers.

The InfoSec app utilises alerts to detect and report on notable events within your data. Understanding how to add, configure and manage alerts is an important skill when it comes to adding additional controls and use-cases to your environment.

![](./Images/ManageAlerts.png)

Further information on working with Alerts can be found in Splunk's [documentation](https://docs.splunk.com/Documentation/Splunk/latest/Alert/Aboutalerts).

## Installation

###Installation Prerequisites

The InfoSec app for Splunk can be installed directly into Splunk in the same way as other available apps from [Splunkbase](https://splunkbase.splunk.com/). Installing the app and pre-requisites should take less than 15 minutes.

It's assumed that you already have Splunk installed somewhere, or you're using Splunk Cloud. This document does not cover installing and configuring Splunk for the first time. If you need to do this before proceeding further, please view the following resources:

* [Installing Splunk on Linux documentation](https://docs.splunk.com/Documentation/Splunk/latest/Installation/InstallonLinux). There's also a video [here](https://www.splunk.com/en_us/training/videos/installing-splunk-enterprise-on-linux.html).

* [Installing Splunk on Windows documentation](https://docs.splunk.com/Documentation/Splunk/latest/Installation/InstallonWindows). There's also a video [here](https://www.splunk.com/en_us/resources/videos/installing-splunk-on-windows.html).

* [Start Splunk Enterprise for the first time](https://docs.splunk.com/Documentation/Splunk/latest/Installation/StartSplunkforthefirsttime)

* [Installing the Splunk Enterprise License](https://docs.splunk.com/Documentation/Splunk/latest/Installation/Installalicense)

* [A short introductory video to using the Splunk web interface](https://www.splunk.com/en_us/resources/videos/splunk-web-demo.html)

###Installation Steps

The method for installing the InfoSec app will vary slightly between Splunk Enterprise and Splunk Cloud. If there is a difference within the steps. Each will be explained.

1. Log into your Splunk environment with an account that has administrative privileges.

	If you are a Splunk Cloud customer and are new to using Splunk Cloud. Splunk will have supplied you with two instances:
	
    * `https://<stackname>.splunkcloud.com` - This instance is your primary Splunk environment and is where you should install the InfoSec app. Log into this instance to perform the installation.
        
    * `https://idm-<stackname>.splunkcloud.com` - This is an 'Inputs Data Manager (IDM)'. It is a heavy forwarder that Splunk provides to assist with the collection of event data from cloud-based services like AWS, Azure, etc. If you're going to bring in Microsoft365, AWS or other cloud service data sources into your Splunk environment, you'll need to install technology Add-ons onto the IDM through a support request. The InfoSec app should not be installed onto the IDM.	

2. From within the Splunk web interface, select the App menu within the black menu bar at the top left of the user interface (just to the right of the Splunk logo). 

   <img src="./Images/AppMenu.png" width=50% height=50%>

3. Select Find More Apps

   <img src="./Images/FindMoreApps.png" width=50% height=50%>
  

4. Within the search menu on the top-left of the page, search for `infosec app for splunk`. The InfoSec App for Splunk should be listed as one of the available apps for installation.

   <img src="./Images/Search&Install.png" width=100% height=100%>
   
   **Splunk Cloud**

   Within Splunk Cloud, the InfoSec app cannot be self-installed and requires a support request to be raised through Splunk's [Support Portal](https://splunkcommunities.force.com). Request that the app is installed on the Search Head. 
   
   One of the supporting apps (The Common Information Model CIM app) also needs to be installed through a support request. Log the installation of this app within the same request.

   **Splunk Enterprise**
   
   5. Press the green `Install` button for the InfoSec App for Splunk. The process will be slightly different between Splunk Cloud and Splunk Enterprise.

   Within the presented dialog box, login with your splunk.com credentials to install the app. The required credentials are what you would use to login to the support portal on the splunk.com website or Splunkbase and is not your Splunk Enterprise instance account login (e.g. administrator, or whatever you have created or been assigned). If you have not yet setup a splunk.com account, you can do so [here](https://www.splunk.com/page/sign_up).
   
   You will also need to accept the Terms and Conditions by checking the box before being able to proceed.
      
   <img src="./Images/Login&Install.png" width=50% height=50%>
   
   Note: The ability to install Apps and Add-ons directly into your Splunk environment requires internet connectivity. Your Splunk environment must be able to access https://splunkbase.splunk.com over port TCP/443. If searching for additional apps like the InfoSec app is not producing any results, you may have a problem with Internet connectivity. If the only method of gaining access is through a proxy server, then this must be configured. Instructions on how to configure Splunk to use your HTTP Proxy Server can be found [here](https://docs.splunk.com/Documentation/Splunk/latest/Admin/ConfigureSplunkforproxy).
    
   If configuring Internet access for your Splunk environment is not possible, you can still install apps manually via a two-step process. You will first need to download the apps from [Splunkbase](https://splunkbase.splunk.com) to your desktop. Next, you will need to install the apps into your Splunk environment via "[Install app from file](https://community.splunk.com/t5/Archive/How-to-install-a-splunk-app/m-p/87912)". This app installation method is not applicable for Splunk Cloud.

   If you have a larger distributed Splunk Enterprise environment, you only need to install the InfoSec app on the search head. It does not need to be installed on the indexers. If your Splunk environment also includes search head clusters, you'll need to use the `Deployer` to push the app out to all the cluster peers. See the documentation [here](https://docs.splunk.com/Documentation/Splunk/latest/DistSearch/PropagateSHCconfigurationchanges). 
   
The InfoSec app for Splunk should now be installed. To confirm this, select the InfoSec app from the App menu (see step 2, above). You should be presented with the `Security Posture` dashboard. At this point, you can ignore any errors you might see on the InfoSec dashboard as there are still a couple of steps needed to complete the installation and configuration.


###Additional Apps and Add-ons

A number of supporting Splunk Apps and Add-ons from Splunkbase must also be installed before you can start using the InfoSec app. These are:

* [Splunk Common Information Model (CIM)](https://splunkbase.splunk.com/app/1621/)
* [Punchcard visualisation](https://splunkbase.splunk.com/app/3129/)
* [Force Directed visualisation](https://splunkbase.splunk.com/app/3767/)
* [Lookup File Editor](https://splunkbase.splunk.com/app/1724/) (new requirement starting from InfoSec v1.5)
* [Sankey Diagram visualisation](https://splunkbase.splunk.com/app/3112/) (new optional prerequisite for the experimental VPN Access dashboard starting from v1.5.3)

Although not essential, the following three Apps and Add-ons should also be installed.

* [Splunk Security Essentials](https://splunkbase.splunk.com/app/3593/)

  The Splunk Security Essentials App includes hundreds of additional security searches that can be integrated into the InfoSec App. The Splunk Security Essentials App also includes comprehensive guided data onboarding examples that can help identify the right data sources to enable the security controls and assisting with the configuration of the underlying data source.
  
* [Alert Manager Add-on](https://splunkbase.splunk.com/app/3365/)
* [Alert Manager App](https://splunkbase.splunk.com/app/2665/)

  The third-party Alert Manager app and add-on provides an incident management capability with simple workflows to support the management of triggered alerts from within the InfoSec app. Installation and configuration instructions are available [here](http://docs.alertmanager.info/).

   
####Splunk Cloud

With the exception of the Splunk Common Information Model app, all these additional apps can be self-installed within Splunk Cloud. Search for these apps in the same way that you searched for the InfoSec app, following the instructions above. Select the green `Install` button for each app.

####Splunk Enterprise
   
The process to install these additional Apps and Add-ons is the same as you've just completed when installing the InfoSec app. Repeat the above steps to install each of these additional Apps and Add-ons.

Once you've reached this step, you are ready to start configuring the InfoSec App for Splunk.


## Data Sources   

For the InfoSec app to function correctly, at a minimum, you should have data from the following security sources collected by your Splunk environment:

* Firewall, IDS/IPS data (e.g. Cisco, Palo Alto Networks, Check Point, Fortinet, Juniper)

* Authentication data (e.g. Active Directory data from the Windows logs on Domain Controllers or Microsoft365) With Microsoft Active Directory, the correct audit policy will need to be set to ensure the logging of the right event data.

* Malware/antivirus tools data (e.g. Symantec, McAfee, Sophos, Trend Micro)

All data used by InfoSec app must be Common Information Model (CIM)-compliant. The easiest way to accomplish that is to use CIM-compliant Splunk Add-ons for your security devices.

###Onboarding Data Sources

Correctly onboarding data into Splunk can be daunting at first. Trying to cover every combination of data source for the InfoSec app is beyond the scope of this documentation.

If you installed the Splunk Security Essentials app when following the [Installation steps](#installation), you'll have access to detailed guided onboarding instructions for many security data sources. As an example, to obtain the instructions to onboard Windows Authentication events, f

1. Open the `Splunk Security Essentials` app

  ![](./Images/SecurityEssentials.png)

2. Navigate to the Data `Source Onboarding Guides`

  ![Onboarding Guide](./Images/DataSourceOnboardingGuide.png)
  
3. Select Authentication

  ![Windows Authentication](./Images/AuthenticationDataSource.png)
  
4. Select Windows Security Logs

  ![Windows Security Logs](./Images/WindowsSecurityLogs.png)
  
5. Follow the presented guided procedure

  ![](./Images/WindowsOnboarding.png)


##Configuration

After performing the installation steps documented above, start by confirming the Health of the InfoSec app within your environment. 

1. Navigate to the InfoSec app by selecting the `InfoSec` app from the App menu at the top of the Splunk web interface.

	![InfoSec app](./Images/ConfigurationInfoSec.png)
	
2. Select the `Health` dashboard from within the InfoSec app.

	![Health dashboard](./Images/ConfigurationHealth.png)

The first two rows of visuals within the Health dashboard will give you an indication of the data within your Splunk environment.

There are three metrics on this dashboard that need to be verified:

1. The count of events feeding each of the data models required for the InfoSec app.

	![Data Model Data](./Images/ConfigurationDataModelsData.png)
	
	In the above example, there is no data feeding the CIM_Authentication, or any of the other data models. Don't be concerned if some of the data models in your environment have no data. Within your Splunk environment you may not have a data source to feed some of these data models. Follow the steps in [Validating Data Sources](#validating-data-sources) to confirm your environment is correctly configured for each of these data models.

2. The Acceleration Status for each of the required InfoSec data models.

	![Data Model Data](./Images/ConfigurationDataModelAcceleration.png)
	
	In the above example, the Health dashboard is reporting that there are no accelerated data models. You should only enable acceleration for the data models that are being fed with data. Follow the steps in [Accelerating Data Models](#accelerate-data-models) to confirm your environment is correctly configured.
	
3. The Installation status for each of the required supporting Apps/Add-ons for InfoSec.

	![Installed Add-ons](./Images/ConfigurationInstalledAdd-ons.png)
	
	In the above example, the Health dashboard is reporting that all the required Add-ons are installed. If you had correctly followed the Installation Instructions above, your Health dashboard should also be reporting that all Add-ons are installed. If this is not the case, follow the steps in [Additional Apps and Add-on](#additional-apps-and-add-ons) to confirm your environment is correctly configured.

###Validating Data Sources

You will need to confirm the data sources for each of the InfoSec data models listed on the Health dashboard. In the example above, the authentication data model is receiving no event data. We'll walk through the steps to validate the configuration of the `Authentication` data model. The same process can be applied to all the data models.

It would pay to validate the data sources for each of the data models, even if the Health dashboard is reporting that data is being fed into the data model. Within your environment, you may find that only some of the data you were expecting within the data model is being fed into it and you may want, or need, to adjust the configuration to ensure full coverage of your environment.

Repeat this process for each data model.

1. Select `Data models` from the `Settings` menu.

	![Settings -> Data models](./Images/SettingsDataModels.png)

2. Find the `Authentication` data model within the list of presented data models and select it. You can use the filters at the top of the page to assist, if required.

	![Settings -> data models -> Authentication](./Images/SettingsDataModelsAuthentication.png)
	
3. You will now be presented with the Authentication data model configuration. It should look similar to the screenshot below.

	![Data model -> Authentication](./Images/DataModelAuthenticationSearch.png) 
	
	At the top of the data model configuration page is a section labelled `CONSTRAINTS`. This contains the Splunk search that identifies the events that should feed the Authentication data model. Your search should look something like this:
	
	``(`cim_Authentication_indexes`) tag=authentication NOT (action=success user=*$)``
	
	The first part of the search contains a macro called `cim_Authentication_indexes`. We know it is a macro because it is enclosed within backticks. This macro is most likely constraining the search to certain indexes.
	
	The next part of the search (`tag=authentication`) is constraining the search to only return events that have been tagged as authentication events.
	
	The last part of the search (`NOT (action=success user=*$)`) is excluding any event containing a field labelled `action` with a value of `success` AND a field `user` that has a value that ends with the `$` character. We can ignore this last part of the search for the moment as it is reducing (NOT) the returned results
	
	We want to find out which data sources we have in Splunk that might fit this search.
	
4. Open a new Splunk search window in another tab of your browser. The quickest way to do this is to right-click on `Search & Reporting` from the `App` menu at the top of the Splunk web interface and select `Open Link in New Tab`.

	![Authentication Open New Search](./Images/AuthenticationOpenNewSearch.png)

	Before pivoting to the new browser tab, highlight and copy the:
	
	 ``(`cim_Authentication_indexes`) tag=authentication NOT (action=success user=*$)`` 
	 
	 search so that we can paste it into the search tab we've just opened. Execute the search in the new tab. In this example, no results are returned. Within your Splunk environment, you may have some data returned.
	 
	 ![Authentication Search 1](./Images/AuthenticationSearch1.png)
	 
	 We're now going to investigate why no results were returned and identify what we need to do to adjust the configuration.
	 
5. The next step is to modify the search to include ALL indexes within your Splunk environment. Replace the macro component of the search with `index=*` and include a statistical count by index and source type at the end of the search by adding `|stats count by index, sourcetype`. In this example, the search will now look like this:

	 ``index=* tag=authentication NOT (action=success user=*$) | stats count by index, sourcetype``
	 
	 Execute the search to see if any results are returned.
	 
	 ![Authentication Search 2](./Images/AuthenticationSearch2.png)
	 
	 In this example, we can see a number of source types returned across two indexes named `demo_oracle` and `demo_wineventlog`. This indicates that we do have correctly tagged events in two indexes within our Splunk environment, but our original search macro, defined as `cim_Authentication_indexes` was not including these indexes within its definition.
	 
	 When you perform this search in your environment you will see different results than this example. If no results were returned, then the data in your environment may not be tagged correctly or may not be CIM compliant. You may need to investigate why by searching the event data. In this example, troubleshooting further would require investigating why `tag=authentication` is not matching any events. This will involve examining the data sources that you believe should contain authentication events.
	 
	 Watch this Splunk Education [video](https://www.youtube.com/watch?v=QTklD7OiN74) on the Splunk Common Information Model. If this doesn't help guide you towards solving the problem, try requesting [help](#support) from the Splunk Community.
	 
	 If your search results returned indexes and data sources, we can proceed with modifying the search macro for this data model.
	 
6. Take note of the name of the indexes returned by the above search as the next step we perform will be to update the macro. In our example, we have two indexes `demo_oracle` and `demo_wineventlog`.

7. Open the `Advanced Search` under the `Settings` menu.

	![Settings -> Advanced Search](./Images/SettingsAdvancedSearch.png)
	
8. Open `Search Macros`

	![Settings -> Search Macros](./Images/SettingsSearchMacros.png)
	
9. Search for the `cim_Authentication_indexes` macro. You will probably need to adjust the filter to find the macro. Set the App context to `All` and type in `cim_authentication_indexes` into the search filter.

	![CIM Authentication Indexes Macro 1](./Images/CIMAuthenticationIndexesMacro1.png)
	
	In this example, we can see the definition is set to `(index=main)`. This is the reason why the Authentication data model was not being fed with data as main contained no events constrained by the original search that included `tag=authentication`. 

10. Click on the macro name to open it for editing.

	![CIM Authentication Indexes Macro 2](./Images/CIMAuthenticationIndexesMacro2.png)
	
	You should be presented with the CIM Setup window for the `Authentication` data model.
	
	![CIM Authentication Indexes Macro 3](./Images/CIMAuthenticationIndexesMacro3.png)
	
	Change the `Indexes whitelist` to include the indexes identified in step 6, above. This terminology may change in a future version to `Indexes Allowlist`.
	
11. Save the change by selecting the Green `Save` button.

12. Verify that the change is successful by re-running the original data model search. In this example, the search was:

	``(`cim_Authentication_indexes`) tag=authentication NOT (action=success user=*$)``
		
	The search should now return events. Your search will be different from the above, depending on the data model you are working with.
	
Repeat this process for all the InfoSec data models:

* Authentication
* Change (for app version 1.6.x and newer) or Change Analysis (for app version 1.5.3 and older)
* Intrusion_Detection
* Malware
* Network_Sessions
* Network_Traffic
* Endpoint
* Web

In order to aid with configuration, the default constraining search and search macro for each of the required data models is listed in the table below. You will notice that for each data model, there is no search macro defined (e.g. `()`). If this is not changed, then the data model is relying on your data residing in indexes searched by default.

| Data model | Base search/CONSTRAINT | Search Macro |
| ---------- | ---------------------- | ------------ |
| Authentication | (\`cim\_Authentication\_indexes\`) tag=authentication NOT (action=success user=*$)` | () |
| Change | (\`cim\_Change\_indexes\`) tag=change NOT (object_category=file OR object_category=directory OR object_category=registry) | () |
| Intrusion Detection | (\`cim\_Intrusion\_Detection\_indexes\`) tag=ids tag=attack | () |
| Malware | (\`cim\_Malware\_indexes\`) tag=malware tag=attack | () |
| Network Sessions | (\`cim\_Network\_Sessions_indexes\`) tag=network tag=session | () |
| Network Traffic | (\`cim\_Network\_Traffic\_indexes\`) tag=network tag=communicate | () |
| Endpoint | (\`cim\_Endpoint\_indexes\`) tag=listening tag=port \| eval transport=if(isnull(transport) OR transport="","unknown",transport),dest\_port=if(isnull(dest\_port) OR dest\_port="",0,dest_port),transport\_dest\_port=mvzip(transport,dest\_port,"/") \| mvexpand transport\_dest\_port | () |
| Web | (\`cim_Web\_indexes\`) tag=web | () |



###Accelerate data Models

Each of the InfoSec data models will need to be accelerated. Only accelerate the data models after you have confirmed that they are being correctly fed with the right event data as once accelerated, the data models cannot be edited without first disabling the acceleration. Perform the following procedure on all the InfoSec data models that are being fed data.

There is no value in accelerating a data model that contains no event data.

In this example, we'll accelerate the `Authentication` data model.

1. Select `Data models` from the `Settings` menu.

	![Settings -> Data models](./Images/SettingsDataModels.png)

2. Find the `Authentication` data model within the list of presented data models and select it. You can use the filters at the top of the page to assist in finding the model, if required.

	From the `Actions` column, select `Edit Acceleration`.

	![Settings -> data models -> Authentication](./Images/DataModelAccelerationEdit.png)

3. Within the `Edit Acceleration` dialog box, check `Accelerate`. Set the Summary Range to a suitable timeframe and `Save`.
	
	![Settings -> data models -> Authentication](./Images/DataModelAccelerationSave.png)

Splunk will start building the data model accelerations. You can track the progress of the accelerations from within the `Health` dashboard of the InfoSec app.

The InfoSec app should now be configured to work with your data sources.

As a final step, view each of the InfoSec dashboards starting with `Security Posture` from the InfoSec app menu and confirm all dashboards are being populated with data. If you come across a dashboard that is not being populated, please see the [Troubleshooting](#troubleshooting) section to identify if this can be resolved. It may just be that you do not have the required data source within Splunk to feed the dashboard. 


##Using the InfoSec app

###Security Posture

![Security Posture](./Images/SecurityPosture.png)

As the title suggests, the Security Posture dashboard provides a high-level view of your security posture. At the top of the dashboard there are two rows of indicators. The top-most row displays statistical counts of events covering your Intrusion Detection System (IDS), Antivirus and Malware systems. Each indicator shows the current state, with an arrow identifying the rate of change (positive, neutral, or negative) and the previously recorded statistic from 24 hours ago.

The second row of indicators displays the number of detected hosts and devices, along with the number of detected accounts being monitored. Each indicator also includes the 24-hour trend and previous result for comparative purposes.

Clicking on any of these indicators will open a new dashboard with more detailed information.

Together, these two rows of indicators give you an immediate view of the state of your environment compared to how it looked yesterday.

The next row includes three dashboards that focus on Intrusion alerts, splitting and breaking down the reporting into a statistical count of the total "Alerts by Severity", a 24-hour view of those alerts over time, and the Top-10 most critical alerts charted over the same 24 hour window.

Clicking on any of these dashboards will open a new window that focuses on your IDS.

The last row contains two punchcard style dashboards that focus on account and asset information within your organisation. For these dashboards to populate, the punchcard visualisation has to have been installed and enabled within your Splunk instance. If you do not see the punchcard visualisation matching the above screenshot, it may indicate that this visualisation has not been installed or may have been disabled. You may see the message "No matching visualization found for type: punchcard, in app: punchcard_app". Installing this app will be discussed [later](# Supporting apps and add-ons).

These two dashboards provide a swim-lane style view of the type and count of events being detected against your identities and assets over the past 24 hours. These two dashboards allow you to quickly identify bursts of activity that may need investigating.

###Continuous Monitoring

####Windows Access and Changes

![Windows Access and Changes](./Images/WindowsAccessAndChanges.png)
	
The `Windows Access and Changes` dashboard focuses on events within your Microsoft Windows environment. It presents information relating to:
	
 * Locked Out Accounts
 * Privilege Escalations
 * Change metrics
 * Authentication metrics

By default, this and other dashboards within the InfoSec app default the search time period to `Last 24 hours`. You can access and modify the search filters associated with these dashboards by selecting `Show Filters` near the title of each dashboard (see below).

![Show Filters](./Images/ShowFilters.png)
     
####All Authentications

![All Authentications](./Images/AllAuthentications.png)
	
The `All Authentications` dashboard provides a consolidated view of authentication actions across all data sources. This dashboard will assist in identifying authentication anomalies within your environment or problem accounts repeatedly failing to login.
	
The second part of the dashboard provides an interactive filter allowing you to filter by `User`, `Host`, `Action` and a frequency criteria (e.g. `Authenticating against 5 or more hosts`.
	
Selecting an identity or host/asset will take you to either the `User Investigation` or `Host Investigation` dashboards.
	
####Malware

![Malware](./Images/Malware.png)

The `Malware` dashboard provides a consolidated view of your antivirus solutions over the last 24 hours.

The first row of the dashboard displays the count of `Unresolved`, `Deferred` and `Blocked` infections. These metrics a derived from the `action` field of the `Malware` data model. Clicking on an action will constrain the results for rest of the dashboards to the selected action.

Selecting a destination will take you to the `Host Investigation` dashboard. Selecting anything else within the presented dashboards will display the underlying results within a Splunk search window.
	
####Intrusion Detection (IDS/IPS)

![Intrusion Detection](./Images/IntrusionDetection.png)

The `Intrusion Detection (IDS/IPS)` dashboard provides a consolidated view across all IDS/IPS systems within your environment. This data would typically come from your NG Firewall solutions and dedicated IPS solutions like Snort, Suricata, Darktrace, etc.

The first row provides a breakdown of the total events by action over the last 24 hours. Clicking on an action will constrain the results in the other dashboards to the selected action.

The second row provides a breakdown of the total events by severity. Clicking on an severity will also constrain the results presented in the other dashboards to the selected severity.

Clicking on any of the displayed data will pivot to the results in a Splunk search window.
	
####Firewalls

![Firewalls](./Images/Firewalls.png)

The `Firewalls` dashboard provides a high-level consolidated view of all firewall events within your organisation.

The first row displays a breakdown by action (Blocked and Allowed) as well as total counts for source and destination IP's. Only the `action` values are selectable, which will constrain the other dashboards to the selected action.

The displayed results are geo-tagged to country.

Clicking on any of the presented results will pivot to displaying the results in an underlying Splunk search.
	
####Network Traffic

![Network Traffic](./Images/Networktraffic.png)

The `Network Traffic` dashboard will display your firewall data in more detail. Clicking on any source or destination will pivot to the `Host Investigation` dashboard.

The second half of the dashboard allows you to filter and investigate the firewall detailed results through a series of filters.

A communications map will display the relationship of the filtered results.
	
####VPN Access
	
![VPN Access](./Images/VPN.png)

The `VPN` dashboard will present VPN session data from all monitored data sources.

Included within the dashboard is a list of geographically improbably VPN connections.

The VPN data can be filtered by user and selecting any of the presented results will pivot to displaying the results in Splunk search.
	
###Advanced Threats

The `Advanced Threat` dashboards applies the power of Splunk's search capabilities to highlight security events of interest. Searches 

####Access Anomalies

![Access Anomalies](./Images/AccessAnomalies.png)

The `Access Anomalies` dashboard identifies events that could potentially pose a security risk. Searches look to identify:

* Spikes or out of character increases in access to hosts
* Brute force attacks by source or user
* Accounts that have high percentage of logon failures vs success
* Users performing new privileged actions
* Geographically improbably access 
	
####Network Anomalies

![Network Anomalies](./Images/NetworkAnomalies.png)

The `Network Anomalies` dashboard identifies:

* Spikes in access to destinations
* Suspected network scanning
* BOT/C2 network indicators
* SMB and DNS anomalies
	
####Custom Use Cases

![Custom Use Cases](./Images/CustomUseCases.png)

The `Custom Use Cases` dashboard starts as a blank canvas for you to incorporate your own searches and dashboards. You can incorporate searches from the [Splunk Security Essentials](https://splunkbase.splunk.com/app/3435/) app into this dashboard. You can follow the example of [adding a custom search](###adding-a-custom-search)
	
###Investigation

The `User Investigation` and `Host Investigation` dashboards provide an interface to investigate user and host-based behaviours and actions. Entry to these dashboards will normally occur through a drilldown from one of the other dashboards within the InfoSec app but you can navigate to the dashboards directly and search using the provided filters.

Selecting any represented data within these two dashboards will either drill-down to that user or host, or display the results of the underlying Splunk search.

####User Investigation

![User Investigation](./Images/UserInvestigation.png)
	
####Host Investigation

![Host Investigation](./Images/HostInvestigation.png)
	
###Compliance

![Compliance](./Images/Compliance.png)

The `Compliance` dashboard provides visibility into controls that are often required under different compliance frameworks. This dashboard can be edited and changed to meet your needs. If you perform regular audits, you may want to add to this dashboard the searches that you use to respond to the audits.

###Executive View

![Executive View](./Images/ExecutiveView.png)

The executive view dashboard provides a high-level view of certain security metrics, reporting on the status of the environment.

###Alerts

![Alerts](./Images/Alerts.png)

The `Alerts` dashboard allows you to investigate and manage alerts raised by the InfoSec app.

Alerts are regularly running scheduled searches that are looking for matching events within your data. You can drill-down to the current alerts defined within the InfoSec app and modify or add to them through this dashboard.

Any search that you create within Splunk can be saved as an alert. All alerts need to include a search schedule. When creating an alert, Splunk offers you a selection of times that a search can run. Selecting the cron schedule allows you to set the scheduled frequency as often as every minute. 

Although there is an option to schedule real-time searches, this should normally be avoided.

This [video](https://youtu.be/0REbozaALX0) covers the steps required to create a new alert.

You may want to consider using the [Alert Manager](https://splunkbase.splunk.com/app/2665/) app in conjunction with the InfoSec app to provide a more feature rich alert management framework.

###Health

![Health](./Images/Health.png)

The `Health` dashboard provides a health-check view of your Splunk environment as it relates to the requirements of the InfoSec app. The dashboard can provide an indication of any issues that may impact the proper functioning of the InfoSec app. It will identify the source and type of data being indexed by your Splunk environment. It will show you which data models are being fed with data and show you the status of each of the required data models.

###Search

####Search

![Search](./Images/Search.png)

The InfoSec app provides a standard Splunk search page from within the App. If you're unfamiliar with how to search in Splunk, this [introductory video](https://www.splunk.com/en_us/resources/videos/search-filter-and-correlate.html) may help.

Please also see [Training](#Training).
	
####Dashboards

![](./Images/Dashboards.png)

The `Dashboards` page will list all saved dashboards within Splunk. From here, you can:

* Open and view a dashboard
* Adjust who can access a dashboard by modifying it's permissions
* Edit a dashboard
* Clone a dashboard
	
####Lookups

![Lookups](./Images/Lookups.png)

The InfoSec app comes bundled with a number of lookups that are used to enrich the event data within your environment. There are two lookups that can be modified to provide additional context when viewing certain data within the InfoSec app. These lookups are:

* Host

The host lookup allows you to manually enter context associated with your organisation's assets. You can record fields such as location, description, owner, priority, make and model. The information in this lookup table is mapped to events within Splunk through the IP address of the host.

Although you can configure this lookup manually through the InfoSec app, at some point you may want to write a search that regularly populates this lookup from Active Directory and/or other sources.

Modifying the lookups within InfoSec app is only possible if you have installed the [Lookup File Editor](https://splunkbase.splunk.com/app/1724) app.

* User

Similar to the `Host` lookup, the `User` lookup enriches the user event data within your Splunk environment with additional information that can assist you, or your security analysts with triaging and actioning invents under investigation. It allows you to record fields such as full-name, phone number, email address, priority, among others.

Although you can configure this lookup manually through the InfoSec app, at some point you may want to write a search that regularly populates this lookup from Active Directory and/or other sources.

Modifying the lookups within InfoSec app is only possible if you have installed the [Lookup File Editor](https://splunkbase.splunk.com/app/1724) app.
	
####Experimental Dashboards

![Experimental Dashboards](./Images/ExperimentalDashboards.png)

There are also a number of experimental dashboards within the InfoSec app. Consider this a sampler of newer dashboards that are under development. These dashboards may eventually be moved and incorporated into other parts of the InfoSec app.
	
###Help

![Help](./Images/Help.png)

The `Help` menu will provide you with links to documentation and instructions on configuring the InfoSec app. Please look through the information provided prior to reaching out to the developer.

##Support

* The InfoSec App for Splunk is built by [Splunk Works](https://splunkbase.splunk.com/apps/#/author/splunklabs) and is developer supported. More information on support can be found on [Splunkbase](https://splunkbase.splunk.com/app/4240/#/details).

If you have issues and require some assistance post a question to [Splunk Answers](https://community.splunk.com) using the tag "[InfoSec App for Splunk](https://community.splunk.com/t5/tag/InfoSec%20App%20for%20Splunk/tg-p)" before directly contacting the developer.

##Troubleshooting

These are some of the more common issues that get raised when first installing and configuring the InfoSec app. Again, if you get stuck, please search [Splunk Answers](https://community.splunk.com) using the tag "[InfoSec App for Splunk](https://community.splunk.com/t5/tag/InfoSec%20App%20for%20Splunk/tg-p)".

1. One or more of my InfoSec app dashboards is not showing any data.

	> This could be caused by a number of things.
	>
	> Check that the search that drives the dashboard is finding data within your Splunk environment. You can find this out by clicking on the `magnifying glass` in the bottom right of the dashboard and examining the associated search string. The first line will identify the data model that the dashboard is based on. Revisit the configuration steps to ensure the right data is feeding the identified data model. 
	> 
	> Try simplifying the search to determine what part of the search is preventing data from being displayed. Try removing all but the first line of the search and see if data is returned. Try re-adding additional lines from the original search, one-by-one to identify what, if anything, in the search is excluding data from being returned. You might find there is something in your data that is not fully CIM compliant. You may need to revisit the configuration.
	> 
	> You could also try posting a question to [Splunk Answers](https://answers.splunk.com).

2. Some of the dashboards are displaying a message `No matching visualization found for type: XXX, in app: XXX`

	> This normally indicates that one of the supporting add-ons is not installed, or it has been disabled.
	>
	> Go to the `Manage Apps` menu and confirm that the identified missing visual has been installed. If it has been installed, also check that it has not been disabled and that the permissions for the app are set correctly (e.g. not private).
	
3. Some of the dashboards are displaying `Data model was not found`.

	> This could indicate that a certain data model is missing. Open the Data Model menu and see if you can find the data model. Confirm the permissions have been set correctly. Confirm that the Common Information Model app has been correctly installed and that the app is enabled within the settings menu.
	
4. The InfoSec app is installed but it is not visible in the Splunk App menu

    > This may indicate that the InfoSec app has been disabled. Go to the `Manage Apps` menu and check the settings for the InfoSec app. Select the `Edit Properties` menu and enable the app if it has been disabled.



##Contributing

We welcome feedback and contributions from the community! Please see our
[contribution guidelines](CONTRIBUTING.md) for more information on how
to get involved.
