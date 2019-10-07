
# 2-1: Create a Workflow Rule

Create custom Workflow Rules

## Tasks:
- Create a class invoke the class from the developer console

## Instructions:
1. Use the developer console to create a new apex class
Public class ContactManager{

public static ID addContact(String lastNameToInsert, String firstNameToInsert)
{
Contact contactToAdd= new Contact(firstname=firstNameToInsert, 
        lastName=lastNameToInsert);
insert contactToAdd;
return ContactToADD.Id;
}
}
