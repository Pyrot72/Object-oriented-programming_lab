# Object-oriented-programming_lab





=============x======================x==============================x=========================  

/*
Write the definition for a class called complex that has floating point data members for
storing real and imaginary parts. The class has the following member functions:
void set(float, float) to set the specified value in object
void disp() to display complex number object
complex sum(complex) to sum two complex numbers & return complex number
1. Write the definitions for each of the above member functions.
2. Write main function to create three complex number objects. Set the value in two objects and
call sum() to calculate sum and assign it in third object. Display all complex numbers.
*/

#include<iostream>  //incuding my header file 
using namespace std;

class complex     //class definatiom
{
   private:
              float a;        //these are private date members 
              float b;
   public:                    //below data is public date and publice member function prototypes (defined after main function)
                void set(float real, float img);         //setting real and imagenary vales protoype
                complex sum (complex);                    //this is defulat constructor prototype
                void disp();                            //Displaying the date prototypes
};

complex complex::sum(complex C)   //this is defulat constructor defnning 
{
 complex n;
 n.a = a + C.a;
 n.b = b + C.b;
 return n;
}

int main()    //start of main function 
{
          complex C1,C2,C3;       //defining class variable
          C1.set(9.5,6.1);        ////setting date by passing vale to member function
          C2.set(9.2,6.5);        //setting date by passing vale to member function
          C3=C1.sum(C2);          //setting date by passing vale to member function

          cout<<"\n 1st complex Number = ";C1.disp();       //Displaying complex number by calling function 1st time
          cout<<"\n 2nd complex Number = ";C2.disp();         //Displaying complex number by calling function 2nd time
          cout<<"\n 3rd complex Number = ";C3.disp();          //Displaying complex number by calling function 3rd time

          return 0;
} //ENd of main function

  
void complex::set(float real, float img)     //function defination to set date 
      {
        a=real; 
        b=img;
      }
void complex::disp()            //function defination to set date 
{
 cout<<a<<" + j"<<b<<endl;
}




=============x======================x==============================x=========================  
/*
Write the definition for a class called Rectangle that has floating point data members
length and width. The class has the following member functions:
void setlength(float) to set the length data member
void setwidth(float) to set the width data member
float perimeter() to calculate and return the perimeter of the rectangle
float area() to calculate and return the area of the rectangle
void show() to display the length and width of the rectangle
int sameArea(Rectangle) that has one parameter of type Rectangle. sameArea returns 1 if the
two Rectangles have the same area, and returns 0 if they don't.
1. Write the definitions for each of the above member functions.
2. Write main function to create two rectangle objects. Set the length and width of the first
rectangle to 5 and 2.5. Set the length and width of the second rectangle to 5 and 18.9. Display
each rectangle and its area and perimeter.
3. Check whether the two Rectangles have the same area and print a message indicating the
result. Set the length and width of the first rectangle to 15 and 6.3. Display each Rectangle and
its area and perimeter again. Again, check whether the two Rectangles have the same area and
print a message indicating the result.

*/

#include <iostream>
using namespace std;

class Rectangle         //class name
{
private:
    float length;        //these are privte date members
    float width;
public:             //below data is public date and publice member function prototypes (defined after main function)
    void setlength(float lenth);          //by this function we will set length
    void setwidth(float widh);           //by this function we will set width
    float perimeter();                  //by this function we will set perimeter
    float area();                       //by this function we will set area
    void show();                        //here we will show the size of length and width
    int sameArea(Rectangle);            //here we will show the two rectangales are equal  not 
};          //End of the class defination  

