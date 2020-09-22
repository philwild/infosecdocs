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
