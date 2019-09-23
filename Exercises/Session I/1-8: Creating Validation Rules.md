# 1-8: Creating Validation Rules

Create custom Validation Rules

## Tasks:
- Create a Validation Rule on the Class Object


## Instructions:
1. Use the setup menu to add a new Validation Rule on the Class Object
   - __Rule Name:__ Class-001 Start Date Not in the Past
   - __Active:__ true
   - __Description:__ Prevents a record from saving if The Start Date is in the Past
   - __Error Condition Formula:__ ```Start_Date__c <  TODAY() ```
   - __Description:__ The Start Date value must  set to Today's date or a future date
   - __Error Location:__ Field (Start_Date)
 2. Verify the new validation