int main()          //Start main function 
{
    Rectangle myfirst;                  //defined class variable  
    Rectangle mysecond;                 //defined class variable
    myfirst.setlength(5);            //setting date by passing vale to member function     
    myfirst.setwidth(2.5);           //setting date by passing vale to member function
    mysecond.setlength(5);          //setting date by passing vale to member function
    mysecond.setwidth(18.9);      //setting date by passing vale to member function
    cout<<"myfirst Rectange : ";       //showing the length the width of 1st
    myfirst.show();                 //showing the legth and width of 1nd
    cout<<endl;
    cout<<"Area is :  "<< myfirst.area()<< " perimeter is : " << myfirst.perimeter() <<endl;
    cout<<endl;
    cout<<"mysecond Rectange : ";       //showing the length the width of 2st
    mysecond.show();            //showing the legth and width of 2nd
    cout<<endl;
    cout<<"Area is :  "<< mysecond.area()<< " perimeter is : " << mysecond.perimeter() <<endl;
    cout<<endl;
    if (myfirst.sameArea(mysecond))          //Comparing rectangle have the same  are are not
        cout<< "Rectangles have the same areas\n ";
    else
        cout<<" Rectangles do not have the same area\n ";
    //.......................................//same like above aetting date and comparing 
    myfirst.setlength(15);
    myfirst.setwidth(6.3);
    cout<<" myFirst Rectangle is : ";
    myfirst.show();
    cout<<endl;
    cout<<"Area is :  "<< myfirst.area()<< " perimeter is : " << myfirst.perimeter() <<endl;
    cout<<endl;
    mysecond.show();
    cout<<"Area is :  "<< mysecond.area()<< " perimeter is : " << mysecond.perimeter() <<endl;
    cout<<endl;
    cout<<endl;
    if (myfirst.sameArea(mysecond))
        cout<< "Rectangles have the same areas\n ";
    else
        cout<<" Rectangles do not have the same area\n ";
    return 0;
}        //end of the main function

void Rectangle::setlength(float lenth)            //defination of setlength member functon
{
    length =lenth;
}
void Rectangle::setwidth(float widh)      //defination of setwidth member functon
{
    width = widh;
}
float Rectangle::perimeter()          //defination of perimeter member functon
{
    return (2 * length + 2  * width);
}
float Rectangle::area()         //defination of Area member functon
{
    return length * width;
}
void Rectangle::show()         //defination of show member functon
{
    cout<<"Length is : "<<length <<" width is : "<<width;
}

int Rectangle::sameArea(Rectangle other)        //defination of sameArea member functon
{
    float areaf = length * width;
    float areas = other.length * other.width;
    if (areaf == areas)
        return 1;
    return 0;
}



=============x======================x==============================x=========================  
/*
Write a C++ program that will multiply two 2D arrays elements. Take values from user
at runtime. Note display values of 1 st , 2 nd and their resultant array.
Hints: A will be the 1 st array, B will be the 2 nd array and C will be resultant array.
Note: Follow Mathematics Matrix Multiplication Rules
Output should be like that:
Enter values for array initialization
a[0][0] =3
b[0][0] =4
a[0][1] =5
b[0][1] =34
a[0][2] =3
b[0][2] =5
a[1][0] =6
b[1][0] =7
a[1][1] =7
b[1][1] =7
a[1][2] =7
b[1][2] =6
a[2][0] =4
b[2][0] =9
a[2][1] =7
b[2][1] =5
a[2][2] =3
b[2][2] =5

Values of Array a
3 5 3
6 7 7
4 7 3
Values of Array b
4 34 5
7 7 6
9 5 5
Values of Array c (Resultant array) after multiplication of Array a and b


*/


#include <iostream>
using namespace std;
    int main(){
        int num1 ,num2,a[3][3],b[3][3],c[3][3];
        cout<<"Enter values for array intialization  "<<endl;
        for (int i = 0; i < 3; i++)
        {
            for (int j = 0; j < 3; j++)
            {
            cout<< "a[" << i <<"][" <<j<<"] =";
            cin>>num1;
            a[i][j]=num1;
            cout<< "b[" << i <<"][" <<j<<"] =";
            cin>>num2;
            b[i][j]=num2;
            c[i][j]=num1 *num2;     // multiplication and using for adding a two number 
            }
        }
        cout<<endl;
        cout<<"Vale of array a \n"<<endl;
        for (int k = 0; k < 3; k++)
        {
            for (int l = 0; l < 3; l++)
            {
            cout<<a[k][l]<<" ";
            }
            cout<<endl;        
            }
        cout<<endl;
       cout<<"Vale of array  b \n"<<endl;
        for (int m = 0; m < 3; m++)
        {
            for (int n = 0; n < 3; n++)
            {
            cout<<b[m][n]<<" ";
            }
            cout<<endl;        
            }
        cout<<endl;
        cout<<"Values of Array  c  after multiplication of Array a and b " <<endl;

        for (int p = 0; p < 3; p++)
        {
            for (int q = 0; q < 3; q++)
            {
            cout<<c[p][q]<<" ";
            }
            cout<<endl;
        }
        return 0;
    }

