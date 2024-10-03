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
C mein single-line comment ( // ) double forward slash se start hota hai. 
~~~
 // Ye ek single line comment hai
```
### Multi-line Comment
Multi-line comment C mein forward slash aur asterisk ( /* ) se start hota hai aur asterisk aur forward slash ( */ ) par end hota hai. Jo bhi text /* aur */ ke beech mein likha hota hai, usse compiler ignore karta hai.
Ye program mein multiple lines ko comment karne ke liye use hota hai.
```
 /* Hello Isha
 Are You Fine? */
```

First Program in C
arduino
Copy code
#include<stdio.h>
int main(){
  printf("Hello World");
  return 0;
}
Output
Copy code
Hello World
Installation
Visual Studio Code ko download karne ke liye, aapko neeche diye gaye steps ko follow karna hoga:

Step 1:- Browser par "Download VsCode" search karo.

Step 2:- Pehli link par click karo.<a href="https://code.visualstudio.com/download">Visual Studio Code</a>

Step 3:- Apne Operating System ke hisaab se sahi download option select karo. Agar aap Ubuntu use kar rahe ho, to aapka download ek .deb file hoga.

<img src="https://res.cloudinary.com/omaha-code/w_768,h_502,c_fit/omaha-code-cdn/2018/12/Download-Visual-Studio-Code.png" alt="VS Code" height="350px" width="450px">
Step 4:- VS Code download hone ke baad, Linux mein terminal open karo ya shortcut ke liye (ctrl + alt + t) press karo.

Step 5:- System ko update hone ke liye command type karo: $ sudo apt update

Step 7:- System update hone ke baad, Download Directory mein jao: cd ~/Downloads

Step 8:- .deb Package ko install karne ke liye ye command type karo aur apna password enter karo: sudo dpkg -i code*.deb

Step 9:- Agar dependencies fix karni hain to ye command run karo: sudo apt install -f

Step 10:- VS Code ko launch karo:- Aap VS Code ko terminal mein code type karke ya application menu mein dhoondh kar open kar sakte ho.



System Requirement
Visual Studio Code (VS Code) chalane ke liye, aapko apne system ki requirements ko ensure karna hoga. Niche di gayi requirements ko aapko meet karna hoga:

OS: Ubuntu 14.04+, Fedora 24+, CentOS 7+
RAM: Kam se kam 4 GB RAM (8 GB ya usse zyada recommended)
Disk Space: 512 MB free disk space (2 GB ya usse zyada recommended)
Processor: Pentium ya faster processor
Mere system ki configurations aur software versions:
OS: Ubuntu 24.04 LTS
RAM: 8GB
Disk Space: 256 GB
Processor: 11th Gen Intel Core i3
VS Code Version: 1.91.1
Variables, Constant and Keywords
Variables
Variables programming mein pieces of information ko store karne ke liye use hote hain.
Ye ek tarah ke containers hote hain jo kuch data store karte hain (jaise hum rice, dal, sugar ko alag containers mein rakhte hain).
Rules of Naming Variables
Pehla character alphabet ya underscore(_) hona chahiye. NOTE:- Underscore ke alawa kisi special symbol ka use allowed nahi hai.
Variables mein commas ya blanks allowed nahi hain.
Variable names case sensitive hote hain. Jaise int STUDENT=10; aur int student=10; dono alag-alag variables hain.
Syntax of Declaring Variables
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20221202181339/Cvariables1.png" alt="Features" height="250px" width="550px">
WAP for Variables
arduino
Copy code
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
Output
makefile
Copy code
Age: 25
Height: 5.9
Initial: A
Salary: 50000.75
Name: Alice
Constant
Constants C mein read-only variables hote hain jinke values program mein declare hone ke baad change nahi kiye jaa sakte.
Constant ek integer, floating point, string, ya character ho sakte hain.
C language mein const keyword ka use constant define karne ke liye hota hai.
Syntax of Declaring Constant
rust
Copy code
const data_type var_name = value;
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20230306215927/syntax-of-constants-in-c.png" alt="Features" height="250px" width="550px">
WAP of Constant
arduino
Copy code
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
Output
less
Copy code
Number of days in a week: 7
Number of months in a year: 12
Highest grade: A
=== Code Execution Successful ===
Keywords
Keywords C language mein reserved words ka set hota hai jinka predefined meaning hota hai aur jo C programming likhne mein use hote hain.
In keywords ka use identifiers ya variable names ke liye nahi ho sakta, kyunki inka ek specific function hota hai language ke andar.
<img src="https://techskillguru.com/cdata/cprogramming/images/C-Keywords.png" alt="Features" height="350px" width="350px">





