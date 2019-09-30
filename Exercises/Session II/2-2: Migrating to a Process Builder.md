# 2-1: Migrating a Workflow to a Process Builder

Create custom Process Builder, and de-activate the previously created Workflow Rule

## Tasks:
- Create a new Process Builder on the Step_Attempt object
- Re-use existing actions & templates
- De-activate the old workflow rule

## Instructions:
1. Use the setup menu to create a new Process Builder for the Step_Attempt Object
   - __Process Name:__ Step Attempt
   - __API Name:__ Step_Attempt
   - __Description:__ Executes actions when a Step Attempt Record is Created or Updated
   - __Process Startst When:__ A Record Changes
2. Add the main Object
   - __Object:__ Step Attempt
   - __Start the Process:__ Only when a record is created
3. Add a Criteria Node 
   - __Criteria Name:__ ```New Registrant```
   - __Criteria for Executing Actions:__ Formula Evaluates to true :: ```ISNEW()```
   - __Description:__ Handle all actions related to registration
   - __Evaluation Criteria:__ ```created ```
   - __Rule Criteria:__ Criteria are met |  Step Attempt: Step Attemp  :: not equal to :: blank
4. Add an Immediate  Action
   - __Type:__ Email Alert
   - __Name:__ Sends Student Registration Email
   - __Email Alert:__ ```SA001 Sends Student Registration Confirmation```
5. Create an Immediate  Action
   - __Type:__ Update Records
   - __Name:__ Update Student Email
   - __Record Type:__ Select the Step_Attempt__c record that started your process
   - __Criteria for Updating Record:__ No criteria—just update the records!
   - __Set new field values for the records you updatea:__ ```Student Email ``` Formula ```[Step_Attempt__c].Student__c.Contact__c.Email ```
6. Add an Scheduled  Action
   - __Time Trigger Edit:__ 5 days before Date Registered
   - __Type:__ Email Alert
   - __Action Name:__ Send Remainder Email
   - __Email Alert:__ ```Sends_Step_Attempt_Remainder_Email ```
7. Activate the Process Builder
8. De-activate the old Workflow


