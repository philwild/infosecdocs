# Welcome to the InfoSec app for Splunk!

InfoSec app for Splunk is your starter security pack. InfoSec app is
designed to adddress the most common security use cases, including
continuous monitoring and security investigations. InfoSec app also
includes a number of advanced threat detection use cases. All of the
components of InfoSec app can be easily expanded using free security
resources available for Splunk like Security Essentials app for Splunk:
https://splunkbase.splunk.com/app/3435/

## Product Goals

* Bring a tested configuration and build of syslog-ng OSE to the market
that will function consistently regardless of the underlying host's
linux distribution * Provide a container with the tested configuration
for Docker/K8s that can be more easily deployed than upstream packages
directly on a customer OS * Provide validated (testable and tested)
implementations of filter and parse functions for common vendor products
* Reduce latency and improve scale by balancing event distribution
across Splunk Indexers

## Before we start

This documentation is not designed to replace formal training or Splunk's own documentation. It focusses on the introductory steps and knowledge required to get the InfoSec app upp and running in a short amount of time. The documentation will introduce you to key Splunk concepts, lightly touching on each. Links will be provided to Splunk's documentation so you can delve further into Splunk's capabilities, as required.

## Introduction

* Overview
* Security Posture
* Continuous Monitoring
	* Windows Access and Changes
	* All Authentications
	* Malware
	* Intrusion Detection (IDS/IPS)
	* Firewalls
	* Network Traffic
* Advanced Threats
	* Access Anomalies
	* Network Anomalies
	* Custom Use Cases
* Investigation
	* user Investigation
	* Host Investigation
* Compliance
* Executive View
* Alerts
* Health
* Search
	* Search
	* Dashboards
	* Lookups
	* Experimental Dashboards
* Help

## Getting Data In

### Forwarders
### HTTP Event Collector (HEC)
### Apps and Add-ons

**Splunk supported Add-ons**



[Full list can be found here](https://docs.splunk.com/Documentation/AddOns)


### Inputs Data Manager (IDM)

## Installation

### Supporting apps and add-ons


## Configuration

### Common Information Model (CIM)

The Splunk Common Information Model (CIM) is a shared semantic model focused on extracting value from data. The CIM is implemented as an add-on that contains a collection of data models (we'll get to what that means soon), documentation, and tools that support the consistent, normalized treatment of data for maximum efficiency at search time.

The InfoSec app relies on the CIM to function properly. If you have not yet installed the CIM to support the InfoSec app. Please look at the [Installation Instructions](#Installation).

The CIM add-on contains a collection of preconfigured data models that you can apply to your data at search time. Each data model in the CIM consists of a set of field names and tags that define the least common denominator of a domain of interest. You can use these data models to normalize and validate data at search time, accelerate key data in searches and dashboards, or create new reports and visualizations with Pivot.

The add-on also contains several tools that are intended to make analysis, validation, and alerting easier and more consistent. These tools include a custom command for CIM validation and a common action model, which is the common information model for custom alert actions. See Approaches to using the CIM for more information about the tools available in the CIM add-on.

### Indexes

### Macros

### Datamodels

## Using the InfoSec app




## Support

* UPDATE! Splunk Connect for Syslog is now officially supported by
Splunk.  That said, it is still very much an open-source product and the
notes below outlining community support are still highly relevant.

Splunk Connect for Syslog is an open source product developed by
Splunkers with contributions from the community of partners and
customers. This unique product will be enhanced, maintained and
supported by the community, led by Splunkers with deep subject matter
expertise. The primary reason why Splunk is taking this approach is to
push product development closer to those that use and depend upon it.
This direct connection will help us all be more successful and move at a
rapid pace.

Post a question to Splunk Answers using the tag "Splunk Connect For
Syslog"

Join the #splunk-connect-for-syslog room in the splunk-usergroups Slack
Workspace. If you don't yet have an account [sign
up](https://docs.splunk.com/Documentation/Community/1.0/community/Chat)

Please use the GitHub issue tracker to submit bugs or request
enhancements: https://github.com/splunk/splunk-connect-for-syslog/issues

Get involved, try it out, ask questions, contribute filters, and make
new friends!

## Contributing

We welcome feedback and contributions from the community! Please see our
[contribution guidelines](CONTRIBUTING.md) for more information on how
to get involved.
