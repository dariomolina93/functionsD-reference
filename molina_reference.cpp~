// Name: Dario Molina
/* 10/15/15
Description: Write and implement the functions with the given conditions
*/
#include<iostream>
#include<string>
#include<cassert>
#include <iomanip>
#include <locale>
#include <sstream>
#include<cmath>
using namespace std;

void sort( int numA, int numB, int numC, int& numD, int& numE, int& numF);//Function which sorts three numbers in increasing order. Values passed in from ( 0 to 100)

void numDigits( int valA, int& numC);// Function which determnes thenumber of digits  in an integer from (-1000 to 1000)

void computeSphere( double& a, double& v, double r);//Write a functions which calcultes area, volume. The values passed in should be double values greater 0  and less than 1000)

void swap( int& A, int& B, int C, int D);// Write a function which swaps  the entered values. the values passed in should be positive.

int main() 
{
  int numD = 0, numE = 0, numF = 0, numC, A, B, C, D;
  double a,v;
  
  cout.setf(ios::showpoint);
  cout.setf(ios::fixed);
  cout.precision(2);
  
 sort(  99,100,-1, numD, numE, numF);// 1st function and its results;
 cout <<" First number = " <<numD << "\n"
      <<" Second number = " <<numE << "\n"
      <<" Third number = " <<  numF << endl << endl;
      
 numDigits( 1000, numC);// 2nd function and its results;
 cout << " The length of the number is " << numC <<  " digits." << endl <<endl;
 
 computeSphere( a, v, 1);// 3rd functin and its results;
 
 cout <<"Area = " << a << "\n"
      <<"Volume = " << v << "\n" << endl;
      
  swap( A, B, 5, 10);// 4rth function and its results;
  
  cout << " Before it was 5 and 10, \n"
       << " Now its " << A << " and " << B << "." << endl;
 
return 0;
}

void sort( int numA, int numB, int numC, int& numD, int& numE, int& numF)//Function which sorts three numbers in increasing order. Values passed in from ( 0 to 100)
{
  int num_A = numA;// i had done abs(numA) but once i finished the program i realized it wasnt only positive number but from 0 to 100
  int num_B = numB;
  int num_C = numC;// That's why i have stored these in other variables
  
 if((num_A >= 0) && (num_B >= 0) && (num_C >=0) && (num_A <= 100) && (num_B <= 100) && (num_C <= 100)   )// make sure each number is between 0 and 100 inclusive.
 {
 // There are 19 if-statements  that check every possible outcome that gives us the desired outcome.
   if ( (num_A == num_C) && (num_A < num_B))
    {
      numE = num_A;
      numF = num_A;
    }  
  
   if(( num_A == num_C) && (num_A > num_B))
   {
     numD = num_A;
     numE = num_A;
   }  
  
   if( (num_A == num_B) && (numB == num_C))
   {
     numD = num_A;
     numE = num_A;
     numF = num_A;
   } 
  
   if ( (num_A == num_B) && num_A > num_C)
   {
     numD = num_A;
     numE = num_A;
   } 
    if (( num_B == num_C) && num_B > num_A)
    {
      numD = num_B;
      numE = num_B;
    }  
    if (( num_A == num_B) && num_A < num_C)
    {
      numE = num_A;
      numF = num_A;
    }
    
    if(( num_B == num_C) && num_B < num_A)
    {
      numE = num_B;
      numF = num_B;
    }
   if (( num_A > num_B) && (num_A > num_C))
    {
     numD = num_A;
    }
   if ( num_A > num_B && num_A < num_C)
     {
       numE = num_A;
     }
   if (( num_A < num_B) && (num_A > num_C))
     {
      numE = num_A;
     }
   if (( num_A < num_C) && ( num_A < num_B))
     {
      numF = num_A;
     }
   if ((num_B > num_A) && (num_B > num_C))
     { 
      numD = num_B;
     }
   if (( num_B > num_A) && (num_B < num_C))
     {
      numE = num_B;
     }
   if ( num_B < num_A && num_B > num_C)
      {
        numE = num_B;
      }
   if (( num_B < num_A) && (num_B < num_C))
     {
      numF = num_B;
     }
   if (( num_C > num_A) && (num_C > num_B))
     {
      numD = num_C;
     }
   if ( num_C > num_A && num_C < num_B)
     {
       numE = num_C;
     }
   if (( num_C < num_A) && (num_B < num_C))
     {
      numE = num_C;
     }
   if (( num_C < num_A) && (num_C < num_B))
     {
      numF = num_C;
     }
 }
 
 else
   {// if one number doesn't meet the criteria -1 is given for all three pass by reference values.
     numD = -1;
     numE = -1;
     numF = -1;
   }
         
  return; 
}

void numDigits( int valA, int& numC)// Function which determnes thenumber of digits  in an integer from (-1000 to 1000)
{
  
  string digits = static_cast<ostringstream*>( &(ostringstream() << valA) )->str();// turn the integer into a string to count how many digits with a for loop.
  
 if( valA >=0 && valA <= 1000)// check to see if number is postive
 {  
  int count = 0;
  
  for( int i = 0; i < digits.length(); i++)// go through each number
   {
     count++;// increase count for the length of string.
   }
   
   numC = count;
 }
 
 else if ( valA >= -1000 && valA < 0 )//if number is negative, i used a separate for loop to substract the negative sign so it doesn't count as a number when the loop does its iteration.
   {  
  int count = 0;
  
  for( int i = 0; i < digits.length()-1; i++)
   {
     count++;
   }
   
   numC = count;// same process as the previos if statement
 }

 
 else// if number is out of bounds -1 is returned.
   numC = -1;
   
 return;
}
void computeSphere( double& a, double& v, double r)//Write a functions which calcultes area, volume. The values passed in should be double values greater 0  and less than 1000)
{
  const double PI = 3.14159;
  const double ratio = 4.0 / 3.0;
  a = 4 * PI * r * r;
  
  v = ratio * PI * pow( r, 3);// power function makes it easier to do the calculation

  return;
}


void swap( int& A, int& B, int C, int D)// Write a function which swaps  the entered values. the values passed in should be positive.
{
  int bucket;// create a new variable as a place holder;
  
  A = C;
  B = D;
  
  bucket = A;// swaping of integers
  A = B;
  B = bucket;
 
 return;
}
