# Pay
This program calculates the amount that will need to be paid for baseballs or candy bars and will loop depending on the users input.

// Author: Roel Cuellar
// File Name: TT10_L1_Cuellar.cpp 

#include <iostream>
#include <iomanip>
using namespace std;


int main()
{

// necessary variables
char action;
double cost, baseballs, total;
double candycost, candy, candytotal;

//Display program options
cout << "What would you like to do today? \n";
cout << "B or b will allow you to calculate the cost of baseballs purchased.\n\
C or c will allow you to calculate the money generated from candy bar sales.\n\
And Q or q will quit the program.\n \n";

do  // request for input and runs the if statements below
{      
      // request user action
      cout << "\nWhich option would you like to do? ";
      cin >> action;
      
      if ((action == 'b') || (action == 'B'))
      { 
          // Get the number of baseballs purchased
          cout << "\nHow many baseballs were purchased for the baseball team? ";
          cin >> baseballs;

          // Get the individual cost for each baseball
          cout << "How much was the individual cost per baseball? $";
          cin >> cost;
    
          // Get the total amount spent
          total = baseballs * cost;
    
          // Display the total cost
          cout << "The total cost for baseballs purchased for the team is $" \
          << total << endl;
      }

      if ((action == 'c') or (action == 'C'))
      {
          // Get the amount of candy bars sold
          cout << "\nHow many candy bars were sold? ";
          cin >> candy;
    
          // Cost per bar
          cout << "How much was each individual candy bar? $";    
          cin >> candycost;
    
          // Calculate total of money generated from sales
          candytotal = candy * candycost;
    
          //Display money received for candy bar sales
          cout << "The amount of money generated from candy bar sales is $" << \
          candytotal << endl;
      }
      
      //If statement to request new action if request is not recognized
      if ((action != 'b') && (action != 'B') && (action != 'c') &&\
      (action != 'C') && (action != 'q') && (action != 'Q'))
      {
          cout << "Oh no! You have entered an invalid command! \
          \nPlease try again.\n";
      }
          
} while ((action !='q') && (action !='Q')); // ends while loop on choosing q

//outro when user quits the program
cout << "Thanks for using the single best program on the planet!! \
Have a good day! =)\n";
     
system("pause");
return 0;

}

/*
What would you like to do today?
B or b will allow you to calculate the cost of baseballs purchased.
C or c will allow you to calculate the money generated from candy bar sales.
And Q or q will quit the program.


Which option would you like to do? 4
Oh no! You have entered an invalid command!
Please try again.

Which option would you like to do? b

How many baseballs were purchased for the baseball team? 10
How much was the individual cost per baseball? $2
The total cost for baseballs purchased for the team is $20

Which option would you like to do? c

How many candy bars were sold? 30
How much was each individual candy bar? $2
The amount of money generated from candy bar sales is $60

Which option would you like to do? q
Thanks for using the single best program on the planet!! Have a good day! =)
Press any key to continue . . .
*/
