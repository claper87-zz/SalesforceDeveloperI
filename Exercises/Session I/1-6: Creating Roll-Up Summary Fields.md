# 1-6: Creating Roll-Up Summary Fields

Create custom Roll-Up Summary fields on the Course object.

## Tasks:
- Create a Roll-Up to count Total Number of Classes
- Create a Roll-Up to count Number of Cancelled Classes
- Create a Roll-Up to count Number of Delivered Classes
- Create a Roll-Up to calculate when the Last Class will start


## Instructions:
1. Use the setup menu to add a new Roll-Up Summary that counts the Total Number Of Classes
   - __Label:__ Total Number of Classes
   - __Field Name:__ Total_Number_of_Classes
   - __Type:__ Roll-Up
   - __Summary Type:__ Count
   - __Filter:__ N/A
2. Use the setup menu to add a new Roll-Up Summary that counts Number of Cancelled Classes
   - __Label:__ Number of Cancelled Classes
   - __Field Name:__ Number_of_Cancelled_Classes
   - __Type:__ Roll-Up
   - __Summary Type:__ Count
   - __Filter:__ ```Status = Cancelled```
3. Use the setup menu to add a new Roll-Up Summary that counts Number of Delivered Classes
   - __Label:__ Number of Delivered Classes
   - __Field Name:__ Number_of_Delivered_Classes
   - __Type:__ Roll-Up
   - __Summary Type:__ Count
   - __Filter:__ ```Status = Delivered```
4. Use the setup menu to add a new Roll-Up Summary to calculate when the Last Class will start
   - __Label:__ Last Class Start Date
   - __Field Name:__ Last_Class_Start_Date
   - __Type:__ Roll-Up
   - __Summary Type:__ MAX(Start_Date)
   - __Filter:__ ```Status = Planned```
