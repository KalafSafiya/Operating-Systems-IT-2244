```
1.
#include <stdio.h>

int main() {
  printf("Hello World!\n");
  return 0;
}

# save as first.c
gcc first.c -o first
./first

output:
[2021ict71@fedora ~]$ ./first
Hello World!

explanation:
#include <stdio.h>        → Includes Standard I/O library.
int main() {}             → Main function (entry point).
printf("...")             → Prints the string.
return 0;                 → Ends the program successfully.


2.
#include <stdio.h>

int main() {
  int age=25;
  printf(age); //incorrect
  printf("%d",age);
  return 0;
}

output:
[2021ict71@fedora ~]$ ./secondc
25[2021ict71@fedora ~]$

explanation:
printf(age);     → Incorrect (no format string).
printf("%d",age) → Correct – prints integer.


##############################
%d / %i → integers  
%f / %F → floats  
%lf     → double  
%s      → string  
%c      → character
##############################


3.
#include <stdio.h>

int main() {
  int age=25;
  printf("%d",age);
  printf("\nc programming");
  age=31;
  printf("\nNew age:%d",age);
  return 0;
}

output:
[2021ict71@fedora ~]$ ./third
25
c programming
New age:31[2021ict71@fedora ~]$


3. (duplicate label, actually 4th)
#include <stdio.h>

int main(){
  int firstNumber=25;
  int secondNumber=firstNumber;
  printf("Second Number:%d",secondNumber);
  return 0;
}

output:
[2021ict71@fedora ~]$ ./first3
Second Number:25[2021ict71@fedora ~]$

explanation:
Copies firstNumber to secondNumber and prints it.


4.
#include <stdio.h>

int main(){
  int firstNumber, secondNumber=36;
  printf("First Number:%d",firstNumber);  // uninitialized
  printf("Second Number:%d",secondNumber);
  return 0;
}

output:
[2021ict71@fedora ~]$ ./first4
First Number:1Second Number:36[2021ict71@fedora ~]$

explanation:
Only secondNumber is initialized. firstNumber has garbage value.

# variable naming rules:
# - no spaces
# - cannot start with a number


5.
#include <stdio.h>

int main(){
  int age=10;
  printf("%d", age);
  printf("size : %zu", sizeof(age));
  return 0;
}

output:
[2021ict71@fedora ~]$ ./first5
10size : 4[2021ict71@fedora ~]$

explanation:
%zu → format specifier for `sizeof`.  
int is usually 4 bytes.


6.
#include <stdio.h>

int main(){
  // double
  double height = 12.45;
  printf("%lf\n", height);
  printf("%.2lf\n", height);
  printf("size of double : %zu\n", sizeof(height));

  // float
  float num2 = 10.9f;
  printf("%.1f\n", num2);
  printf("size of float: %zu\n", sizeof(num2));

  // char
  char character = 'z';
  printf("%c\n", character);
  printf("%d\n", character); // ASCII value
  printf("size of char: %zu\n", sizeof(character));

  return 0;
}

output:
[2021ict71@fedora ~]$ ./first8
12.450000
12.45
size of double : 8
10.9
size of float: 4
z
122
size of char: 1


7. // user input
#include <stdio.h>

int main(){
  int age;
  printf("Enter the age:");
  scanf("%d", &age);  // & → address of variable
  printf("\nAge: %d", age);
  return 0;
}

output:
[2021ict71@fedora ~]$ ./first9
Enter the age:23

Age: 23[2021ict71@fedora ~]$


8.
#include <stdio.h>

int main(){
  double height;
  printf("Enter the height:");
  scanf("%lf", &height);
  printf("Height: %.2lf\n", height);
  return 0;
}

output:
[2021ict71@fedora ~]$ ./first10
Enter the height:155.67
Height: 155.67


9.
#include <stdio.h>

int main(){
  float number;
  char character;

  printf("Enter a float value:");
  scanf("%f", &number);
  printf("Float number: %f\n", number);

  printf("Enter a character:");
  scanf(" %c", &character);  // notice space before %c
  printf("Character is:%c\n", character);

  return 0;
}

output:
[2021ict71@fedora ~]$ ./first11
Enter a float value:45.67
Float number: 45.669998
Enter a character:y
Character is:y


10. // take multiple inputs together
#include <stdio.h>

int main(){
  double num;
  char alpha;
  printf("Enter inputs:");
  scanf("%lf %c", &num, &alpha);
  printf("First input: %lf\n", num);
  printf("Second input: %c\n", alpha);
  return 0;
}

output:
[2021ict71@fedora ~]$ ./first12
Enter inputs:99.5 G
First input: 99.500000
Second input: G


################# COMMENTS #################
Single-line comment: // (Ctrl + /)
Multi-line comment: /* */ (Ctrl + Shift + /)


11. ################ C Operators
#include <stdio.h>

int main(){
  int num1, num2;
  printf("Enter num1:");
  scanf("%d", &num1);
  printf("Enter num2:");
  scanf("%d", &num2);

  int sum = num1 + num2;
  int sub = num1 - num2;
  int mul = num1 * num2;
  float div = (float)num1 / num2;

  printf("Summation of %d + %d: %d\n", num1, num2, sum);
  printf("Subtraction of %d - %d: %d\n", num1, num2, sub);
  printf("Multiplication of %d * %d: %d\n", num1, num2, mul);
  printf("Division of %d / %d: %.2f\n", num1, num2, div);

  return 0;
}

output:
[2021ict71@fedora ~]$ ./first13
Enter num1:4
Enter num2:3
Summation of 4 + 3: 7
Subtraction of 4 - 3: 1
Multiplication of 4 * 3: 12
Division of 4 / 3: 1.33

