// Author: Muhammad Asad Naveed
// U.No.: 3035957848
// Assignment 2 Question 4
// Description: Write a C program to determine if an input string of digits is a valid code. Luhn algorithm

#include <stdio.h>
#include <string.h>
#include <ctype.h>
#include <stdlib.h>


void reversenumbers (char digits [30])   //function to reverse the input char
{
  int j=0;  
  char strnum[30];
  char revduplicate[30];
  strcpy(strnum,digits);

  int length = strlen(strnum);

  int x=(length-1);                      //refereing to the last char


  for (int i=0;i<strlen(digits);i++){
    digits[x] = strnum[i];
    x--;                                  
  }

    
}

int sumofodd_digits(char digits[30])        //function for sum of odd digits
{

  

    int sumofodd=0;
    for(int i=0; i<strlen(digits); i+=2)
    {
        sumofodd += digits[i]-'0';       //for converting to iteger

    }


    return sumofodd;

}

int sumofeven_digits( char digits[30])   //thi function first multiplies by 2 if output less then 10 it add the sum of the indiviidual integer
{
    int temporary;
    int sumofeven=0;
    for(int i=1; i<strlen(digits); i+=2)
    {
        temporary = (digits[i]-'0')*2;
        
        if(temporary<10)
        {
            sumofeven+=temporary;
        }
        
        else                              //if greater then 10
        {
            char array[30];

            sprintf(array, "%d", temporary);            //sprintf function is useful to convert a integer into string

     
            sumofeven+= ((array[0]-'0')+(array[1]-'0'));    //-0 for converting back to intger
            

        }
    }


    return sumofeven;

}



int main()
{
    char digits[30];

    scanf("%s", digits);          //takes input

    reversenumbers(digits);

    printf("%s\n", digits);         //prints the reversed output

    int sum_of_odd_S1= sumofodd_digits(digits);

    int sum_of_even_S2= sumofeven_digits(digits);

    printf("%d%s%d\n", sum_of_odd_S1 , " " , sum_of_even_S2);

    if((sum_of_odd_S1 +sum_of_even_S2)%10==0)
    {
        printf("valid\n");
    }
    else
    {
        printf("invalid\n");
    }
    

    return 0;

}
