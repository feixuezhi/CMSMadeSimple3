****Exploit Title: CMS Made Simple Version: 2.2.21 - Stored XSS****

**Date: 2025-05-12**

**Exploit Author: feixuezhi**

**Vendor Homepage: https://www.cmsmadesimple.org/**

**Version: 2.2.21**

**Tested on: https://softaculous.com/demos/cms_made_simple**

**Description: **

Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting') vulnerability in CMS Made Simple Version 2.2.21 allows Stored XSS. This vulnerability resides in the Design Manager module of the admin panel. Specifically, the issue arises due to inadequate sanitization of user input in the "Template Types/Prototypes" field.

**Steps to Reproduce:**

1) Log in as admin and navigate to Layout > Design Manager > Template Types/Prototypes.
2) Click on "Search::Search Results line  Edit" button
3) Click on "Description"
4) In "Description" field, input payload ji</textarea> <img/src=1 onerror=alert(document.cookie)>//
5) Click "Submit"
6) After submitting, payload will be executed every time we click on "Search::Search Results line Edit" button.

**Notes:**

* This exploit confirms the presence of XSS vulnerability in.
* The payloads are utilized to evaluate expressions and verify the XSS.
* Use responsibly and with proper authorization; unauthorized use of this exploit may lead to legal consequences.
