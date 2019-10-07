Public Class ContactManager{
        public static ID addContact(String lastNameToInsert, String firstNameToInsert)
        {
                Contact contactToAdd= new Contact(firstname=firstNameToInsert, 
                                          lastName=lastNameToInsert)
                insert contactToAdd;
                return ContactToADD.Id;
        }
}

