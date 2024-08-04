OpenIntelligence Natural Language Interface App version 2.0.0
Copyright (C) 2022 Ideasol Australia Pty Ltd (trading as OpenIntelligence). All Rights Reserved. 
---

## Introduction
Welcome to the OpenIntelligence Natural Language Interface for Splunk.
Our natural language interface allows both novices and experienced Splunk users to search for information or define complex correlation rules in their language. 
This version brings the new natural language search bar.  This sophisticated AI interface understands your users' language and translates their natural language statements to Splunk queries and visualisations.  It also included an improved version of our standard natural language wizard with an incremental, guided approach for building natural language statements and associated Splunk queries. It also brings a history of queries.
Our custom version (please see Versions and Licenses below) extend these capabilities with tailored queries using organisation specific data-models, events, and lookups.  It also includes customisation options like the ability to define new entities, adjectives, verbs, and adverbs.
For additional documentation or access to the latest version of this app, please visit [openintelligence-nli-app](https://openintelligence.com.au/openintelligence-nli-app) or our public GitHub project [openintelligence_nli_app](https://github.com/alonsom/openintelligence_nli_app).

## Dependencies
This app has the following dependencies:
- Splunk 8.x  (e.g. 8.2.1). Version 9.x has introduced some changes to the Python libraries that are impacting the App used for the rest calls. It will be fixed in the next few days,
- Licensed access to the Rest API of an OpenIntelligence Natural Language Rules Engine instance. This REST API provides access to our sophisticated Rules Engine and its capability to translate natural language statements to Splunk queries. 
- The Webtools Add-on. This Add-on includes a *curl* command and is used to access the Rest API above. This Add-on may be downloaded at [Webtools Add-on](https://splunkbase.splunk.com/app/4146).

Our App does not depend on the Splunk Common Information Model App ([Splunk_SA_CIM](https://splunkbase.splunk.com/app/1621/)) but will benefit from any data model and acceleration available.

## Versions and Licenses
OpenIntelligence offers three different Rest API/SW licenses:
- ** A Trial Licence ** provides temporary access to the Rest API of our Rules Engine development instance. This license is for evaluation purposes only and has a limit on the number of daily queries.
- ** A Shared Production License ** provides access to the Rest API of our shared Rules Engine Production instance and includes OpenIntelligence standard support. 
- ** A Custom Production Licence ** provides access to a dedicated and customized Rules Engine Production instance with several hosting and support options.
Please visit [licenses](https://openintelligence.com.au/licenses) for more details and how to request any of these licences.

## Install Instructions
This App depends on a valid Rest API license that will provide you with the Rules Engine URL (host/port) and initial user credentials (user/password).
Please Install the App and above dependencies and then select the *Settings* tab in the main menu to configure the apps macros *oi_host*, *oi_port*, *oi_user* and *oi_pass* with the values provided by your license (remember to insert all values between double-quotes).

## Main Menu
- The Natural Language Search tab provides very sophisticated Search and Visualisation capabilities using plain Natural Language statements.
- The Natural Language Wizard tab provides Search and Visualisation capabilities using a semantically driven, guided approach.
- The Settings tab provides a variety of customisation options
- The Entities Mapping tab displays identified entities and their mapping to local lookups/queries.

## Troubleshooting
This App will return an error message if the Webtools Add-on is uninstalled or the App is unable to connect to a licensed OI-Rest API

## Feedback/Support
The Shared and Custom Rest API licenses include standard support for this App. 
No official support is provided for the Trial License but please feel free to drop us an email to info@openintelligence.com.au or visit our [contact-us](https://openintelligence.com.au/contact-us) page if you have any problem, question or suggestion.

## Disclaimer
This App is released under the [GNU GENERAL PUBLIC LICENSE](https://www.gnu.org/licenses/gpl-3.0.html) and is provided on an “as is” and “as available” basis. 
Open Intelligence does not give any warranties, whether express or implied, as to the suitability or usability of the App beyond the ones included in any valid Rest API Licenses assigned to you.