=============x======================x==============================x=========================  
/*
Make a calculator using if-else-if else statement which perform addition, subtraction,
multiplication, division and remainder operations. Take values and operator from user on runtime.
Use while loop for user choice. Means after performing one operation program will ask from user
“do you want to do another calculation(yes/no)?”. If user press yes then user will enter number
1, number 2 and operator for calculation and if user press no then terminate the loop.

*/

#include <iostream>
#include <math.h>

using namespace std;

int main(){


    //int a cin for number and reusult storge a ans
    int first_number , second_number ,result;

    //char operation (+ , - ,/ ,*)
    char operater, choice;

    // using a do while loop for a function
    do
    {
        //user  enter the first input in user
        cout<<"Enter the first number =  ";
        cin>>first_number;

        //user enter the second input 
        cout<<"Enter the second number = ";
        cin>>second_number;


        //user enter the operation that can work funcion 
        cout<<"Enter the operation (+ , - ,/ ,* ) =  ";
        cin>>operater;

        
        //if condition used the operation == to + the iner fuction exction
        if (operater == '+'){

            //first_number and second number add and storge in result
            result=first_number + second_number;
            cout<<"The result of Addition is  : "<<first_number<<"  +  "<<second_number << "  =  " <<result<<endl;
        }
        
        
        // else if condition and also same work to cheak in function operation == - the function was work.
        else if (operater == '-')
            {
                //first_number subraction second_number and storge in result 
                result = first_number - second_number;
                cout<<"The result of Subraction is : "<<first_number<<"  -  "<<second_number << "  = " <<result<<endl;
            }

        //also same conditional operation == / the function can work   
        else if (operater == '/')
            {
                //if condition for the second number == 0 the  function was not work other wiashe alse condition
                if (second_number == 0)
                {
                    
                    cout<<"The number was not  divided by 0   = " <<second_number<<endl;
                }

                // if condition flase they ex in alse condition  
                else{

                    //first_number divide second_number and storge in result
                    result = first_number / second_number;
                    cout<<"The result  of divide is : "<<first_number<<"  /  "<<second_number << "  =  " <<result<<endl;
                }
            } 
        
        ////also same conditional operation == * the function can work 
        else if (operater == '*')
        
        {
            //first_number multiplication second_number and storge in result
            result= first_number * second_number;
            cout<<"The result of multiplication is : "<<first_number<<"  *  "<<second_number << "  =  " <<result<<endl;
        }


        //else the operation was worrge , thay can no work any fuction
        else {
            
            //cout the worry operation in output
            cout<<"You get a worry input in operation in fuctoin : " <<operater<<endl;
            cout<<"agina try = "<<operater<<endl;
        }

        // using agina start a function  y /n
        cout << "Do you want to do another calculation? (y/n)> ";

        //enter you choose please
        cin >> choice;

     //while you choose    
    }while(choice != 'n' && choice != 'N');
    return 0;
}

=============x======================x==============================x=========================  
/*
In a company, there are deductions from the salary of the employees for a fund. The deductions
rules are as follows:
• If salary is less than Rs.10,000 then no deduction
• If salary is equal to or more than Rs.10,000 and less than Rs.20,000 then deduct Rs.1,000
as fund
• If salary is equal to or more than 20,000 then deduct 7 % of the salary for fund
• Input salary from user and after appropriate deduction show the net payable amount.

*/


#include<iostream>
#include<math.h>

using namespace std;

