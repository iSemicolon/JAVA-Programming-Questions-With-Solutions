# JAVA-PROGRAMMING-QUESTIONS-WITH-SOLUTIONS  #

1.	Area and perimeter of square
2.	Area and perimeter of rectangle
3.	Total marks and percentage taking 4 input
4.	Read product name, price, display product price
5.	Take weight and height and calculate bmi
6.	Read integer check special digit or not
7.	Print biggest fro  two numbers
8.	Check two numbers are same or not
9.	Print positive integer or not
10.	Read product price and print 10% discount of product if price is greater than 5000
11.	Read three input and print smallest one
12.	Check even or odd
13.	Print idf divisible by 3 print “Sanju”, divisible by 5 print  “geeta” divisible by 3& 5 print “sanju weds getea”, otherwise breakup
14.	Read three integer print biggest one
15.	Read three integer print middle value
16.	Read month number print corresponding name
17.	Check leap year
18.	Read day number print corresponding day
19.	Enter a character check vowel or not
20.	Read integer check it’s a one digit or not
21.	Read integer it’s a double digit or not
22.	Print number from 1 to N and N to 1
23.	Print sum of number
24.	Print sum of odd number
25.	Factorial of a number
26.	Average of a number
27.	Enter a number and print how many leap Year up to these number
28.	Ask user to generate a number to 0-9 and generate a random from 0-9. Guess number are same or not. If same print you win otherwise you lose and count how many time you attend to reach correct value
29.	Take a number check it it’s a prime or not
30.	Count how many digit in a number
31.	Sum of digit of a number
32.	Calculate product of digit
33.	Calculate how many even and odd in digit and find sum
34.	Find reverse number
35.	Check number is palindrome or not
36.	Check number is strong number oir not
37.	Find a to the power of a number. Ex- 2^3=8
38.	Diserium number
39.	 Take a number and print its multiplication table up to 10
40.	Convert binary to decimal
41.	Octal to decimal
42.	Hexa to decimal
43.	Decimal to binary
44.	Decimal to octal
45.	Decimal to hexa
46.	Print all prime number within 100
47.	Display how many Armstrong within 1000
48.	Print diserium number within 1000
49.	Print all three digit palindrome number
50.	Print sum of all perfect number within 1000
51.	Print first n Fibonacci number
52.	Check a number is happy number or not
53.	Print all happy number within 1000
54.	Print first 10 prime numbers
55.	Write a method and return product of digits
56.	Return sum of first n prime numbers
57.	Find average of digits
58.	Print Fibonacci Series With & Without Recursion
*****
*****
*****
*****
*****
59.	12345
12345
12345
12345
12345
60.	111
222
333
61.	10101
10101
10101
10101
10101
62.	1111
****
1111
****
63.	Take array input and display
64.	Sum of value of array
65.	Print average of product using array
66.	Test a specified value is present in array or not, if present how many times
67.	Print of array index of particular array elements
68.	print smallest and largest value of an array & difference, sum
69.	Count how many even and odd element is present in array
70.	Sum of even and odd of an array.
71.	DUPLICATE ARRAY
72.	REVERSE OF ARRAY
73.	PRODUCT OF ARRAY
74.	FIND LARGEST AND SMALLEST ELEMENT PRESENT IN ARRAY
75.	READ AND DISPLAY ARRAY ELEMENT RETURN ENTIRE ARRAY
76.	MERGE TWO ARRAY’S AND RETURN SDINGLE ARRAY
77.	COUNT HOW MANY PRIME NUMBER PRESENT ION ARRAY
78.	 HOW MANT POSTIVE AND NEGATIVE ELEMENT PRESENT IN ARRAY
79.	HOW MANY PERFECT NUMBER PRESENT IN ARRAY
80.	HOW MANY ZERO AND NON-ZERO ELEMENT IN ARRAY
81.	DEFINE A METHOD MERGER TWO ARRAY’S IN ZIGZAG ARRAY
82.	insert a element in specified location in array
83.	Delete a element from a specified index in array
84.	Wajp to intersection between two array elements

105.	READ TWO DIMENSIONAL ARRAY, RETURN TWO DIMENSIONAL ARRAY
106.	FIND LARGEST AND SMALLEST ELEMENT IN ARRAY 
107.	ADD TWO MATRIX
108.	TRANSPOSE OF MATRIX
109.	ROW WISE AND COLUMN WISE BIGGEST ELEMENT
110.	ROW WISE AND COLUMN WISE REVESE ELEMENT
111.	ROTATE MATRIX 90 DEGREE LEFT AND 90 DEGREE RIGHT
112.	Read DIAGONAL ELEMENT ,REVERSE DIAGONAL ELEMENT
113.	FIND SMALLEST AND LARGEST IN DIAGONAL ELEMENT
114.	MULTIPLY TWO MATRIX
115.	ROW WISE AND COLUMN WISE SUM OF MATRIX


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                                                                       STRING
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
/*
String to Character Conversion :

String s="JAVA";
char array[]=s.toCharArray();

Character At Particular Index :

char array=s.charAt(1); //A

LENGTH OF STRING = s.length();

*/


