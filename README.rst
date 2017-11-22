***********************
cinq-auditor-cloudtrail
***********************

===========
Description
===========

This auditor ensures that CloudTrail is enabled and logging to a 
central location and that SNS/SQS notifications are enabled and being 
sent to the correct queues for the CloudTrail Logs application.

=====================
Configuration Options
=====================

+------------------+----------------+--------+-----------------------------------------------------------------------------------------------------------+
| Option name      | Default Value  | Type   | Description                                                                                               |
+==================+================+========+===========================================================================================================+
| enabled          | False          | bool   | Enable the Cloudtrail auditor                                                                             |
+------------------+----------------+--------+-----------------------------------------------------------------------------------------------------------+
| interval         | 60             | int    | Run frequency in minutes                                                                                  |
+------------------+----------------+--------+-----------------------------------------------------------------------------------------------------------+
| bucket_account   | CHANGE ME      | string | Name of the account (must exist) in which to create the S3 bucket where CloudTrail logs will be delivered |
+------------------+----------------+--------+-----------------------------------------------------------------------------------------------------------+
| bucket_name      | CHANGE ME      | string | Name of the S3 bucket to send CloudTrail logs to                                                          |
+------------------+----------------+--------+-----------------------------------------------------------------------------------------------------------+
| bucket_region    | us-west-2      | string | Region where to enable global events logging                                                              |
+------------------+----------------+--------+-----------------------------------------------------------------------------------------------------------+
| sns_topic_name   | CHANGE ME      | string | Name of the SNS topic for CloudTrail log delivery                                                         |
+------------------+----------------+--------+-----------------------------------------------------------------------------------------------------------+
| sqs_queue_account| CHANGE ME      | string | Name of the account (must exist) which owns the SQS queue for CloudTrail log delivery notifications       |
+------------------+----------------+--------+-----------------------------------------------------------------------------------------------------------+
| sqs_queue_name   | SET ME         | string | Name of the SQS queue                                                                                     |
+------------------+----------------+--------+-----------------------------------------------------------------------------------------------------------+
| sqs_queue_region | us-west-2      | string | Region for the SQS queue                                                                                  |
+------------------+----------------+--------+-----------------------------------------------------------------------------------------------------------+
