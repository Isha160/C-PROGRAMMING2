# C Programming

<img src="https://contentstatic.techgig.com/photo/90325682.cms" alt="C Programming" height="350px" width="450px">

# Table of Content
- [Introduction](#Introduction)
- [Installation](#Installation)
- [System Requirement](#System-Requirement)
- [Variables, Constant and Keywords](#Variables-Constant-and-Keywords)
- [Operators](#Operators) 
- [Control Statements and Decision Making](#Control-Statements-and-Decision-Making)
- [Pointer](#Pointer)
- [Array](#Array)
- [String](#String)
- [References](#References)

# Introduction 
* Programming- Computer programming ek medium hai jisse hum computers se communicate karte hain. Jaise humans Hindi/English language ka use karke ek dusre se communicate karte hai, waise hi Programming ek tareeka hai jisse hum apne 
    instructions computer ko deliver karte hain unse communicate krne k liye.
* C ek sabse purani Programming languages mein se ek hai, jo Dennis Ritchie ne 1972 me develop ki thi.

# Features 
<img src="https://techvidvan.com/tutorials/wp-content/uploads/sites/2/2021/08/Features-of-C.jpg" alt="Features" height="350px" width="350px">

# Comments in C
C Programming me do tarah ke comments hote hain:
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

* Step 3:- Apne Operating System ke hisaab se sahi option select karo. Agar aap Ubuntu use kar rahe ho, to aapka download ek .deb file hoga.

<img src="https://res.cloudinary.com/omaha-code/w_768,h_502,c_fit/omaha-code-cdn/2018/12/Download-Visual-Studio-Code.png" alt="VS Code" height="350px" width="450px">

* Step 4:- VS Code download hone ke baad, Linux mein terminal open karo ya shortcut ke liye (ctrl + alt + t) press karo.

* Step 5:- System ko update hone ke liye command type karo: $ sudo apt update

* Step 7:- System update hone ke baad, Download Directory mein jao: cd ~/Downloads

* Step 8:- .deb Package ko install karne ke liye ye command type karo aur apna password enter karo: sudo dpkg -i code*.deb

* Step 9:- Agar dependencies fix karni hain to ye command run karo: sudo apt install -f

* Step 10:- VS Code ko launch karo:- Aap VS Code ko terminal mein code type karke ya application menu mein dhoondh kar open kar sakte hai.



# System Requirement
Visual Studio Code (VS Code) chalane ke liye, aapko apne system ki requirements ko ensure karna hoga. Niche di gayi requirements ko aapko fulfill karna hoga:

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
  
# Variables, Constant and Keywords
## Variables
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
* Constants read-only variables hote hain, jinke values program mein declare hone ke baad change nahi kiye jaa sakti.
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
* Keywords C language mein reserved words hote hai, jinka predefined meaning hota hai aur jo C programming likhne mein use hote hain.
* In keywords ka use identifiers ya variable names ke liye nahi ho sakta, kyunki inka ek specific function hota hai language ke andar.
  
<img src="https://techskillguru.com/cdata/cprogramming/images/C-Keywords.png" alt="Features" height="350px" width="350px">

  # Operators
* Programming mein, operators wo symbols hote hain jo ek ya zyada operands par operations ko perform karte hain.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20231214120748/Operators-in-C.png" alt="Features" height="350px" width="350px"> 
* Note :- Operators ki or jankari k liye is link ko follow kre : <a href="https://www.geeksforgeeks.org/operators-in-c/">https://www.geeksforgeeks.org/operators-in-c</a>

## Arithmetic Operators:
* Arithmetic operators ka use operands par arithmetic ya mathematical operations perform karne ke liye kiya jaata hai.

### Yeh hain Arithmetic Operators:

| S. No. | Symbol | Operator | Description                                      | Syntax  |
|--------|--------|----------|--------------------------------------------------|---------|
| 1      | +      | Plus     | Do number ko jodta hai.                          | a + b   |
| 2      | –      | Minus    | Do number ko Subtract krta hai                   | a – b   |
| 3      | *      | Multiply | Do number ko multiply karta hai.                 | a * b   |
| 4      | /      | Divide   | Do number ko divide karta hai.                   | a / b   |
| 5      | %      | Modulus  | Do number ka divide karne ke baad remainder return karta hai. | a % b   |

### Program for Arithmetic Operator
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
## Relational Operators
* C mein relational operators ka use do operands ka comparison karne ke liye hota hai.
* Ye saare operators binary operators hain jo comparison ke result mein true ya false value return karte hain.
Yeh hain Relational Operators:

| S. No. | Symbol | Operator | Description | Syntax |
|---|---|---|---|---|
| 1 | < | Less than |Agar left operand right operand se chhota ho toh true return karta hai. Warna false | a < b |
| 2 | > | Greater than | Agar left operand right operand se bada ho toh true return karta hai. Warna false | a > b |
| 3 | <= | Less than or equal to |Agar left operand right operand se chhota ya equal ho toh true return karta hai. Warna false | a <= b |
| 4 | >= | Greater than or equal to | Agar left operand right operand se bada ya equal ho toh true return karta hai. Warna false | a >= b |
| 5 | == | Equal to | Agar dono operands barabar ho toh true return karta hai. | a == b |
| 6 | != | Not equal to | Agar dono operands barabar na ho toh true return karta hai. | a != b |

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
## Logical Operator
* C Programming mein logical operators ka use true ya false result check karne ke liye kiya jaata hai.
 Yeh hain Logical Operators:

| Operator    | Symbol | Description                                | Syntax   |
|-------------|--------|--------------------------------------------|----------|
| Logical AND | `&&`   | Tabhi true return karta hai jab dono operands true hoon.    | `a && b` |
| Logical OR  | `\|\|`   | Tabhi true return krega jb at least ek operand true h. | `a \|\| b` |
| Logical NOT | `!`    | Operand ki opposite truth value return karta hai.| `!a`     |

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
* Ternary operator ek shorthand tareeka hai if-else statement likhne ka.
### Syntax 
```
Condition? expression-if-true: expression-if-false;
```
### Example 
```
#include<stdio.h>
int main(){
    int a;
    printf("Enter value of a\n");
    scanf("%d",&a);
    (a<5)?printf("A is less than 5"):printf("A is not less than 5");
    return 0;
}
```
### Output
```
Enter value of a
7
A is not less than 5ements

=== Code Execution Successful ===
```
# Control Statements and Decision Making
* Control statements wo statements hote hain jo instructions ke execution k flow ko control karte hain.
    <img src="https://examradar.com/wp-content/uploads/2016/10/Classification-of-control-statements.png" alt="Control statements" width="450px" height="350px">
    ## Branching Statements
  ### If Statements
  * "if" statement ek control flow structure hai jo ek block code ko tabhi execute karta hai jab koi specified condition true ya false ho.
    ##### Example
  ```
  #include <stdio.h>
  int main() {
    int number = 10;
    if (number > 5) {
        printf("The number is greater than 5.\n");
     }
  }
  ```
  #### Output
  ```
  The number is greater than 5.
  ```
  ### If-else Statements
  * The if-else statement ek conditional control structure hai jo hume ek block of code tab execute karne deta hai jab condition true ho, aur doosra block of code tab execute hota hai jab condition false ho.
     #### Example
    ```
    #include <stdio.h>
     int main() {
     int number = 3;
     if (number > 5) {
        printf("The number is greater than 5.\n");
       } else {
        printf("The number is 5 or less.\n");
       }
     }
    ``
  #### Output
  ```
  The number is 5 or less.
  ```
  ### If-else-if Statements
  * The if-else if statement multiple conditions ko sequence me test karne ke liye use hota hai.
* Yeh tumhe alag-alag blocks of code ko execute karne ka mauka deta hai, ye is baat par depend karta hai kaunsi condition true hoti hai.
  #### Example
    ```
    #include <stdio.h>  
    int main() {
    int number = 0;
    if (number > 0) {
        printf("The number is positive.\n");
    } else if (number < 0) {
        printf("The number is negative.\n");
    } else {
        printf("The number is zero.\n");
     }
    }
   ```
#### Output
```
The number is zero.
```
### Switch Statements
* The switch statement C mein ek control flow structure hai jo expression ki value ke basis par alag-alag code blocks ko execute karne ki suvidha deta hai.
  #### Example
```
#include <stdio.h>
int main() {
    int day = 3;
    switch (day) {
        case 1:
            printf("Monday\n");
            break;
        case 2:
            printf("Tuesday\n");
            break;
        case 3:
            printf("Wednesday\n");
            break;
        case 4:
            printf("Thursday\n");
            break;
        case 5:
            printf("Friday\n");
            break;
        case 6:
            printf("Saturday\n");
            break;
        case 7:
            printf("Sunday\n");
            break;
        default:
            printf("Invalid day\n");
            break;
    }
}
```
#### Output
```
Wednesday
```
## Iterative/ Loop Statements 
* Iterative ya loop statements unhe kehte hain jo ek block of code ko condition ke basis par baar-baar execute karte hain.
* Yeh repetitive tasks ko efficiently perform karne ki suvidha dete hain bina same code ko baar-baar likhne ke.
### For Loop
* Loop statements ka use instructions ke set ko repeated order mein execute karne ke liye hota hai.
* Instructions ka execution ek particular condition par depend karta hai.
   #### Syntax of for Loop
   ```
   for (initialization; condition; Increment/decrement) {
    // Code to execute on each iteration
    }
   ```
     #### Example
    ```
    #include <stdio.h>
     int main() {
    // Loop from 0 to 4
    for (int i = 0; i < 5; i++) {
        printf("Number %d\n", i);
      }
    }
    
   ```
### Output

```
Number 0
Number 1
Number 2
Number 3
Number 4
```
### While Loop
* The while loop C mein ek control flow statement hai jo tumhe ek block of code tab tak baar-baar execute karne deta hai jab tak specified condition true hoti hai.
 #### Syntax of While Loop
  ```
  while (condition) {
  // code block to be executed
   }
  ```
#### Example
```
#include <stdio.h>
int main() {
    int i = 0;
    // Loop from 0 to 4
    while (i < 5) {
        printf("Number %d\n", i);
        i++; // Increment the loop variable
    }
 }
```
#### Output
```
Number 0
Number 1
Number 2
Number 3
Number 4
```
### do While Loop
* The do-while loop ek control flow statement hai jo tumhe ek block of code ko tab tak baar-baar execute karne deta hai jab tak specified condition true hoti hai.
* Do-while loop mein body ko kam se kam ek baar toh execute kiya jaata hai condition test karne se pehle.
 ####  Syntax of do While Loop
 ```
 do {
    // Code to execute at least once and then repeatedly while condition is true
  } while (condition);
```
#### Example
```
#include <stdio.h>
int main() {
    int i = 0;
    // Loop that runs as long as i is less than 5
    do {
        printf("Number %d\n", i);
        i++; // Increment the loop variable
    } while (i < 5);
 }
```
#### Output
```
Number 0
Number 1
Number 2
Number 3
Number 4
```
## Jump Statements
* Jump statements C programming me programmers ko apne code ke normal flow of execution ko alter (badalne) ki suvidha dete hain.
* Jump statements 3 types ke hote hain.
  i)   Break
 ii)  continue
  ### Break Statements
  *The break statement ka use loop se bahar nikalne ke liye kiya jaata hai.
#### Example
    ```
    #include <stdio.h>
    int main() {
    for (int i = 0; i < 10; i++) {
        if (i == 5) {
            break; // Exit the loop when i equals 5
        }
        printf("%d ", i);
      }
    }
    ```
#### Output
```
0 1 2 3 4
```
### Continue Statements
* The continue statement ka use current iteration ke liye loop body ke bache hue part ko skip karne aur loop ke agle iteration par jaane ke liye kiya jaata hai.
  #### Example
  ```
  #include <stdio.h>
   int main() {
    for (int i = 0; i < 10; i++) {
        if (i % 2 == 0) {
            continue; // Skip the rest of the loop body for even numbers
        }
        printf("%d ", i);
    }
    return 0;
  }
  ```
#### Output
```
1 3 5 7 9 
```
* Note :- About goto statements : <a href="https://www.javatpoint.com/c-goto">https://www.javatpoint.com/c-goto</a>
# Pointer
* Ek pointer ek variable hai jo kisi doosre variable ka address store karta hai.
   ## Syntax of pointer
  ```
  datatype * ptr;
  where,
      ptr is the name of the pointer.
      datatype is the type of data it is pointing to.
  ```
  ## Address Of (&) Operator
  * Address of operator '&' ek variable ka address return karta hai.
  * Lekin, variable ka address display karne ke liye hume % ka use karna padta hai.
     ## Example of Pointer
  ```
  #include <stdio.h>
  int main() {
  int a=6;
  int *ptr;
  ptr=&a;
  printf("The address of variable a is %u\n",ptr);
  printf("The address of variable a is %u\n",*ptr);
    }
``
### Output
```
The address of variable a is 1763721828
The address of variable a is 6
```
 # Array
 * Ek array similar type ke elements ka collection hota hai.
* Yeh ek simple aur fast tareeka hai multiple values ko ek hi naam ke sath store karne ka.
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20230302091959/Arrays-in-C.png" alt="Array" height="350px" width="450px">
    ## Syntax of Array
   ```
   data_type array_name [size1] [size2]...[sizeN];
   ```
   ## Example
   ```
   #include <stdio.h>
   int main() {
   int marks[5];
   for(int i=0;i<5;i++){
     printf("Enter the English marks of students %d :",i+1);
     scanf("%d",&marks[i]);
    }
   }
  ``
## Output
```
Enter the English marks of students 1 :70
Enter the English marks of students 2 :60
Enter the English marks of students 3 :90
Enter the English marks of students 4 :98
Enter the English marks of students 5 :78

=== Code Execution Successful ===
```
# String
* C Programming me, String ko characters ki ek sequence ke roop mein define kiya jaata hai, jo ek special character se khatam hoti hai, jise null character ('\0') kha jata hain.
* Yeh null character string ke end ko indicate karta hai.
## Initializing Strings
* Kyunki string characters ka array hai, isliye ise is tarah se initialize kiya jata hai:
  <img src="https://d8it4huxumps7.cloudfront.net/uploads/images/6492a64d1cd59_strings_in_c_03.jpg" alt="string" height="350px" width="450px">
 ## Printing Strings
 * Ek string ko character by character print kiya ja sakta hai by using "printf" aur "%s".
    ### Example
      ```
      #include<stdio.h>
      int main(){
      char st[]="hello isha";
      printf("%s",st);
        }
      ```
     
### Output

```
hello isha
```
## gets() and puts()
* gets() ek function hai jo multi-word string ko receive karne ke liye use kiya ja sakta hai.
* puts() ek function hai jo string ko print karta hai aur output ko ek newline par le jaata hai.
   ### Example
  ```
  #include<stdio.h>
   int main(){
    char s[34];
    printf("Enter your name : ");
    gets(s);
    puts(s);
    printf("Your Name is %s ",s);   
  }
  ```
 ### Output
```
Enter your name : ISHA JANGRA
ISHA JANGRA
Your Name is ISHA JANGRA
```
 # References
 
* https://www.studocu.com/row/document/tribhuvan-vishwavidalaya/information-technology/c-programming-notes/2664815
* https://www.geeksforgeeks.org/operators-in-c/
* https://www.scholarhat.com/tutorial/c/loops-in-c
* https://www.javatpoint.com/c-gets-puts#:~:text=C%20puts()%20function&text=The%20puts()%20function%20is,being%20printed%20on%20the%20console.















