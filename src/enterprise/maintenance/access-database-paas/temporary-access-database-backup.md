---
summary: Check how you can request access to a database backup on the OutSystems PaaS
---

# Temporary Access to Database Backup

The access to a database backup service is designed to help our OutSystems Cloud customers recover their production environments from unforeseen technical events, with significant business impact.

It is subject to our standard 15 days retention policy so you'll only be able to access a backup to a point in time within the last **15 days**.

Customers can extract the necessary data from a previous point in time or perform tests.


This service is available only for Production type environments hosted in the OutSystems Cloud.

## Request Temporary Access to Database Backup

To request this service contact us using any of our available channels, [here](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/01_Contact_OutSystems_technical_support).

Please include:

- the point in time of the backup you want to access, specifying the precise date and time in UTC;

- the environments' address, if you have multiple production environments;

- the business justification for this request.

OutSystems may, at its own discretion, agree or decline to provide this service, based on the business justification. OutSystems will not provide this service on a regular basis, so you should not include it in the design of your regular tasks or development processes.

## What will OutSystems deliver?

 - We will install the snapshot in a dedicated RDS database that is not connected to any OutSystems environment. This way, any operation performed in the temporary database will not impact your running production environment.
 - We will provide you with system admin credentials and the RDS database address that you can use to connect with a database client (such as SQL Server Management Studio or SQL Developer).

## For how long I’ll have access to the backup?

OutSystems will make this temporary database available for direct access by the customer for 1 week.

Upon OutSystems approval, this period can be extended when given proper justification.

 

