+++++++++++++++++++++++++++
CCS Notifications - Testing
+++++++++++++++++++++++++++

Pre-Requistes
=============

* Active Python 2.7+ SDK should be installed
* MS Outlook Application should be installed & configured
* CCS Test Server should be up & running

Usage
=====

.. highlight:: bash

::

  $ driver.py [-h] [-a] [-t TESTNAME]

  -h, --help            show this help message and exit
  -a, --all             run all test cases
  -t TESTNAME,
  --testname TESTNAME   name of the test to run

Steps
=====

Data Creation in TTS Cache
--------------------------
* Create CM Ticket
* Create SM Ticket
* Create Affected Element
* Create SM Audit if RESCHEDULED Scenario

Data Creation in Couchbase Server
---------------------------------
* Create Impact Document if not exists
* Replace Impact Document if exists & different
* Create Customer Document with confiured EmailId for all accounts in Impact Document if not exists
* Replace Customer Document if exists & different

Data Creation in Notification Reporting DB
------------------------------------------
* Applicable for for RESCHEDULED/CANCELLED/COMPLETE Scenario
* Create mock Notification Data in specified previous State based on data in TTS Cache & Couchbase Server

Run CCS Notification Engine in Remote Server
--------------------------------------------
* Run Notification Engine for specified service
* SFTP log file to local
* SFTP Vendor's Phone Notifications file to local (Applicable for SMB only)

Validate Mail/Phone Notification
--------------------------------
* Validate Notification sent or not
* Check Expected vs Actual contents of Notification if sent

Validate data stored in Reporting DB
------------------------------------
* Validate Notifcation data stored in Reporting DB
* Check Expected vs Actual Notifcation data if available
