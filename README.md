
# Event Management

This software is the software for event managing.







## My Contributions

 - [Build the Event  display Category](https://)
 - [Delete event](http://)

### 1. Category Function 

1. Made the 'displayEventsByCategory' function.

### Code - 

        void displayEventsByCategory(const string& category) const {
        bool found = false;
        cout << "---------------------------------------------" << endl;
        for (const auto& event : events) {
            if (event.category == category) {
                event.display();
                cout << "---------------------------------------------" << endl;
                found = true;
            }
        }
        if (!found) {
            cout << "No events found in the category: " << category << endl;
            cout << "---------------------------------------------" << endl;

        }
        getch();
        system("cls");
    }




 2. Explaination : 


 Made a function in the 'Event' class name 'displayEventsByCategory'. 
    Used the string library and used the STL C++ sring function to make it. 
    Used 'for loop'  to check some conditions related to display category. 
    where used the 'if' conditions two times first 'if' to check that 
    wheather the category of event exists or not and second 'if' condition 
    says that if 'found' is false then show in terminal "No events found in 
    the category". Added 'getch()' and 'system(cls)' keywords for as you click 
    'enter'  the terminal get clear.


## 2. Delete Event

  1. Made the 'deleteEvent' Function.

    

### Code - 

    void deleteEvent(const string& name) {
        for (auto it = events.begin(); it != events.end(); ++it) {
            if (it->name == name) {
                events.erase(it);
                cout << "---------------------------------------------" << endl;
                cout << "Event deleted successfully!" << endl;
                cout << "---------------------------------------------" << endl;
                getch();
                system("cls");
                return;
            }
        }
        cout << "---------------------------------------------" << endl;
        cout << "Event not found." << endl;
        cout << "---------------------------------------------" << endl;
        getch();
        system("cls");
    }


2. Explaination : 

    The function is to deleting events. Used a for-loop  in which made a iterable where itration runs from begin to end of the name-string. There is a if-condition also , if name is equal to the given name then events will erase if not , show "Event not found". that it.

    
       