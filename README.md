OpenIntelligence Natural Language Interface App version 1.0.2
Copyright (C) 2021 Ideasol Australia Pty Ltd (trading as OpenIntelligence). All Rights Reserved. 
---

## Introduction
Welcome to the OpenIntelligence Natural Language Interface for Splunk.
Our natural language interface allows both novices and experienced Splunk users to search for information or define complex correlation rules in their own language. 
The interface uses an entity driven approach (e.g. devices or accounts) to incrementally build complex natural language queries (a subset with a very precise and unambiguous semantic) and translate them to the Splunk SPL query language. These entities also help to identify suitable queries and automatically generate joining attributes between different event types.
This initial version of the App offers two different natural language wizards. Later version will complement these wizards with a natural language search bar.
For additional documentation or access to the latest version of this app, please visit [openintelligence-nli-app](https://openintelligence.com.au/openintelligence-nli-app) or visit the public github project [openintelligence_nli_app](https://github.com/alonsom/openintelligence_nli_app).

## Dependencies
This app has the following dependencies:
- Licensed access to the Rest API of an OpenIntelligence Natural Language Rules Engine instance. This REST API provides access to our sophisticated Rules Engine and its capability to translate natural language statements to Splunk queries. 
- The Webtools Add-on.  This Add-on includes a *curl* command and is used to access the Rest API above. This Add-on may be downloaded at [Webtools Add-on](https://splunkbase.splunk.com/app/4146).

Our App works best  when the Splunk Common Information Model App (Splunk_SA_CIM) is installed. This App is available at [Splunk_SA_CIM](https://splunkbase.splunk.com/app/1621/).

## Rest API Licenses
OpenIntelligence offers three different Rest API/SW licenses:
- ** A Trial Licence ** provides temporary access to the Rest API of our Rules Engine development instance. The trial license is for evaluation purposes only and provides limited functionality. 
- ** A Shared Production License ** provides access to the Rest API of our shared Rules Engine Production instance and includes OpenIntelligence standard support. 
- ** A Custom Production Licence ** provides access to a dedicated and customized Rules Engine Production instance with several hosting and support options.
Please visit [licenses](https://openintelligence.com.au/licenses) for more details and how to request any of these licences.

## Install Instructions
This App depends on a valid Rest API license that will provide you with the Rules Engine URL (host/port) and initial user credentials (user/password).
Please Install the App and above dependencies and then configure the apps macros *oi_host*, *oi_port* and *oi_user* with the values provided by your license (remember to insert all values between double-quotes).
You will also need to setup a *user* and *password* in **passwords.conf** (please follow the template provided in the default folder) and reload the settings (e.g. restart the server).
The password may be entered in plain test or encoded ("encrypted") using Splunk standard encoding of credentials.
To obtain an encoded version of your password, please run the following command in your Splunk instance:
For NIX instances:
`/opt/splunk/bin/splunk show-encrypted --value YOUR_PLAIN_TEXT_LICENSE_PASSWORD`
For Window instances:
`C:\Program Files\Splunk\bin> .\splunk.exe show-encrypted YOUR_PLAIN_TEXT_LICENSE_PASSWORD`

This App includes two saved searches: CacheEntities and CacheEvents that synchronize cached entities and events with their latest definition in the Rest API server.
If you have installed the latest version of the Splunk App you will only need to run theses searches each time a new version of the Rest API has been released (we will notify you of any release date in advance). Alternatively, you could download the latest version of this App that will include updated versions of cached entities and events.
For Customized Production instances is recommended to schedule both searches to run daily or maybe more often depending on the frequency of your changes to the entities, data-models and events tables.

## Available Versions
The trial and shared versions of the rule engine generate both simple and complex correlation and statistical queries that could be run in any platform where the CIM Model App is available. They also generate queries using some common events like Windows events (you will not need the CIM Model App in this case).
Custom versions extend these capabilities with optimized queries using organisation specific data-models, events, and lookups.  It also enables the organizations to extend the product natural language capabilities by defining new entities, adjectives, verbs, and adverbs.

## Main Menu
- The Event Wizard enable building simple and complex correlations and statistical operations over CIM data-models/common events. 
- The Entity Wizard extends the Event Wizard with entities (e.g. device, account) driving the generation of the natural language statements.
- The search option give you access to Splunk standard search bar (to be replaced by a natural language search bar in the next version of this tool).
- The Entities Mapping displays list of identified entities and their mapping to local lookups/queries (to update available entities and associated mappings you will need a valid Custom licence).

## Troubleshooting
If the Webtools Add-on is not installed or the App is unable to connect to a licensed OI-Rest API, the App will return an error message.
If the Splunk_SA_CIM App is not installed, many of the generated queries will not be able to be executed in this Splunk environment (but they could be copied to run in other environments where this App is available).

## Feedback/Support
This is an open source App, no official support is provided but please feel free to drop us an email to info@openintelligence.com.au or visit our [contact-us](https://openintelligence.com.au/contact-us) page if you have any problem, question or suggestion.
Shared and Custom Rest API licenses include standard support for this App. 

## Disclaimer
This App is released under the [GNU GENERAL PUBLIC LICENSE](https://www.gnu.org/licenses/gpl-3.0.html) and is provided on an “as is” and “as available” basis. 
Open Intelligence does not give any warranties, whether express or implied, as to the suitability or usability of the App beyond the ones included in any valid Rest API Licenses assigned to you.