int main()
{   
    //decdecle a verbile 
    float  salary,deductions ,taxes;
    
    //user enter the number 
    cout<<"Enter the Salary = ";
    cin>>salary;

    //using a if else-if  else loop 
    //if salary are less than or equal to 10000 they no taxes
    if (salary <= 10000)
    {
        //cout the salary
        cout <<"They are no deductions = "<<salary<<endl;
    }

    //using a else-if stamment
    //if salary a less than 20000 they are substartion a 1000 for salary
    else if (salary <=20000 )
    {
        //substarion to salary 1000 
        salary=  salary - 1000;
        cout<<"The  deductions  are subsartion in salary = "<<salary<<endl;
    }

    //using a else-if condition if number equal or great than 20000 they are substarion 7% in total salary 
    else if (salary >= 20000 || salary == 20000)
    {
        //salary/ 100  and storge in taxe
        taxes =salary/100;

        //taxes * 7% of taxes and substarion in salary and storge in ans is deductions
        deductions = salary - (taxes*7);
        cout<<"The tatal monye is remaine is  :-  "<<deductions<<endl;
    }


    //after all function is false the are run in else
    else 
    {
        cout<<"The are invidie number :- "<<salary<<endl;
    }
    
    return 0;
    
}
=============x======================x==============================x=========================  
/*
Write a program in C++ that ask a user to enter radius and calculate the volume of a
sphere. After calculating the volume, print the output on screen.
v=4/3(π r^3)

Take values from user at runtime using cin
*/

#include<iostream>
#include<math.h>

using namespace std;
int main()
{
    // float charatare
    float radius,volume;
    float pi = 3.14;
    float divide = (4/3);
    
    //user enter the number of radius
    cout<<"Enter the radius vale   =";
    cin>>radius;


    //same work find a volume and storge in volume
    //volume= divide*pi*radius*radius*radius;
    // volume= (4/3*pi*(radius*radius*radius));

	volume = divide*(pi*(radius*radius*radius));

    //print the output of volume 
    cout<<"The volume is = "<<volume<<endl;
    return 0;
}
=============x======================x==============================x=========================  

/*
Write a program to combine two strings by using pointers?
*/

#include<iostream>
using namespace std;

int main(){
    //sting varbile 
    string firststr,secondstr,*firstp,*secondp;
    //combine a two string 
    firstp =&firststr;
    secondp =&secondstr;
    //using enter 
    cout<<"Enter the first str : ";
    cin>>firststr;

    cout<<"Enter the second str : ";
    cin>>secondstr;
    //first + second add 
    cout<<"Comcationantion of string = "<<*firstp+*secondp<<endl;
return 0;
}

=============x======================x==============================x=========================  
/*
Write a program to copy one string to another string by using pointers?
*/

#include<iostream>
using namespace std;
int main(){
    char text1[100], text2[100];
    char *str1= text1;
    char *str2= text2;
    //inputting string form user
    cout<<"Enter any string : ";
    cin>>str1;
    //iterating though last element of string
    while (*(str1) !='\0')
    {
        *str2++ = *str1++;
        *str2='\0';
    }
    cout<<"Copy of "<<text1 <<" is : " <<text2<<endl;
    return 0;
}


=============x======================x==============================x=========================  
/*
Write a program to find out the length of string by using pointers?
*/

#include <iostream>
using namespace std;
int main(){
    //array
    char text[100];
    char *strArray =text;
    
    //count a world whloe
    int count= 0;

    //using enter the number 
    cout<<"Enter the string please : ";
    cin>>text;

    //using a while loop to count a text
    while (*(strArray++)!='\0')
    {
        count++;
    }
    //print the length
    cout<<"Length of string is :  "<<count<<endl;

    return 0;
}

=============x======================x==============================x=========================  


/* 
Q No.1: Define a class TEST in C++ with following description:
Private Members
TestCode of type integer
Description of type string
NoCandidate of type integer
CenterReqd (number of centers required) of type integer
A member function CALCNTR() to calculate and return the number of centers as
(NoCandidates/100+1)
Public Members
A function SCHEDULE() to allow user to enter values for TestCode, Description,
NoCandidate & call function CALCNTR() to calculate the number of Centres.
A function DISPTEST() to allow user to view the content of all the data members.
*/

