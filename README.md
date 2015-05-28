#include <stdio.h>
#include <cs50.h>

int main (void)
{
  //n = height, h = hashes, s = spaces, r = rows
  int n;
  
  do
  {
    print ("How tall would you like your pyramid?(between 1-23): ");
    n = GetInt();
  }
  while (n < 0 || n > 23);
  
  //rows
  for (int r = 0; r < n; r++) 
  {
    //spaces
    for (int s = 0; s < n - r; s++)
    {
      printf (" ");
    }
    //hashes
    for (int h = 0; h < n + r - 1; h++)
    {
      printf("#");
    }
    //new line
    printf ("\n");
  }
}
