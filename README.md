# Clearswift SECURE Email Gateway Add-on for Splunk Enterprise
## Table of Contents

### OVERVIEW

- About the Clearswift SECURE Email Gateway Add-on for Splunk Enterprise
- Release notes
- Support and resources

### INSTALLATION AND CONFIGURATION

- Hardware and software requirements
- Installation steps
- Deploy to single server instance
- Deploy to distributed deployment
- Deploy to distributed deployment with Search Head Pooling
- Deploy to distributed deployment with Search Head Clustering
- Deploy to Splunk Cloud 
- Configure Clearswift SECURE Email Gateway Add-on for Splunk Enterprise

### USER GUIDE

- Data types
- Lookups

### OVERVIEW

#### About the Clearswift SECURE Email Gateway Add-on for Splunk Enterprise

| Author | Mikael Bjerkeland |
| --- | --- |
| App Version | 1.1 |
| Vendor Products | Clearswift SECURE Email Gateway 3.8 or higher |
| Has index-time operations | True |
| Create an index | False |
| Implements summarization | False |

The Clearswift SECURE Email Gateway Add-on for Splunk Enterprise allows a Splunk® Enterprise administrator to extract and filter event information from Clearswift SECURE Email Gateway appliances. The app sets the correct sourcetype and adds fields required for CIM compliance.

##### Scripts and binaries

No scripts or binaries are included.

#### Release notes

##### About this release

Version 1.1 of the Clearswift SECURE Email Gateway Add-on for Splunk Enterprise is compatible with:

| Splunk Enterprise versions | 6.x |
| --- | --- |
| CIM | 4.2, 4.1, 4.0 |
| Platforms | Platform independent |
| Vendor Products | Clearswift SECURE Email Gateway |
| Lookup file changes |  |

##### New features

Clearswift SECURE Email Gateway Add-on for Splunk Enterprise includes the following new features:

- Renamed message_id as internal_message_id.

##### Fixed issues

Version 1.1 of the Clearswift SECURE Email Gateway Add-on for Splunk Enterprise fixes the following issues:

- None

##### Known issues

Version 1.1 of the Clearswift SECURE Email Gateway Add-on for Splunk Enterprise has the following known issues:

- None known

##### Third-party software attributions

Version 1.1 of the Clearswift SECURE Email Gateway Add-on for Splunk Enterprise incorporates the following third-party software or libraries.

- None

##### Support and resources

**This app is community supported on a best effort basis. In case you have needs for professional support billed by the hour, please contact the author.

* Access questions and answers specific to the Clearswift SECURE Email Gateway Add-on for Splunk Enterprise at http://answers.splunk.com/answers/app/2916

## INSTALLATION AND CONFIGURATION

### Hardware and software requirements

#### Hardware requirements

Clearswift SECURE Email Gateway Add-on for Splunk Enterprise supports the following server platforms in the versions supported by Splunk Enterprise:

- Windows 7, 8, and 8.1 (64-bit)
- Windows Server 2008, 2008 R2, 2012 and 2012 R2 (64-bit)
- Windows 7, and 8 and 8.1 (32-bit)
- Windows Server 2008 (32-bit)
- 2.6+ kernel Linux distributions (64-bit)
- 2.6+ kernel Linux distributions (32-bit)
- Solaris 10, 11 (64-bit)
- Solaris 10, 11 (SPARC)
- OSX 10.8 (Intel)
- OSX 10.9 (Intel)
- OSX 10.10 (Intel)
- FreeBSD 8, and 9 (64-bit)
- AIX 6.1, 7.1

#### Software requirements

To function properly, Clearswift SECURE Email Gateway Add-on for Splunk Enterprise requires the following software:

- Optional: Splunk App for Enterprise Security

#### Splunk Enterprise system requirements

Because this add-on runs on Splunk Enterprise, all of the [Splunk Enterprise system requirements](http://docs.splunk.com/Documentation/Splunk/latest/Installation/Systemrequirements) apply.

#### Download

Download the Clearswift SECURE Email Gateway Add-on for Splunk Enterprise at https://splunkbase.splunk.com/app/2916/

#### Installation steps

To install and configure this app on your supported platform, follow these steps:

1. In your Splunk Enterprise web interface, click on App(s) -> Manage Apps
1. Click on Install app from file
1. Select the file you downloaded, Click Upload, optionally selecting Upgrade app if you are upgrading from an earlier version. Restart Splunk if required

##### Deploy to single server instance

Follow these steps to install the app in a single server instance of Splunk Enterprise:

1. In your Splunk Enterprise web interface, click on App(s) -> Manage Apps
1. Click on Install app from file
1. Select the file you downloaded, Click Upload, optionally selecting Upgrade app if you are upgrading from an earlier version. Restart Splunk if required

##### Deploy to distributed deployment

**Install to search head**

1. In your Splunk Enterprise web interface, click on App(s) -> Manage Apps
1. Click on Install app from file
1. Select the file you downloaded, Click Upload, optionally selecting Upgrade app if you are upgrading from an earlier version. Restart Splunk if required

**Install to indexers**

1. In your Splunk Enterprise web interface, click on App(s) -> Manage Apps
1. Click on Install app from file
1. Select the file you downloaded, Click Upload, optionally selecting Upgrade app if you are upgrading from an earlier version. Restart Splunk if required

**Install to forwarders**

This app should not be installed on forwarders.

##### Deploy to distributed deployment with Search Head Pooling
Follow the same steps as *Install to search head*.
##### Deploy to distributed deployment with Search Head Clustering
Follow the same steps as *Install to search head*.
##### Deploy to Splunk Cloud
Unknown
#### Configure Clearswift SECURE Email Gateway Add-on for Splunk Enterprise

1. Install in $SPLUNK_HOME/etc/apps/TA-Clearswift_SEG

1. Create a TCP input on one of your Splunk servers or a forwarder with sourcetype set to *clearswift:seg*.
2. Configure your Clearswift SECURE Email Gateway appliances to send their Audit and Message syslogs to the TCP input created in step 1.
3. Restart Splunk

## USER GUIDE

### Data types

This app provides search-time knowledge for the following types of data from Clearswift SECURE Email Gateway:

**Search-time**

- clearswift:seg - Syslog events from your appliances

These data types support the following Common Information Model data models:

| Source Type | CIM Data Models |
| --- | --- |
| clearswift:seg | Change Analysis<br/>Email<br/>|


### Lookups

The Clearswift SECURE Email Gateway Add-on for Splunk Enterprise contains 1 lookup file.

**clearswift_seg_actions.csv**

Maps a vendor action to a CIM compliant action.

- File location: lookups/clearswift_seg_actions.csv
- Lookup fields: vendor_action, action
- Lookup contents: See the file contents