#include <iostream>
using namespace std;
class TEST
						//CLASS DECLARATION
{
private:
	//DEFINING PRIVATE MEMBERS
	int TestCode;
	string Description;
	int NoCandidates;
	int CALCNTR()
	
{
	return (NoCandidates / 100 + 1);
}
public:
	void SCHEDULE();
	void DISPTEST();
	//char ch;

}; 					//function protypes
void TEST::SCHEDULE()
				//MEMBER FUNCTION OUTSIDE CLASS
{
	
	//char ch;
	
	cout<<"\nEnter you subject code name and Candidate "<<endl;

	cout << "Enter TestCode: ";
	cin >> TestCode;
	//Taking input
	cout << "Enter Description: ";
	cin.ignore();
	//Taking input
	getline(cin, Description);
	cout << "Enter No of Candidate: ";
	cin >> NoCandidates; 
	//Taking input for user
	int number_of_centers = CALCNTR();
	cout<<endl;
	cout<<" RESULT "<<endl;
	cout<<endl;
	
}
void TEST ::DISPTEST()
		{
		cout << "TestCode: " << TestCode << endl;
		//Taking output
		
		cout<< "Description: " << Description << endl;
		//Taking output

		
		cout<< "No of Candidates: " << NoCandidates << endl;
		cout<< "Number of centers: " << CALCNTR() << endl;
		}

	
int main()
//Main function 
	{
	TEST TEST;
	//Making object
	TEST.SCHEDULE(); // Calling function through object
	TEST.DISPTEST(); // Calling function through object
return 0;
	}
  
  
=============x======================x==============================x=========================  
  
  /*
  Q No.2: Define a class in C++ with following description:
Private Members
A data member Flight number of type integer
A data member Destination of type string
A data member Distance of type float
A data member Fuel of type float
A member function CALFUEL() to calculate the value of Fuel as per the following
criteria
Distance Fuel
<=1000 500
more than 1000 and <=2000 1100
more than 2000 2200
Public Members
A function FEEDINFO() to allow user to enter values for Flight Number, Destination,
Distance & call function CALFUEL() to calculate the quantity of Fuel
A function SHOWINFO() to allow user to view the content of all the data members.
  
  
 */
  
  #include <iostream>
using namespace std;
class FLIGHT // Declaring Flight
	{
private: //Declaring  private members


	int Flight;
	string Destination;
	float Distance;
	float Fuel;
	int CALFUEL()
	//condition function
{
	if (Distance <= 1000)
{
return 500;
}
	else if (Distance > 1000 && Distance <= 2000)
{
return 1100;
}
	else if (Distance > 2000)
{
return 2200;
}
	}
public:
	//Declaring members function as private function
	void FEEDINFO() //members function
	cout << "Enter Flight : ";
	cin >> Flight; //user enter the vale 
	cout << "Enter Destination : ";
	cin >> Destination; ////user enter the vale 
	cout << "Enter Distance : ";
	cin >> Distance; ////user enter the vale 
	Fuel = CALFUEL();
}
void SHOWINFO() //members function to show output the data
	cout << "Flight = " << Flight << endl;
	cout << "Destinstion = " << Destination << endl;
	cout << "Distance = " << Distance << endl;
	cout << "Fuel = " << Fuel << endl;
}
};
	int main() //main function call
	{
		FLIGHT a1;
		//creating object in main function
		a1.FEEDINFO(); //Calling function through object
		a1.SHOWINFO(); //Calling function through object
	}


  
  
  
=============x======================x==============================x=========================  

  
  
 /*
  Q No.3: Define a class BOOK with the following specifications :
Private members of the class BOOK are
BOOK NO integer type
BOOKTITLE 20 characters
PRICE float (price per copy)
TOTAL_COST() A function to calculate the total cost for N number of copies where
N is passed to the function as argument.
Public members of the class BOOK are
INPUT() function to read BOOK_NO. BOOKTITLE, PRICE
PURCHASE() function to ask the user to input the number of copies to be
purchased. It invokes TOTAL_COST() and prints the total cost to be paid by the user.
Note : You are also required to give detailed function definitions.
  */
  
  
 #include<iostream>
using namespace std;
class BOOK
// Declaring class
	{
	//by defaut public member function 
	int BOOKNO;
	char BOOKTITLE[20];
	float PRICE;
	void TOTAL_COST(int N)
	{
		float tcost;
		tcost=PRICE*N;
		cout<<tcost;
}
public:
	void INPUT()
	//member function 
{
	//user input
	cout<<"Enter Book Number : ";
	cin>>BOOKNO; 
	cout<<"Enter Book Title : ";
	cin>>BOOKTITLE; 
	cout<<"Enter price per copy : ";
	cin>>PRICE; 
}
	void PURCHASE()

	//member function 
	{
	int n;
	cout<<"Enter number of copies to purchase : ";
	cin>>n;
	cout<<"Total cost is : ";
	TOTAL_COST(n);
	}
};
	int main()
	