85.	WAJP TO CONVERT A USER ENTERED NUMBER INTO A SENTENCE. 

Input::211652509
output: Twenty One Crore Sixteen Lakh Fifty Two Thousand Five Hundred Nine



Programm::

import java.util.Scanner;

class TestNumberToSentence{
public static void isNumberToSentence(int num, String s){

String one[]={"","One", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Eleven","Twelve", "Thirteen", "Fourteen", "Fifteen", "Sixteen", "Seventeen", "Eighteen", "Nineteen"};

String two[]={"","","Twenty", "Thirty", "Fourty", "Fifty", "Sixty", "Seventy","Eighty", "Ninety"};


if(num>=20)
{

System.out.print( two[num/10]+" "+ one[num%10]);

}

else
{
System.out.print(one[num]);
}

if(num!=0)
{

System.out.print(" "+s+" ");
}

}
public static void main(String args[])


{

Scanner sc=new Scanner(System.in);
System.out.println("Enter The Number");

int n=sc.nextInt();

//Crore Calculate
isNumberToSentence((n/10000000), "Crore"); //21

//Lakh Calculate
isNumberToSentence(((n/100000)%100), "Lakh"); // 2116%100=16

//Thousand Calculate
isNumberToSentence(((n/1000)%100), "Thousand"); // 211652%100=52


//Hundred Calculate
isNumberToSentence(((n/100)%10), "Hundred"); //2116525%10=5


//Decimal Calculation
isNumberToSentence(n%100,"");


}
}



---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
86.	WAJP TO ENTER A DATE IN DD MM YYYY FORMAT AND FIND THE CORRESPONDING DAY NAME

input- 07-04-1997
output- Monday


Programm:

import java.util.Scanner;
class TestDayName
{

public static void isDayName(int d, int m, int y)
{


String day[]={"Sunday", "Monday", "Tuesday", "Wednesday", "Thrusday", "Friday", "Saturday"};
int month[]={0,31,28,31,30,31,30,31,31,30,31,30,31};

int totalDay=0;
//calculate numbers of day from 0 to particular year

y=y-1;

totalDay=365*y;

//extra day because of leap year

int ed= (y/400)+(y/4)-(y/100);

totalDay=totalDay+ed;

// Calculate the day from o to particular month of particular Year

 m=m-1;

for(int i=1; i<=m;i++)
{
totalDay=totalDay+month[i];
}

//Number of for that month

totalDay=totalDay+d;


System.out.println((d)+"-"+(m+1)+"-"+(y+1)+" "+" is "+day[totalDay%7]);


}

public static void main(String args[])
{
Scanner sc=new Scanner(System.in);
System.out.println("Enter Date DD FORMAT");
int d=sc.nextInt();

System.out.println("Enter Month MM FORMAT");
int m=sc.nextInt();

System.out.println("Enter Year YYYY FORMAT");
int y=sc.nextInt();

isDayName(d,m,y);

}
}

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
87.	WAJP TO COUNT THE NUMBER OF DAYS BETWEEN TO DATE (DD MM YYYY FORMAT)

input1-07-04-1997
input2-02-03-1800

output-71989

programm::
import java.util.Scanner;
class TestDayCount
{

public static int isDayCount(int d, int m, int y)
{

int month[]={0,31,28,31,30,31,30,31,31,30,31,30,31};

int totalDay=0;
//calculate numbers of day from 0 to particular year

y=y-1;

totalDay=365*y;

//extra day because of leap year

int ed= (y/400)+(y/4)-(y/100);

totalDay=totalDay+ed;

// Calculate the day from o to particular month of particular Year

 m=m-1;

for(int i=1; i<=m;i++)
{
totalDay=totalDay+month[i];
}

//Number of day for that month

totalDay=totalDay+d;


return totalDay;

}

public static void main(String args[])
{
Scanner sc=new Scanner(System.in);
System.out.println("First Date");
System.out.println("Enter Date DD FORMAT");
int d1=sc.nextInt();

System.out.println("Enter Month MM FORMAT");
int m1=sc.nextInt();

System.out.println("Enter Year YYYY FORMAT");
int y1=sc.nextInt();

int td1=isDayCount(d1,m1,y1);


System.out.println("Second Date");
System.out.println("Enter Date DD FORMAT");
int d2=sc.nextInt();

System.out.println("Enter Month MM FORMAT");
int m2=sc.nextInt();

System.out.println("Enter Year YYYY FORMAT");
int y2=sc.nextInt();

int td2=isDayCount(d2,m2,y2);

System.out.println("Day Difference Between Two days is "+(td1-td2));

}

}




---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
88.	CONVERT STRING TO CHARACTER ARRAY, STRING DIGIT TO INTEGER, STRING ELEMENT TO CHAR
89.	FIND STRING LENGTH, INDEX VALUE, INDEX ELEMENT OF PARTICULAR STRING
90.	TAKE INPUT FROM USER AND PRINT FIRST AND LAST LETTER, SECOND LAST LETTER
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
91.	PRINT REVERSE STRING

INPUT:: I AM PALASH
OUTPUT:: HSALAP MA I



import java.util.Scanner;

class TestReverseString
{
public static void isReveseString(String st)
{

String str="";

for(int i=st.length() -1; i>=0; i--)
{

str=str+st.charAt(i);
}

System.out.println(str);

}

public static void main(String args[])
{
Scanner sc=new Scanner(System.in);
System.out.println("Enter String");
String s=sc.nextLine();

isReveseString(s);

}
}


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
92.	REVERSE STRING WITHOUT AFFECTING SPECIAL CHARACTER

INPUT-AB@C
OUTPUT-CB@A

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
93.	WAJP TO COUNT HOW MANY UPPER CASE , LOWER CASE, VOWEL, CONSONANT, DIGITS, SPECIAL CASE IN A GIVEN STRING
94.	WAJP TO ADD ALL THE DIGITS IN GIVEN STRING
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
95.	COUNT NUMBER OF OCCURENCE OF A STRING
input- I AM PALASH
OUTPUT-
I No Of Occurence: 1
A No Of Occurence: 3
M No Of Occurence: 1
P No Of Occurence: 1
L No Of Occurence: 1
S No Of Occurence: 1
H No Of Occurence: 1

programm::

import java.util.Scanner;

class TestLetterCount{

public static void isCount(String st)
{

int count[]=new int[256];

for(int i=0; i<st.length();i++)
{

count[st.charAt(i)]++;
}

for(int j=0; j<st.length();j++)
{
int flag=0;
char ch=st.charAt(j);
for(int k=0; k<=j;k++)
{

if(ch==st.charAt(k))
{
flag++;
}


}

if(ch!=' ' && flag==1)
{
System.out.println(ch+" No Of Occurence: "+count[ch]);
}

}

}

public static void main(String args[])

{
Scanner sc=new Scanner(System.in);
System.out.println("Enter String");

String s=sc.nextLine();

isCount(s);
}
}

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
96.	WAJP TO CONVERT ALL SENTENCE IN UPPER CASE AND ALSO LOWER CASE


97.	WAJP TO COUNT HOW MANY WORD PRESENT IN GIVEN A GIVEN SENTENCE

input: I AM PALASH
input: AM I PALASH

output: 3

import java.util.Scanner;
class TestCountWord{

public static void isWordCount(String s){

int count=0;

for(int i=0; i<s.length();i++)
{

if((i==0 && s.charAt(i)!=' ') ||(s.charAt(i)!=' ' && s.charAt(i-1)==' '))
{
count++;
}
}

System.out.println("Number Of Word Present is : "+count);

}
public static void main(String args[])
{
Scanner sc=new Scanner(System.in);
System.out.println("Enter String As a Sentence");
String st=sc.nextLine();

isWordCount(st);
}
}

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
98. WAJP GIVEN SUBSTRING IS PRESENT OR NOT IN A  STRING


import java.util.Scanner;

class TestSubStringFind{

