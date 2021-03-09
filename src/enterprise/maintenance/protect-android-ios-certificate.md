---
summary:
---

# How OutSystems protects your Android and iOS certificates

## Overview 
With the release of OutSystems 10, OutSystems has introduced the functionality of performing builds for Android and iOS mobile applications for your OutSystems application.

In order to properly generate the mobile application so it can be submitted to the respective stores, it's necessary that you provide your own developer signing key.

This article briefly explains how this key is used and protected by OutSystems.

## Key Lifecycle 
1. The key and corresponding password are stored on your environment's database
2. When a request is made, the key and password are transmitted to the Mobile Apps Builder Service
3. The key is saved to an S3 bucket
4. The password is put on the work queue
5. When the build is being processed, the key is fetched and saved to disk
6. The password is obtained from the work queue and kept in memory to use the key
7. The key is deleted from the builder
8. The key is automatically deleted from S3 after 7 days

## How the key is protected 
At the environment level, the key and password are kept in a database table and encrypted using the environment's unique 128 bit key. In order to read the key a user has to be able to both read the database entry and access the file system to obtain this key.

When communicating to the Mobile Apps Builder Service we always use HTTPS which guarantees confidentiality in transit.

In the S3 bucket and queue service, both provided by Amazon, access to the key is protected by IAM permissions, which are only given to the assets that need to access it.

On the build machine the key is persisted in its encrypted form with a password provided by the customer. The password which allows to unlock the key is not persisted to disk.

## Who has access to the assets 
On-premises anyone with read access to the database can read the encrypted key and password, but cannot decrypt it. Your system administrator with access to the file system can access the key to decrypt this data.

In the OutSystems Cloud offer, the OutSystems Support team has access equivalent to your DBA and system administrator to your cloud environments. This access is only used for troubleshooting purposes with an associated support case opened by the customer, or in the context of a system outage.

The OutSystems Support team has access to the cloud assets supporting the Mobile Application Builder Service (S3, queue, mobile application builders). This access is only used for troubleshooting purposes with an associated support case opened by the customer, or in the context of a system outage.