//Main  function 
	{
	//Declaring  object
	BOOK obj;
	
	//Calling function through object
	obj.INPUT(); 
	obj.PURCHASE(); 
return 0;
}


  
 =============x======================x==============================x=========================  
/*
  Q No.4 : Define a class REPORT with the following specification:
Private members :
adno 4 digit admission number
name 20 characters
marks an array of 5 floating point values
average average marks obtained
GETAVG() a function to compute the average obtained in five subject
Public members:
READINFO() function to accept values for adno, name, marks. Invoke the
function GETAVG()
DISPLAYINFO() function to display all data members of report on the screen.
You should give function definitions. 
  */
 
  
  #include <iostream>
using namespace std;
class REPORT 
	// Declaring class
	{
	//Declaring  private members
	int adno;
	char name[20];
	float marks[5];
	float average;
	void GETAVG()
	{
average = (marks[0]+marks[1]+marks[2]+marks[3]+marks[4])/5;
}
public:
	//function protypes
	void READINFO();
	void DISPLAYINFO();
};
	void REPORT::READINFO() //Declaring members function outside the class
{
	do
	{
	cout<<"Enter 4 digit admission number : ";
	cin>>adno;
	}while(adno<999 || adno>10000);
	cout<<"Enter name : ";
	cin>>name;
	cout<<"Enter marks in "<<endl;
	for(int m=0;m<5;m++)
		{
		cout<<"Subject "<<m+1<<" : ";
		cin>>marks[m];
		};
		GETAVG();
}
	void REPORT::DISPLAYINFO() //Declaring members function outside the class
{
	cout<<"Admission number : "<<adno<<endl;
	cout<<"Name : "<<name<<endl;;
	cout<<"Marks are : "<< marks[0]<<" "<< marks[1]
	<<" "<<marks[2]<<" "<< marks[3]<<" "<< marks[4]<<endl;
	cout<<"Average : "<<average<<endl;;
	
}
int main()

//Main function
{
	REPORT obj; //Creating object of the class report

	//Calling function through object
	obj.READINFO(); 
	obj.DISPLAYINFO(); 
}

  
  
  
 
  
  =============x======================x==============================x=========================  

  /*
  
  Q No.5: Write the definition for a class called time that has hours and minutes as
integer. The class has the following member functions:
void settime(int, int) to set the specified value in object
void showtime() to display time object
time sum(time) to sum two time object & return time
1. Write the definitions for each of the above member functions.
2. Write main function to create three-time objects. Set the value in two objects and call
sum() to calculate sum and assign it in third object. Display all time objects.
  
  */
  
  
  #include <iostream>
using namespace std;
//Class time 
class time 
	{
	private: 
	//Declaring  private members
		int hours;
		int minutes;

		//public member function 
	public: 
		void settime(int h, int m)
	{
	hours = h;
	minutes = m;
}
	time sum(time);
	void showtime();
};
	times time ::sum(time TM)
{
	//function
	time t;
	t.minutes = minutes + TM.minutes;
	t.hours = t.minutes / 60;
	t.minutes = t.minutes % 60;
	t.hours += hours + TM.hours;
return t;
}
//Declaring function outside the class
	void time::showtime() 
{
	cout << hours << " hours and " << minutes << " minutes" << endl;
}
//Main function
int main() 
{
	times T1, T2, T3;
	//CREATING 3 OBJECTS OF CLASS TIME
	T1.settime(2, 45); //CALLING FUNCTION AND SETTING PARAMETERS FOR OBJECT 1
	T2.settime(3, 30); //CALLING FUNCTION AND SETTING PARAMETERS FOR OBJECT 2
	T3 = T1.sum(T2);
	cout << "\n Time 1 : ";
	T1.showtime();
	cout << "\n Time 2 : ";
	T2.showtime();
	cout << "\n Time 3 : ";
	T3.showtime();
	return 0;
}

