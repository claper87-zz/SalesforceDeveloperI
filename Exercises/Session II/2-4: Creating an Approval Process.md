# 2-4: Creating an Approval Process

Create a new custom field & Email template

## Tasks:
- Create a new Approval Procces

## Instructions:
1. Use the setup menu to create a new Approval Process on Course Feedback
   - __Name:__ Contact Feedback Approval
   - __Specify Entry Criteria:__ Criteria Met :: Contact | Not Equal To | blank
   - __Specify Entry Criteria:__ Formula evaluatets to true :: ``` NOT(ISNULL(Contact__c) )```
   - __Select Approver:__ Automatically Assign Approvers :: Users => your user
2. Edit the first step of the approval
   - __Name:__ Low Rating Approval
   - __Unique Name:__ Low_Rating_Approval
   - __Specify Step Criteria:__ Enter this step if the following ```criteria are met```, else ```approve record```
   - __criteria:__ ```Rating``` less than ```3```
3. Add a Finally Approved Email Alert Action
   - __Type:__ Email Alert
   - __Description:__ Course Feedback Approved Notification
4. Add a Finally Approved Field Update Action
   - __Type:__ Field Update
   - __Name:__ Update Use for Public Content
   - __Field to Update:__ Use for Public Content
   - __Specify New Field Value:__ True
5. Activate the Process Builder




