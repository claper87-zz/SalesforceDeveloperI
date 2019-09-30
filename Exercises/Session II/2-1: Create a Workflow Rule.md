# 2-1: Create a Workflow Rule

Create custom Workflow Rules

## Tasks:
- Create a new Field Called Student Email on the Step Attempt object
- Create an Email Template
- Create a Workflow Rule on the Step_Attempt object
- Create an Immediate Email Alert Workflow Action
- Create an Immediate Field Update Workflow Action



## Instructions:
1. Use the steup menu to add a new Email Field on the Step_Attempt Object
   - __Label:__ Student Email
   - __Field Name:__ Student_Email
   - __Type:__ Email
2. Use the steup menu to create a new Email Template
   - __Type:__ Custom
   - __Available for Use:__ true
   - __Email Template Name:__ Step Attempt Registration Confirmation
   - __Subject:__ ```You have been Registered for {!Step_Attempt__c.Certification_Step__c}```
   - __Email Body:__ ```Hi,<br/> <p>You have been registered to take {!Step_Attempt__c.Certification_Step__c} on {!Step_Attempt__c.Date_Registered__c}.</p> <p>Regards,<br/> CourseWare Management</p>```
2.1  Clone the newly Created Email Template
   - __Type:__ Custom
   - __Available for Use:__ true
   - __Email Template Name:__ Step Attempt Reminder
   - __Subject:__ ```Your examination for {!Step_Attempt__c.Certification_Step__c} is coming up```
   - __Email Body:__ ```Hi,<br/> <p>On your upcoming examination {!Step_Attempt__c.Certification_Step__c} is due on {!Step_Attempt__c.Date_Registered__c} .</p> <p>Regards,<br/> CourseWare Management</p>```
3. Use the setup menu to add a new Workflow Rule on the Stemp_Attempt Object
   - __Object:__ Step Attempt
   - __Rule Name:__  Registration Actions
   - __Description:__ Handle all actions related to registration
   - __Evaluation Criteria:__ ```created ```
   - __Rule Criteria:__ Criteria are met |  Step Attempt: Step Attemp  :: not equal to :: blank
4. Create an Immediate Workflow Action
   - __Type:__ Email Alert
   - __Description:__ Sends Step Attempt Registration Email
   - __Email Template:__ ```Step Attempt Registration ```
   - __Recipient Type:__ Email Field :: Student Email
5. Create an Immediate Workflow Action
   - __Type:__ Field Update
   - __Description:__ Updates Step Attempt Student Email
   - __Specify New Field Value:__ Use a formula to set the new value
   - __Formula:__ ``` Student__r.Contact__r.Email ```
6. Create an Time-Dependent Workflow Action
   - __Time Trigger Edit:__ 5 days before Date Registered
   - __Type:__ Email Alert
   - __Description:__ Send Step Attempt Remainder Email
   - __Email Template:__ ```Stept Attempt Reminder ```
   - __Recipient Type:__ Email Field :: Student Email


