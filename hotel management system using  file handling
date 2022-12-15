//Library Management system in data structure

#include<iostream>
#include<conio.h>
using namespace std;

class library
{
    private:
        struct node
        {
            int id;
            string name, author, publisher;
            node *next_add;
        };
        public:
            node *head = NULL;
            void menu();
            void insert();
            void search();
            void update();
            void del();
            void sort();
            void show();
};

void library::menu()
    {
        p:
        system("cls");
        int choice;
        cout<<"\n\n\t\t\t===================================================";
        cout<<"\n\n\t\t\t============LIBRARY MANAGEMENT SYSTEM==============";
        cout<<"\n\n\t\t\t===================================================";
        cout<<"\n\n 1. Insert New Record";
        cout<<"\n\n 2. Search Record";
        cout<<"\n\n 3. Update Record";
        cout<<"\n\n 4. Delete Record";
        cout<<"\n\n 5. Show all Record";
        cout<<"\n\n 6. Exit";
        cout<<"\n\n Enter your Choice";
        cin>>choice;
        switch(choice)
        {
            case 1:
                insert();
                break;
            case 2:
                search();
                break;
            case 3:
                update();
                break;
               
            case 4:
                del();
                break;
            case 5:
                sort();
                show();
                break;
            case 6:
                exit(0);
            default:
                cout<<"\n\n Invalid choice. Please try again....";
        }
        getch();
        goto p;    
    }
    void library::insert()
    {
        system("cls");
        cout<<"\n\n\t\t\t===================================================";
        cout<<"\n\n\t\t\t============LIBRARY MANAGEMENT SYSTEM==============";
        cout<<"\n\n\t\t\t===================================================";
        node *new_node = new node;
        cout<<"\n\n Book ID: ";
        cin>>new_node -> id;
        cout<<"\n\n Name : ";
        cin>>new_node -> name;
        cout<<"\n\n Authtor name : ";
        cin>>new_node -> author;
        cout<<"\n\n Publisher name : ";
        cin>>new_node -> publisher;
        new_node -> next_add = NULL;
        if(head== NULL)
        {
            head = new_node;
        }
        else 
        {
            node *ptr = head;
            while(ptr -> next_add != NULL)
            {
                ptr = ptr -> next_add;
            }
            ptr -> next_add = new_node;
        }
        cout<<"\n\n\t\t\t New Book Inserted successfully";

    }
    void library::search()
    {    
        system("cls");
        int t_id,found=0;
        cout<<"\n\n\t\t\t===================================================";
        cout<<"\n\n\t\t\t============LIBRARY MANAGEMENT SYSTEM==============";
        cout<<"\n\n\t\t\t===================================================";
        if(head== NULL)
        {
            cout<<"\n\n Linked list is Empty..";
        }
        else
        {
            cout<<"\n\n Book ID : ";
            cin>>t_id;
            node *ptr = head;
            while (ptr != NULL)
            {
                if(t_id == ptr -> id)
                {
                    system("cls");
                    cout<<"\n\n\t\t\t===================================================";
                    cout<<"\n\n\t\t\t============LIBRARY MANAGEMENT SYSTEM==============";
                    cout<<"\n\n\t\t\t===================================================";
                    cout<<"\n\n Book ID : "<<ptr -> id;
                    cout<<"\n\n Book name : "<<ptr -> name;
                    cout<<"\n\n Author name : "<<ptr -> author;
                    cout<<"\n\n publisher : "<<ptr -> publisher;
                    found++;
                }
                ptr = ptr -> next_add;

            }
            if (found == 0)
            {
                cout<<"\n\n Book ID is invalid ";
            }
        }
    }

        
    void library::update()
    {
        system("cls");
        int t_id,found=0;
        cout<<"\n\n\t\t\t===================================================";
        cout<<"\n\n\t\t\t============LIBRARY MANAGEMENT SYSTEM==============";
        cout<<"\n\n\t\t\t===================================================";
        if(head== NULL)
        {
            cout<<"\n\n Linked list is Empty..";
        }
        else
        {
            cout<<"\n\n Book ID : ";
            cin>>t_id;
            node *ptr = head;
            while (ptr != NULL)
            {
                if(t_id == ptr -> id)
                {
                    system("cls");
                    cout<<"\n\n\t\t\t===================================================";
                    cout<<"\n\n\t\t\t============LIBRARY MANAGEMENT SYSTEM==============";
                    cout<<"\n\n\t\t\t===================================================";
                    cout<<"\n\n Book ID : ";
                    cin>>ptr -> id;
                    cout<<"\n\n Book name : " ;
                    cin>>ptr -> name;
                    cout<<"\n\n Author name : ";
                    cin>>ptr -> author;
                    cout<<"\n\n publisher : " ;
                    cin>>ptr -> publisher;
                    found++;
                    cout<<"\n\n\t\t\tBook Updated succesfully ";
                }
                ptr = ptr -> next_add;

            }
            if (found == 0)
            {
                cout<<"\n\n Book ID is invalid ";
            }  
        }
    }


    void library::del()
    {
        system("cls");
        int t_id,found=0;
        cout<<"\n\n\t\t\t===================================================";
        cout<<"\n\n\t\t\t============LIBRARY MANAGEMENT SYSTEM==============";
        cout<<"\n\n\t\t\t===================================================";
        if(head== NULL)
        {
            cout<<"\n\n Linked list is Empty..";
        }
        else
        {
            cout<<"\n\n Book ID : ";
            cin>>t_id;
            if(t_id == head -> id)
            {
                node *ptr = head;
                head = head -> next_add;
                delete ptr;
                cout<<"\n\n Delete book sucessfully";
                found++;
            }
            else
            {
                node *pre =head; //point to previous node
                node *ptr = head; //point to current node
                while(ptr !=NULL)
                {
                    if(t_id == ptr ->id)
                    {
                        pre -> next_add = ptr -> next_add;
                        delete ptr;
                        cout<<"\n\n Delete book sucessfully";
                        found++; 
                        break;
                    }
                    pre = ptr;
                    ptr = ptr -> next_add;
                }
            }
            if (found==0)
            {
                cout<<"\n\nbook ID is invalid"; //8:27 full code
            }
        }
    
    }
    void library::sort()
    {
        if(head == NULL)
        {
            system("cls");
            cout<<"\n\n\t\t\t===================================================";
            cout<<"\n\n\t\t\t============LIBRARY MANAGEMENT SYSTEM==============";
            cout<<"\n\n\t\t\t===================================================";
            cout<<"\n\n linked list is empty";
            getch();
            menu();
        }
        int count =0,t_id;
        string t_name,t_author,t_publisher;
        node *ptr = head;
        while(ptr !=NULL)
        {
            count++;
            ptr = ptr -> next_add;     
        }
        for(int i=1; i<=count;i++)
        {
            node *ptr =head;
            for(int j=1;j<count;j++)
            {
                if(ptr -> id > ptr -> next_add -> id)
                {
                        //save data in temp variables
                        t_id = ptr -> id;
                        t_name = ptr -> name;
                        t_author = ptr -> author;
                        t_publisher = ptr -> publisher;
                        //save data in current node
                        ptr -> id = ptr -> next_add -> id;
                        ptr -> name = ptr -> next_add -> name;
                        ptr -> author = ptr -> next_add -> author;
                        ptr -> publisher = ptr -> next_add -> publisher;
                        //save data into next node
                        ptr ->  next_add -> id = t_id;
                        ptr -> next_add -> name = t_name;
                        ptr -> next_add -> author = t_author;
                        ptr -> next_add -> publisher = t_publisher;
               }
               ptr = ptr -> next_add;
            }
        }
    }
    void library::show()
    {
        system("cls");
        cout<<"\n\n\t\t\t===================================================";
        cout<<"\n\n\t\t\t============LIBRARY MANAGEMENT SYSTEM==============";
        cout<<"\n\n\t\t\t===================================================";
            node *ptr = head;
            while (ptr != NULL)
            {
                {
                    cout<<"\n\n Book ID : "<<ptr -> id;
                    cout<<"\n\n Book name : "<<ptr -> name;
                    cout<<"\n\n Author name : "<<ptr -> author;
                    cout<<"\n\n publisher : "<<ptr -> publisher;
                    cout<<"\n\n\n ==============================";
                }
                ptr = ptr -> next_add;

            }
            
        
    }
    


 int main()
 {
    library obj;
    obj.menu();

 }
