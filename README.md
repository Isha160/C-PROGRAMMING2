# C Programming

<img src="https://contentstatic.techgig.com/photo/90325682.cms" alt="C Programming" height="350px" width="450px">

# Table of Content
- [Introduction](#Introduction)
- [Installation](#Installation)
- [System Requirement](#System-Requirement)
- [Variables, Constant and Keywords](#Variables,-Constant-and-Keywords)
- [Operators](#Operators) 
- [Control Statements & Decision Making](#Control-Statements-&-Decision-Making)
- [Pointer](#Pointer)
- [Array](#Array)
- [String](#String)

# Introduction 
* Programming- Computer programming ek medium hai jisse hum computers se communicate karte hain. Jaise insaan Hindi/English language ka use karke ek dusre se communicate karte hain, waise hi Programming ek tareeka hai jisse hum apne 
    instructions computer ko deliver karte hain unse communicate krne k liye.
* C ek sabse purani Programming languages mein se ek hai, jo Dennis Ritchie ne 1972 mein develop ki thi.

# Features 
<img src="https://techvidvan.com/tutorials/wp-content/uploads/sites/2/2021/08/Features-of-C.jpg" alt="Features" height="350px" width="350px">

# Comments in C
C language mein do tarah ke comments hote hain:
1- Single-line comment
2- Multi-line comment

### Single-line Comment
* C mein single-line comment ( // ) double forward slash se start hota hai. 
~~~
 // Ye ek single line comment hai
~~~
### Multi-line Comment
* Multi-line comment C mein forward slash aur asterisk ( /* ) se start hota hai aur asterisk aur forward slash ( */ ) par end hota hai. Jo bhi text /* aur */ ke beech mein likha hota hai, usse compiler ignore karta hai.
* Ye program mein multiple lines ko comment karne ke liye use hota hai.
  
 ~~~
 /* Hello Isha
 Are You Fine? */
~~~

# First Program in C
~~~
#include<stdio.h>
int main(){
  printf("Hello World");
  return 0;
}
~~~
Output
~~~
Hello World
~~~

# Installation
Visual Studio Code ko download karne ke liye, aapko neeche diye gaye steps ko follow karna hoga:

* Step 1:- Browser par "Download VsCode" search karo.

* Step 2:- Pehli link par click karo.<a href="https://code.visualstudio.com/download">Visual Studio Code</a>

* Step 3:- Apne Operating System ke hisaab se sahi download option select karo. Agar aap Ubuntu use kar rahe ho, to aapka download ek .deb file hoga.

<img src="https://res.cloudinary.com/omaha-code/w_768,h_502,c_fit/omaha-code-cdn/2018/12/Download-Visual-Studio-Code.png" alt="VS Code" height="350px" width="450px">

* Step 4:- VS Code download hone ke baad, Linux mein terminal open karo ya shortcut ke liye (ctrl + alt + t) press karo.

* Step 5:- System ko update hone ke liye command type karo: $ sudo apt update

* Step 7:- System update hone ke baad, Download Directory mein jao: cd ~/Downloads

* Step 8:- .deb Package ko install karne ke liye ye command type karo aur apna password enter karo: sudo dpkg -i code*.deb

* Step 9:- Agar dependencies fix karni hain to ye command run karo: sudo apt install -f

* Step 10:- VS Code ko launch karo:- Aap VS Code ko terminal mein code type karke ya application menu mein dhoondh kar open kar sakte ho.



# System Requirement
Visual Studio Code (VS Code) chalane ke liye, aapko apne system ki requirements ko ensure karna hoga. Niche di gayi requirements ko aapko meet karna hoga:

* OS: Ubuntu 14.04+, Fedora 24+, CentOS 7+
* RAM: Kam se kam 4 GB RAM (8 GB ya usse zyada recommended)
* Disk Space: 512 MB free disk space (2 GB ya usse zyada recommended)
* Processor: Pentium ya faster processor
#### Mere system ki configurations aur software versions:
* OS: Ubuntu 24.04 LTS
* RAM: 8GB
* Disk Space: 256 GB
* Processor: 11th Gen Intel Core i3
* VS Code Version: 1.91.1
* Variables, Constant and Keywords
  
# Variables
* Variables programming mein pieces of information ko store karne ke liye use hote hain.
* Ye ek tarah ke containers hote hain jo kuch data store karte hain (jaise hum rice, dal, sugar ko alag containers mein rakhte hain).
### Rules of Naming Variables
* Pehla character alphabet ya underscore(_) hona chahiye. NOTE:- Underscore ke alawa kisi special symbol ka use allowed nahi hai.
* Variables mein commas ya blanks allowed nahi hain.
* Variable names case sensitive hote hain. Jaise int STUDENT=10; aur int student=10; dono alag-alag variables hain.
#### Syntax of Declaring Variables
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20221202181339/Cvariables1.png" alt="Features" height="250px" width="550px">

#### WAP for Variables
~~~
#include <stdio.h>

int main() {
  // Alag-alag types ke variables declare karna
  int age = 25;                // Integer variable
  float height = 5.9;          // Float variable
  char initial = 'A';          // Character variable
  double salary = 50000.75;    // Double variable
  char name[] = "Alice";       // String (array of characters)

  // Variables ke values print karna
  printf("Age: %d\n", age);               // %d integers ke liye use hota hai
  printf("Height: %.1f\n", height);       // %.1f floats ke liye ek decimal place ke saath
  printf("Initial: %c\n", initial);       // %c characters ke liye
  printf("Salary: %.2f\n", salary);       // %.2f doubles ke liye do decimal places ke saath
  printf("Name: %s\n", name);             // %s strings ke liye
}
~~~
Output
~~~
Age: 25
Height: 5.9
Initial: A
Salary: 50000.75
Name: Alice
~~~
# Constant
* Constants C mein read-only variables hote hain jinke values program mein declare hone ke baad change nahi kiye jaa sakte.
* Constant ek integer, floating point, string, ya character ho sakte hain.
* C language mein const keyword ka use constant define karne ke liye hota hai.
### Syntax of Declaring Constant
~~~
const data_type var_name = value;
~~~
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20230306215927/syntax-of-constants-in-c.png" alt="Features" height="250px" width="550px">

### Constant ka Program
~~~
#include <stdio.h>
int main() {
  // Constant variables declare aur initialize karna using const keyword
  const int DAYS_IN_WEEK = 7;
  const int MONTHS_IN_YEAR = 12;
  const char GRADE = 'A';

  // Constants ke values print karna
  printf("Number of days in a week: %d\n", DAYS_IN_WEEK);
  printf("Number of months in a year: %d\n", MONTHS_IN_YEAR);
  printf("Highest grade: %c\n", GRADE);

  // Constants ko modify karne ki koshish karna compile-time error dega
  // Ye lines uncomment karne se errors aayenge
  // MONTHS_IN_YEAR = 10;
  // DAYS_IN_WEEK = 8;

  return 0;
}
~~~
Output
~~~
Number of days in a week: 7
Number of months in a year: 12
Highest grade: A
=== Code Execution Successful ===
~~~
# Keywords
* Keywords C language mein reserved words ka set hota hai jinka predefined meaning hota hai aur jo C programming likhne mein use hote hain.
* In keywords ka use identifiers ya variable names ke liye nahi ho sakta, kyunki inka ek specific function hota hai language ke andar.
<img src="https://techskillguru.com/cdata/cprogramming/images/C-Keywords.png" alt="Features" height="350px" width="350px

    # Operators
* Programming mein, operators wo symbols hote hain jo ek ya zyada operands par operations ko perform karte hain.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20231214120748/Operators-in-C.png" alt="Features" height="350px" width="350px"> 

## Arithmetic Operators:
* Arithmetic operators ka use operands par arithmetic ya mathematical operations perform karne ke liye kiya jaata hai.

### Yeh hain Arithmetic Operators:

| S. No. | Symbol | Operator | Description                                      | Syntax  |
|--------|--------|----------|--------------------------------------------------|---------|
| 1      | +      | Plus     | Do numeric values ko jodta hai.                  | a + b   |
| 2      | –      | Minus    | Right operand ko left operand se ghatata hai.    | a – b   |
| 3      | *      | Multiply | Do numeric values ko multiply karta hai.         | a * b   |
| 4      | /      | Divide   | Do numeric values ko divide karta hai.           | a / b   |
| 5      | %      | Modulus  | Left operand ko right operand se divide karne ke baad remainder return karta hai. | a % b   |

# Program for Arithmetic Operator
```
#include <stdio.h>
int main() {
   int num1,num2;
   printf("Enter first number: ");
   scanf("%d", &num1);
   printf("Enter Second number: ");
   scanf("%d", &num2);
   printf("num1+num2 = %d\n ", num1+num2);
   printf("num1-num2 = %d\n ", num1-num2);
   printf("num1*num2 = %d\n ", num1*num2);
   printf("num1/num2 = %d\n ", num1/num2);
   printf("num1%num2 = %d\n ", num1%num2);
   return 0;
}
```
Output
~~~
Enter first number: 7
Enter Second number: 9
num1+num2 = 16
num1-num2 = -2
num1*num2 = 63
num1/num2 = 0
num1%num2 = 1
=== Code Execution Successful ===
~~~
# Relational Operators
* C mein relational operators ka use do operands ka comparison karne ke liye hota hai.
* Ye saare operators binary operators hain jo comparison ke result mein true ya false value return karte hain.
Yeh hain Relational Operators:
| S. No. | Symbol | Operator | Description | Syntax |
|---|---|---|---|---|
| 1 | < | Less than | Returns true if the left operand is less than the right operand. Else false | a < b |
| 2 | > | Greater than | Returns true if the left operand is greater than the right operand. Else false | a > b |
| 3 | <= | Less than or equal to | Returns true if the left operand is less than or equal to the right operand. Else false | a <= b |
| 4 | >= | Greater than or equal to | Returns true if the left operand is greater than or equal to right operand. Else false | a >= b |
| 5 | == | Equal to | Returns true if both the operands are equal. | a == b |
| 6 | != | Not equal to | Returns true if both the operands are NOT equal. | a != b |

 ### Program for Relational Operators
```
#include <stdio.h>
int main() {
    int a, b;
    // Input two integers
    printf("Enter two integers: ");
    scanf("%d %d", &a, &b);
    //  Relational operators
    printf("%d == %d is %d\n", a, b, a == b);   // Equal to
    printf("%d != %d is %d\n", a, b, a != b);   // Not equal to
    printf("%d > %d is %d\n", a, b, a > b);     // Greater than
    printf("%d < %d is %d\n", a, b, a < b);     // Less than
    printf("%d >= %d is %d\n", a, b, a >= b);   // Greater than or equal to
    printf("%d <= %d is %d\n", a, b, a <= b);   // Less than or equal to
    return 0;
}
```
### Output
```
Enter two integers: 10 20
10 == 20 is 0
10 != 20 is 1
10 > 20 is 0
10 < 20 is 1
10 >= 20 is 0
10 <= 20 is 1
=== Code Execution Successful ===
```
### Logical Operator
* C mein logical operators ka use true ya false result check karne ke liye kiya jaata hai.
 Yeh hain Logical Operators:
| Operator    | Symbol | Description                                | Syntax   |
|-------------|--------|--------------------------------------------|----------|
| Logical AND | `&&`   | Returns true if both operands are true.     | `a && b` |
| Logical OR  | `||`   | Returns true if at least one operand is true. | `a || b` |
| Logical NOT | `!`    | Returns the opposite truth value of the operand. | `!a`     |
### Program for Logical Operators
```
#include <stdio.h>
int main() {
    int a, b;
    // Input two integers
    printf("Enter two integers: ");
    scanf("%d %d", &a, &b);

    //Logical AND (&&)
    if (a > 0 && b > 0) {
        printf("Both a and b are positive.\n");
    } else {
        printf("Either a or b (or both) are not positive.\n");
    }

    // Logical OR (||)
    if (a > 0 || b > 0) {
        printf("At least one of a or b is positive.\n");
    } else {
        printf("Neither a nor b is positive.\n");
    }

    // Logical NOT (!)
    if (!(a > 0)) {
        printf("a is not positive.\n");
    } else {
        printf("a is positive.\n");
    }

    return 0;
}
```
### Output
```
Enter two integers: 10 -10
Either a or b (or both) are not positive.
At least one of a or b is positive.
a is positive.

=== Code Execution Successful ===
```
## Assignment Operators
* Assignment operators ka use kisi variable ko value assign karne ke liye hota hai.
  Yeh hain Assignment Operators:
  | S. No. | Symbol | Operator | Description | Syntax |
|---|---|---|---|---|
| 1 | = | Simple Assignment | Assign the value of the right operand to the left operand. | `a = b` |
| 2 | += | Plus and assign | Add the right operand and left operand and assign this value to the left operand. | `a += b` |
| 3 | -= | Minus and assign | Subtract the right operand and left operand and assign this value to the left operand. | `a -= b` |
| 4 | *= | Multiply and assign | Multiply the right operand and left operand and assign this value to the left operand. | `a *= b` |
| 5 | /= | Divide and assign | Divide the left operand with the right operand and assign this value to the left operand. | `a /= b` |
| 6 | %= | Modulus and assign | Assign the remainder in the division of left operand with the right operand to the left operand. | `a %= b` |
				
### Example of Assignment Operators
```
#include <stdio.h>
int main(){
    int a = 25, b = 5;
    //  Assignment Operators
    printf("a = b: %d\n", a = b);
    printf("a += b: %d\n", a += b);
    printf("a -= b: %d\n", a -= b);
    printf("a *= b: %d\n", a *= b);
    printf("a /= b: %d\n", a /= b);
    printf("a %= b: %d\n", a %= b);
    return 0;
}
```
### Output
```
a = b: 5
a += b: 10
a -= b: 5
a *= b: 25
a /= b: 5
a %= b: 0
```

## Conditional/ Ternary Operator



