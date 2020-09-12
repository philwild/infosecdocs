# Welcome to the InfoSec app for Splunk!

The [InfoSec App for Splunk](https://splunkbase.splunk.com/app/4240/) is a free app for the Splunk platform which can be downloaded and installed into your Splunk environment. It is available from [Splunkbase](https://splunkbase.splunk.com/).

The InfoSec App for Splunk should not to be confused with [Enterprise Security](https://www.splunk.com/en_us/software/enterprise-security.html), Splunk's premium security solution. Although both solutions are security solutions, the features and capabilities of Enterprise Security are significantly deeper than what is available within the InfoSec app.

InfoSec app for Splunk is an entry, or starter level security solution powered by the Splunk platform. It is
designed to address the most common security use cases, including continuous monitoring and security investigations. InfoSec app also includes a number of advanced threat detection use cases that can be further expanded using security resources available for Splunk like the [Security Essentials app for Splunk](https://splunkbase.splunk.com/app/3435/).

Splunk Apps provide solutions for many common use cases. They provide specialised insight into your data and systems with pre-configured dashboards, reports, data inputs, and saved searches. Apps for Splunk are available from [Splunkbase](https://splunkbase.splunk.com/). The Splunkbase library has 1000+ apps and add-ons from Splunk, our partners, and our community. They can be directly downloaded, installed and configured within your Splunk environment.

## Product Goals

The InfoSec app for Splunk aims to achieve the following:

* Provide an entry level security solution to new and existing Splunk customers that are not yet ready or able to invest in Splunk's Enterprise Security platform.
* Make it easy to direct Splunk's powerful features towards security.
* Provide a single pane view of your security events and posture.
* Allow the user to investigate security alerts and incidents.
* Provide a base platform that can be customised and expanded to meet your security needs using additional apps and add-ons from Splunkbase.

## Before we start

This documentation is not designed to replace formal training or Splunk's own documentation. It focusses on the introductory steps and knowledge required to get the InfoSec app up and running in a short amount of time. It assumes the user is fairly new to Splunk and may not have yet grasped many of Splunk's fundamental concepts. Consider this documentation as a fast-start guide to getting the InfoSec app up and running within your environment. This documentation will introduce you to key Splunk concepts, lightly touching on each. Links will be provided to Splunk's documentation so you can delve further into Splunk's capabilities, as required. Although this document focuses on the InfoSec App for Splunk, the topics covered can be applied to other apps and configurations within Splunk.

## Introduction to the InfoSec app

The InfoSec app provides the user with a number of pre-configured and customisable security focussed dashboards and alerts. 

* Overview

Description

[** Video **]

**Security Posture**

![Security Posture](./Images/SecurityPosture.png)
As the title suggests, the Security Posture dashboard provides a high-level view of your security posture. At the top of the dashboard there are two rows of indicators. The top-most row displays statistical counts of events covering your Intrusion Detection System (IDS), AntiVirus and Malware systems. Each indicator shows the current state, with an arrow identifying the rate of change (positive, neutral, or negative) and the previously recorded statistic from 24 hours ago.

The second row of indicators displays the number of detected hosts and devices, along with the number of detected accounts being monitored. Each indicator also includes the 24 hour trend and previous result for comparative purposes.

Clicking on any of these indicators will open a new dashboard with more detailed information.

Together, these two rows of indicators gives you an immediate view of the state of your environment compared to how it looked yesterday.

The next row includes three dashboards that focus on Intrusion alerts, splitting and breaking down the reporting into a statistical count of the total "Alerts by Severity", a 24 hour view of those alerts over time, and the Top-10 most critical alerts charted over the same 24 hour window.

Clicking on any of these dashboards will open a new window that focuses on your IDS.

The last row contains two punchcard style dashboards that focus on account and asset information within your organisation. For these dashboards to populate, the punchcard visualisation has to have been installed and enabled within your Splunk instance. If you do not see the punchcard visualisation matching the above screen-shot, it may indicate that this visualisation has not been installed or may have been disabled. You may see the message "No matching visualization found for type: punchcard, in app: punchcard_app". Installing this app will be discussed [later](# Supporting apps and add-ons).

These two dashboards provide a swim-lane style view of the type and count of events being detected against your identities and assets over the past 24 hours. These two dashboards allow you to quickly identify bursts of activity that may need investigating.

**Continuous Monitoring**

* Windows Access and Changes

	![Windows Access and Changes](./Images/WindowsAccessAndChanges.png)
	
	The Windows Access and Changes dashboard focuses on events within your Microsoft Windows environment. It presents information relating to:
	
 - Locked Out Accounts
      - Privilege Escalations
      - Change and 
     
   * All Authentications

	![All Authentications](./Images/AllAuthentications.png)

	[Description here]
	
	* Malware

	![Malware](./Images/Malware.png)

	[Description here]
	
	* Intrusion Detection (IDS/IPS)

	![Intrusion Detection](./Images/IntrusionDetection.png)

	[Description here]
	
	* Firewalls

	![Firewalls](./Images/Firewalls.png)

	[Description here]
	
	* Network Traffic

	![Network Traffic](./Images/Networktraffic.png)

	[Description here]
	
	* VPN Access
	
	![VPN Access](./Images/VPN.png)

	[Description here]
	
* Advanced Threats
	* Access Anomalies

	![Access Anomalies](./Images/AccessAnomalies.png)

	[Description here]
	
	* Network Anomalies

	![Network Anomalies](./Images/NetworkAnomalies.png)

	[Description here]
	
	* Custom Use Cases

	![Custom Use Cases](./Images/CustomUseCases.png)

	[Description here]
	
* Investigation
	* user Investigation

	![User Investigation](./Images/UserInvestigation.png)

	[Description here]
	
	* Host Investigation

	![Host Investigation](./Images/HostInvestigation.png)

	[Description here]
	
* Compliance

	![Compliance](./Images/Compliance.png)

	[Description here]

* Executive View

	![Executive View](./Images/ExecutiveView.png)

	[Description here]

* Alerts

	![Alerts](./Images/Alerts.png)

	[Description here]

* Incident Posture

	![Incident Posture](./Images/IncidentPosture.png)

	[Description here]

* Health

	![Health](./Images/Health.png)

	[Description here]

* Search
	* Search

	![Search](./Images/Search.png)

	[Description here]
	
	* Dashboards

	![](./Images/Dashboards.png)

	[Description here]
	
	* Lookups

	![Lookups](./Images/Lookups.png)

	[Description here]
	
	* Experimental Dashboards

	![Experimental Dashboards](./Images/ExperimentalDashboards.png)

	[Description here]
	
* Help

	![Help](./Images/Help.png)

	[Description here]


## Getting Data In

### Forwarders
### HTTP Event Collector (HEC)
### Apps and Add-ons

* Introduction to Apps and Add-ons
* Splunkbase
* Installing Apps and Add-ons

### Inputs Data Manager (IDM)

**Splunk supported Add-ons**

[Full list can be found here](https://docs.splunk.com/Documentation/AddOns)



## Installation

**Installation Prerequisites**

The InfoSec app for Splunk can be installed directly into Splunk in the same way as other available apps from [Splunkbase](https://splunkbase.splunk.com/).

It's assumed that you already have Splunk installed somewhere, or you're using Splunk Cloud. This document does not cover installing and configuring Splunk for the first time. If you need to do this before proceeding further, please view the following resources:

* [Installing Splunk on Linux documentation](https://docs.splunk.com/Documentation/Splunk/latest/Installation/InstallonLinux). There's also a video [here](https://www.splunk.com/en_us/training/videos/installing-splunk-enterprise-on-linux.html).

* [Installing Splunk on Windows documentation](https://docs.splunk.com/Documentation/Splunk/latest/Installation/InstallonWindows). There's also a video [here](https://www.splunk.com/en_us/resources/videos/installing-splunk-on-windows.html).

* [Start Splunk Enterprise for the first time](https://docs.splunk.com/Documentation/Splunk/latest/Installation/StartSplunkforthefirsttime)

* [Installing the Splunk Enterprise License](https://docs.splunk.com/Documentation/Splunk/latest/Installation/Installalicense)

* [A short introductory video to using the Splunk web interface](https://www.splunk.com/en_us/resources/videos/splunk-web-demo.html)

**Installation Steps**

The method for installing the InfoSec app will vary slightly between Splunk Enterprise and Splunk Cloud. If there is a difference within the steps. Each will be explained.

1. Log into your Splunk environment with an account that has administrative privileges.

2. Select the App menu within the black menu bar at the top left of the Splunk web user interface (just to the right of the Splunk logo). 

   <img src="./Images/AppMenu.png" width=50% height=50%>

3. Select Find More Apps

   <img src="./Images/FindMoreApps.png" width=50% height=50%>
  

4. Within the search menu on the top-left of the page, search for "infosec app for splunk". The InfoSec App for Splunk should be listed as one of the available apps for installation.

   <img src="./Images/Search&Install.png" width=100% height=100%>
   
5. Press the green "Install" button for the InfoSec App for Splunk. The process will be slightly different between Splunk Cloud and Splunk Enterprise.

    Note: The ability to install Apps and Add-ons directly into your Splunk environment requires internet connectivity. Your Splunk environment must be able to access https://splunkbase.splunk.com over port TCP/443. If searching for additional apps like the InfoSec app is not producing any results, you may have a problem with Internet connectivity. If the only method of gaining access is through a proxy server, then this must be configured. Instructions on how to configure Splunk to use your HTTP Proxy Server can be found [here](https://docs.splunk.com/Documentation/Splunk/latest/Admin/ConfigureSplunkforproxy). If configuring Internet access for your Splunk environment is not possible, you can still install apps manually via a two step process. You will need to download the apps from [Splunkbase](https://splunkbase.splunk.com) to your desktop and then install the apps into your Splunk environment via "[Install app from file](https://community.splunk.com/t5/Archive/How-to-install-a-splunk-app/m-p/87912)". This is not applicable for Splunk Cloud.

   **Splunk Cloud**

   When asked to confirm, select "Continue".

   **Splunk Enterprise**

   Login with your splunk.com credentials to install the app, not your Splunk Enterprise instance account. You will also need to accept the Terms and Conditions before being able to proceed.
      
   <img src="./Images/Login&Install.png" width=50% height=50%>
   
   If you have a larger distributed Splunk Enterprise environment you only need to install the InfoSec app on the search head. It does not need to be installed on the indexers.  
   
The InfoSec app for Splunk should now be installed. To confirm this, select the InfoSec app from the App menu (see step 2, above). You should be presented with the "Security Posture" dashboard.

**Additional Apps and Add-ons**

A number of supporting Splunk Apps and Add-ons from Splunkbase must also be installed before you can start using the InfoSec app. These are:

* [Splunk Common Information Model (CIM)](https://splunkbase.splunk.com/app/1621/)
* [Punchcard visualization](https://splunkbase.splunk.com/app/3129/)
* [Force Directed visualization](https://splunkbase.splunk.com/app/3767/)
* [Lookup File Editor](https://splunkbase.splunk.com/app/1724/) (new requirement starting from InfoSec v1.5)
* [Sankey Diagram visualization](https://splunkbase.splunk.com/app/3112/) (new optional prerequisite for the experimental VPN Access dashboard starting from v1.5.3)

The process to install these additional Apps and Add-ons is the same as you've just completed when installing the InfoSec app. Repeat the above steps to install each of these additional Apps and Add-ons.

Once you've reached this step, you are ready to start configuring the InfoSec App for Splunk.
   

## Configuration

### Data Sources   




Notes:

IMPORTANT: PREREQUISITES

At a minimum, you should have data from the following security sources collected by your Splunk environment:

Firewall data like Cisco ASA, Palo Alto Networks, Check Point, Juniper, Fortinet, etc.
Active Directory security logs (make sure that your audit policy enables logging failed and successful authentication attempts)
Antivirus/Malware data like McAfee, Symantec, Trend Micro, etc.
All data used by InfoSec app must be Common Information Model (CIM)-compliant. The easiest way to accomplish that is to use CIM-compliant Splunk Add-ons for your security devices *(*** See Splunkbase list of CIM add-ons ***)
*

The following Data Models must be accelerated:

Authentication
Change (for app version 1.6.x and newer) or Change Analysis (for app version 1.5.3 and older)
Intrusion_Detection
Malware
Network_Sessions
Network_Traffic
Endpoint
Web (new requirement starting from InfoSec v1.5)

### required Data Sources

- Firewall, IDS/IPS data (e.g. Cisco, Palo Alto Networks, Check Point, Fortinet, Juniper)

- Active Directory data (Windows logs from Domain Controllers)

- Malware/antivirus tools data (e.g. Symantec, McAfee, Sophos, Trend Micro)





- Microsoft365 or AD
- Linux Authentication
- Windows Security Logs
- Palo Alto Firewall
- Symantec Endpoint Protection
- Suricata IDS

##Concepts and definitions

The InfoSec app relies on accelerated data models and the Common Information model (CIM) to provide a consistent and normalised view into the event data that you'll bring into Splunk. Understanding how to configure and use the CIM and data models also requires an understanding of indexes, sourcetypes, sources, fields, eventtypes, tags, macros and a few other concepts.

Splunk provides a [Splexicon](https://docs.splunk.com/Splexicon), which is a glossary of technical terminology that is specific to Splunk software. Definitions include links to related information in the Splunk documentation.
 
###Common Information Model (CIM)

The Splunk Common Information Model (CIM) is a shared semantic model focused on extracting value from data. The CIM is implemented as an add-on that contains a collection of data models (we'll get to what that means soon), documentation, and tools that support the consistent, normalised treatment of data for maximum efficiency at search time.

The InfoSec app relies on the CIM to function properly. If you have not yet installed the CIM to support the InfoSec app. Please look at the [Installation Instructions](#Installation).

Splunk Education has published a short video explaining the value and use of the CIM,  one to Youtube [here](https://www.youtube.com/watch?v=QTklD7OiN74) (8:30 mins). The video also covers installation and configuration of the CIM.

The CIM add-on contains a collection of preconfigured data models that you can apply to your data at search time. Each data model in the CIM consists of a set of field names and tags that define the least common denominator of a domain of interest. You can use these data models to normalise and validate data at search time, accelerate key data in searches and dashboards, or create new reports and visualisations with Pivot.

The add-on also contains several tools that are intended to make analysis, validation, and alerting easier and more consistent. These tools include a custom command for CIM validation and a common action model, which is the common information model for custom alert actions. See [Approaches to using the CIM](https://docs.splunk.com/Documentation/CIM/latest/User/HowtouseCIM) for more information about the tools available in the CIM add-on.

For the InfoSec app to correctly report on the data that you have in Splunk, that data must be present within the supporting data models which means the data must be CIM compliant.

###Index

Splunk stores your data in indexes as events. The default index in splunk is called "main". Splunk will store your event data in this main index if you don't tell Splunk to put it anywhere else. You can create and specify other indexes for different data inputs. There are several key reasons for having multiple indexes:

* To control user access.
* To accommodate varying retention policies.
* To speed searches in certain situations.

When configuring data models in Splunk, in most cases, you would restrict each datamodel to just the indexes that contain the data that populates the data model.

Further information on using, creating and manageing indexes in Splunk can be found [here](https://docs.splunk.com/Documentation/Splunk/latest/Indexer/Setupmultipleindexes).

###Source type

A source type is used to name or identify each different type of data in Splunk. The definition of a sourcetype will define how the timestamp is interpreted, what defines the break between different events and how Splunk might decipher and understand the structure of events. A source type could be considered the fingerprint or DNA of the event data entering Splunk. When configuring Splunk to receive or index data, you will always define a source type, or a source type may be pre-defined within an Add-on that you've chosen to use to help you onboard data into Splunk. As an example, the source types defined within the Splunk Add-on for Windows are listed within Splunk's documentation [here](https://docs.splunk.com/Documentation/WindowsAddOn/latest/User/SourcetypesandCIMdatamodelinfo).

Some source types may be structured, such as json, XML or CSV whereas others may have no structure.

This [blog post](https://www.splunk.com/en_us/blog/tips-and-tricks/sourcetypes-whats-in-name.html) provides a good introduction to source types with Splunk.

Splunk software ships with a set of built-in source types that are known as [pretrained source types](https://docs.splunk.com/Documentation/Splunk/latest/Data/Listofpretrainedsourcetypes).

###Source

A source in Splunk is not to be confused with source type. Where a source type identifies the structure of events or data within Splunk, the source identifies where that event data has come from. The source is the name of the file, stream or other input from which a particular event has cme from. The below is an example of the difference between source and sourcetype

`source=/var/log/messages and sourcetype=linux_syslog`

Every event in Splunk will have a pre-defined index, host, source, sourcetype and _time field. For more information, see [default fields](https://docs.splunk.com/Splexicon:Defaultfield).

###Host

Within Splunk, all event data will be asigned to a host. The host identifies the network device that collected the data for Splunk. It may be a hostname or IP address. Further information can be found in the [Splunk documentation](https://docs.splunk.com/Documentation/Splunk/8.0.5/Data/Abouthosts). The host field is considered a [default fields](https://docs.splunk.com/Splexicon:Defaultfield).

###Field

Fields appear in event data as searchable name-value pairings such as `user_name=fred`. Fields are the building blocks of Splunk searches, reports and data models.

Splunk will attempt to auto-extract values into fields from within the event data that is being indexed. This is normally performed at search time.

Fields will often be defined within event data as key value pairs such as `user=fred` or `src:192.168.10.5` or may simply be a number or text within the structure of the event with no defined key. Splunk can still identify these fields using a custom [field extraction](https://docs.splunk.com/Splexicon:Fieldextraction) through Splunk web. A field extraction is defined against a source type, a source or a host.

Further information on fields in Splunk can be found [here](https://docs.splunk.com/Documentation/Splunk/latest/Knowledge/Aboutfields).

The values from fields within event data are used populate enabled data models within Splunk. 

Often, fields defined as key value pairs within event data may not align with the naming standard defined within the CIM and data models. In order to work with this event data the names of these fields needs to be be changed to conform with the CIM naming standard. This can be done using Aliases.

###Alias

An alias (or field alias) in Splunk is an alternate name assigned to a field that has been extracted from the event data within a Splunk index. Field aliases for fields can be defined against a source type, a source or a host. They can be defined within Splunk web by going into the Settings -> Fields menu. If you are working with a data source that is not yet CIM compliant, you may need to create field aliases to map existing fields within your data source to the [CIM naming convention](https://docs.splunk.com/Documentation/CIM/latest/User/CIMfields).

See Splunk's [documentation on Fields](https://docs.splunk.com/Documentation/Splunk/latest/Knowledge/Abouttagsandaliases) for further information.

###Event type

An event type in Splunk is a category of events united by the same search. Event types are useful for categorising a subset of event data from within one source type, or uniting events of a certain type across multiple source types. Event types and tags go hand-in-hand in asisting with preparing data for use in data models.

This is an older Splunk [video](https://www.youtube.com/watch?v=KhdMgT9VbHs) that covers the subject of event types.

See Splunk's [documentation on event types](https://docs.splunk.com/Documentation/Splunk/latest/Knowledge/Abouteventtypes) for further information.

###Tags

Tags enable you to assign names to specific field and value combinations. This includes event type, host, source and source type field value combinations. Tags tend to work hand-in-hand with event types.
An example of the use of tags might be to create an `authentication` tag as:

	`eventtype=windows_successful_login
	eventtype=windows_failed_login
	eventtype=vpn_successful_login
	eventtype=vpn_failed_login`

###Permissions, users, roles and apps

###Macros

###Datamodels and acceleration

###Configuration Files

###The data pipeline

###Alerts

##Using the InfoSec app

##Troubleshooting


##Support

* The InfoSec App for Splunk is built by [Splunk Works](https://splunkbase.splunk.com/apps/#/author/splunklabs) and is developer supported. More information on support can be found on [Splunkbase](https://splunkbase.splunk.com/app/4240/#/details).

If you have issues and require some assistance post a question to [Splunk Answers](https://community.splunk.com) using the tag "[InfoSec App for Splunk](https://community.splunk.com/t5/tag/InfoSec%20App%20for%20Splunk/tg-p)" before contacting the developer.

Get involved, try it out, ask questions, and make
new friends!

##Contributing

We welcome feedback and contributions from the community! Please see our
[contribution guidelines](CONTRIBUTING.md) for more information on how
to get involved.
