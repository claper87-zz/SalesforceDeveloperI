# 2-3: Prepare for the Approval Process

Create a new custom field & Email template

## Tasks:
- Create a new Custom Field on the Course Feedback Object
- Relate the Course Feedback with the Contact Object
- Create a tab for the Course Feedback Object
- Create a new Email Template & Email Alert Action

## Instructions:
1. Use the setup menu to create a new Checkbox Field on Course Feedback
   - __Label:__ Use for Public Content
   - __API Name:__ Use_for_Public_Content
   - __Description:__ N/A
2. Use the setup menu to create a new Relationship Lookup Field on Course Feedback
   - __Label:__ Contact
   - __API Name:__ Contact
   - __Description:__ N/A
3. Use the setup menu to create a tab for the Course Feedback Object
4. Use the setup menu to create a new Email Template 
   - __Type:__ Custom
   - __Email Template Name:__ Course Feedback Approved for Public Content
   - __Subject:__ Your feedback will be featured in our newsletter!
   - __HTML Body:__ ```Hi,<br/> <p>Thank you for submitting a feedback regarding {!Course_Feedback__c.Course__c}. We've reviewed your comments and will include them in our next newsletter issue.<br/><br/> <strong>Congratulations!!</strong> </p> <h4>Here is your feedback</h4><strong>Rating: </strong>{!Course_Feedback__c.Rating__c}</br><strong>Feedback:</strong><p>{!Course_Feedback__c.Feedback__c}</p>Regards,<br/>CourseWare Management ```
5. Create a new Email Alert
   - __Type:__ Email Alert
   - __Description:__ Course Feedback Approved Notification
   - __Object:__ ```Course Feedback```
   - __Email Template:__ Course Feedback Approved for Public Content
   - __Recipient Type:__ Related Contact :: Contact



