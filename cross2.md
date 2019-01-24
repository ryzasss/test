Postmortem (incident \#AESEDI-53447)
====================================

Date
----

2019-01-24

Authors
-------

-   Julius Bernotas

Status
------

Resolved

Summary
-------

AES CIS service issue impacted AES EDI data transaction.

A Jira issue (AESEDI-53447) was logged that the customer data was not
sent from AES EDI. 486,000 records were affected. The investigation
showed that the file with the data was sent, but it did not get
processed due to an issue with the AES CIS service (Jira Issue No:
AESCIS-38263) at that point of time. The same issue affected EDI to CIS
monitoring service working on the CIS side. So the missed records were
not discovered automatically. The file was resent and the issue got
resolved. The missing records were discovered at 11:56 AM, processed at
1:00 PM

Impact
------

Estimated 486,000 records were affected, no revenue impact.

Root Causes
-----------

AES CIS service (Jira No: AESCIS-38263) issue resulted in 486,000
records loss by customer from AES EDI. This has also affected EDI to CIS
monitoring service working on the CIS side and missed records were not
discovered automatically.

Trigger
-------

Did not get processed due to an issue with the AES CIS service.

Resolution
----------

The file was resent and the issue got resolved at 1:00 PM.

Detection
---------

The missing records were discovered at 11:56 AM, A Jira issue
(AESEDI-53447) was logged that the customer data was not sent from AES
EDI.

Action Items
------------

Insure that CIS monitoring service wouldn't miss records.
