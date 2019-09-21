# 1-5: Creating Formula Fields

Create custom formula fields on the Class object.

## Tasks:
- Add Fields using setup menu


## Instructions:
1. Use the setup menu to add a new Formula field that calculate the End Time of a Class
   - __Label:__ End time
   - __Field Name:__ End_Time
   - __Type:__ Time
   - __Formula:__ ```Start_Time + Course__r.Session_Length__c```
2. Use the setup menu to add a new Formula Field to the Class  Object
   - __Label:__ End Date
   - __Field Name:__ End_Date
   - __Type:__ Date
   - __Formula:__ Calculate the End Date Based on the Course’s Session and Session Frequency
3. Confirm the Page Layout
