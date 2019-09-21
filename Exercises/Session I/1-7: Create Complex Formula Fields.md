# 1-7: Create Complex Formula Fields

Create custom Formula field that calculates the Course Cancellation Rate

## Tasks:
- Add Fields using setup menu


## Instructions:
1. Use the setup menu to add a new Formula on the Course Object
   - __Label:__ Course Cancellation Rate
   - __Field Name:__ Course_Cancellation_Rate
   - __Type:__ Formula(Percent), Decimal 2
   - __Formula:__ ```IF((Number_of_Courses_Cancelled__c + Number_Of_Courses_Delivered__c) > 0 , Number_Of_Courses_Cancelled__c / (Number_Of_Courses_Cancelled__c + Number_Of_Courses_Delivered__c), null)```
3. Confirm the Page Layout