 public static boolean isStringFind(String str, String s)
{



for(int i=0; i<str.length(); i++)
{

int j=i;
int k=0;
System.out.println(str.length()+" "+s.length());

while( (k<s.length()) && (s.charAt(k)==str.charAt(j)) &&(j<str.length()) )
{
j++; //2-7
k++;
System.out.println(j+" "+k);
}


if(k==s.length())
{
return true;
}
}

return false;

}

public static void main(String args[])
{

Scanner sc=new Scanner(System.in);

String str="APALASHPALASH SAMANDTA PALASH SAMANTA PALASH ";
System.out.println("ENTER STRING");
String s=sc.nextLine();
System.out.println("ENTER STRING");
boolean bool=isStringFind(str, s);

if(bool==true)
{
System.out.println("String is Present");
}

else
{
System.out.println("String is NOT Present");
}

}
}

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
100. WAJP HOW MANY TIMES SUBSTRING PRESENT IN A STRING 
101.	WAJP TO CONVERT EVERY WORD FIRST CHARACTER INTO CAPITAL REMAINING ALL TO SMALL
I am PALasH
I Am Palash
99.	WAJP TO CONVERT EVERY WORD Last CHARACTER INTO CAPITAL REMAINING ALL TO Upper
I am palash
I aM  palasH
100.	Wajp to REVERSE THE WORD IN THE SENTENCE
RAMA AND LAXMANA
AMAR DNA ANAMXAL
101.	WAJP TO REVERSE THE SENTENCE
rama and laxmana
laxmana and rama 
102.	Wajp PRINT HOW MANY VOWELS PRESENT IN EACH WORD
103.	WAJP SWAP EVER WORD FIRST CHARACTER WITH THERE LAST CHARACTER
EX: Rama and laxman 
aamr dna naxmal

104.	 First and second and last index of sentence from where sub string occurrence present. if not present return =-1

