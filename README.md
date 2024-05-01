Capitalize first and last letter of each word
Today we will learn how to code a C program on how to Capitalize first and last letter of each word of a string i.e. to convert first and last letter of each word into uppercase . We will use toupper() function in the process. The toupper() function is used to convert lowercase alphabet to uppercase.

Capitalizing first and last letter
Example
Lets take example to understand this if the input string is :- "Prep insta" we need to capitalize first and last letter of each word of a string. The output here will be "PreP InstA"
Algorithm:
Initialize the variables.
Accept the input.
Calculate the length of input.
Initialize a for loop and terminate it at the end of string. 
Convert first and last index of the string to uppercase using toupper() function.
Check for space and if space found convert the element present at index before space and after space to uppercase using the same function.
Print result. 
C programming code to capitalize the first and last letter of each word of a string
#include<stdio.h>
#include<conio.h>
#include <ctype.h>
#include<string.h>
int main() 
{
  //Initializing variables
  char str[100] = "str ing";
  int length = 0;
  
  //Calculating length.
  length = strlen(str);
  for(int i=0;i<length;i++)
  {
      if(i==0||i==(length-1)) //Converting character at first and last index to uppercase.
      {
          str[i]=toupper(str[i]);
      }
      else if(str[i]==' ') //Converting characters present before and after space to uppercase.
      {
          str[i-1]=toupper(str[i-1]);
          str[i+1]=toupper(str[i+1]);
      }
  }
  
  //Printing result.
  printf("String after capitalizing first and last letter of each word:\n%s", str);
  return 0;
}
Output
String after capitalizing first and last letter of each word:
StR InG
