# assignment-2.1
QN a. Write a Java code with the class name, “acad,” and a method called “main.”
Hard code the program with two integers and print the sum of those two
integers
public class acad {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
int a=40;//initialising a variable directly
int b=20;//initialising b variable directly
int sum=a+b;
System.out.println(sum);
	}

}
QN b. Rewrite the above code, wherein the inputs are provided by the user at
runtime and the output is printed.
import java.util.Scanner;


public class acad {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
Scanner in=new Scanner(System.in);
System.out.println("enter input");
int number1=in.nextInt();//getting input at runtime
int number2=in.nextInt();//getting input at runtime
int sum=number1+number2;
System.out.println(sum);
	}

}
  QN c. Write a program with the method name, “sum()” that accepts two
parameters from the user and print the sum of those two numbers. The
output format should be:
First number is:
Second number is:
Sum is

import java.util.Scanner;


public class acad {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
Scanner in=new Scanner(System.in);//scanner used for getting input from user through keybaord 

int number1=in.nextInt();//getting input at runtime
int number2=in.nextInt();//getting input at runtime
sum(number1,number2);//calling the static method sum which accepts 2 parameters(number1,number2)
	}
	static void sum(int a,int b)
	{
		int sum=a+b;
		System.out.println("First number is: "+a);
		System.out.println("Second number is: "+b);
		System.out.println("Sum is:"+sum);
	}

}
QN d. Write a program to accept two numbers from “stdin” and find all the odd
as well as even numbers present in betwee


import java.util.ArrayList;
import java.util.Scanner;


public class acad {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
Scanner in=new Scanner(System.in);
System.out.println("enter numbers between which you want to find odd and even(inclusive of those 2 numbers)");
int number1=in.nextInt();//getting input 
int number2=in.nextInt();//getting input
ArrayList<Integer> odd=new ArrayList<>();//used arraylist as there is no size related problem;
ArrayList<Integer> even=new ArrayList<>();

for(int a=number1;a<=number2;a++)//running for loop
{
	
	if(a%2==0)//getting even numbers
	{
		even.add(a);
		
	}

	
	if(a%2!=0)//getting odd numbers
	{
		odd.add(a);
	}
	}
System.out.println("Even numbers between "+number1+" and "+number2);//printing even numbers
for(int m=0;m<even.size();m++)
{
System.out.print(even.get(m)+" ");
}
System.out.println();
System.out.println("Odd numbers between "+number1+" and "+number2);//printing odd numbers
for(int m=0;m<odd.size();m++)
{
System.out.print(odd.get(m)+" ");
}
}
}
QN e. Joe is scared to go to school. When her dad asked for the reason, Joe said
that she was unable to complete the task given to her by her teacher. The
task was to find the “first 10 multiples” of the number entered from
“stdin”.

import java.util.ArrayList;
import java.util.Scanner;


public class acad {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
Scanner in=new Scanner(System.in);
System.out.println("enter numbers between which joe want to find multiples");
int number1=in.nextInt();//getting input 
int sum=0;
//since we want to find multiples first 10 multiples running a for loop and I am adding 10 times the given number
for(int a=1;a<=10;a++)
{
	sum=sum+number1;
	System.out.println(number1+"*"+a+"="+sum);//printing the tables
	
}
}
}
QN f. Write a program consisting the method “sum()” and demonstrate the
concept of method overloading using this method
OVERLOADING helps to modify the same method according to our wish.This helps in acheiving one of the concepts of OOPS "polymorphism" 
overloading could be done by changing 
1. Number of parameters.
2. Data type of parameters.
3.Sequence of Data type of parameters.

public class acad {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
Scanner in=new Scanner(System.in);//scanner used for getting input from user through keybaord 
System.out.println("Enter name");
String name=in.next();
System.out.println("Enter marks");
int number1=in.nextInt();//getting input at runtime
int number2=in.nextInt();//getting input at runtime
int number3=in.nextInt();

acad a=new acad();//creating object a to call non staic method sum inside static method
acad a1=new acad();
acad a2=new acad();
acad a3=new acad();
a.sum(number1,number2);//calling the static method sum which accepts 2 parameters(number1,number2)
	a1.sum(number1,number2,number3);
	a2.sum(name,number1,number2,number3);
	a3.sum(number1,number2,number3,name);
	
	}
	
	// Overloading – Different Number of parameters
	
	public void sum(int a,int b)
	{
		int sum=a+b;
		
		System.out.println("Sum of 2 main subject:"+sum);
	}
	public void sum(int a,int b,int c)
	{
		int sum=a+b+c;
		System.out.println("Sum of 3 subjects(including optional subject):"+sum);

	}
	public void sum(String name,int a,int b,int c)//Overloading – Data type of parameters.
	{
		int sum=a+b+c;
		System.out.println("Marks of "+name+" and his marks");
		System.out.println("Sum of 3 subjects(including optional subject):"+sum);

	}
	public void sum(int a,int b,int c,String name)//Overloading –Sequence of Data type of parameters.
	{
		int sum=a+b+c;
		System.out.println("Marks of "+name+" and his marks");
		System.out.println("Sum of 3 subjects(including optional subject):"+sum);

	}

}

QN-g. Can you overload a method with the same return type? Explain your
answer with proper logic
1.YES we can overload a method with same return type by changing the number of parameters.Take the case if we want to find the performance of student in 2 main subjects and suppose we want to find the total of other subjects also.
In this case we can use two sum methods with different parameters and find the students' performance
2.If we overlad with different return type it will be confusing for the compiler to call which method
import java.util.Scanner;


public class acad {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
Scanner in=new Scanner(System.in);//scanner used for getting input from user through keybaord 
System.out.println("Enter name");
String name=in.next();
System.out.println("Enter marks");
int number1=in.nextInt();//getting input at runtime
int number2=in.nextInt();//getting input at runtime
int number3=in.nextInt();

acad a=new acad();//creating object a to call non staic method sum inside static method
acad a1=new acad();
a.sum(number1,number2);//calling the static method sum which accepts 2 parameters(number1,number2)
	a1.sum(number1,number2,number3);//calling the method which accepts 3 parameters
	
	
	}
	
	// Overloading – Different Number of parameters
	
	public void sum(int a,int b)
	{
		int sum=a+b;
		
		System.out.println("Sum of 2 main subject:"+sum);
	}
	public void sum(int a,int b,int c)
	{
		int sum=a+b+c;
		System.out.println("Sum of 3 subjects(including optional subject):"+sum);

	}
}
QN h. Write a program in Java using Arrays, that sorts the element in a
descending order.


import java.util.Arrays;
import java.util.Scanner;


public class acad {

	public static void main(String[] args) {
	Scanner in=new Scanner(System.in);
	System.out.println("Enter the no of elements in the array "); 
	int n=in.nextInt();	
	int[] a=new int[n];
	System.out.println("Enter the numbers");
	for(int m=0;m<n;m++)
	{
		a[m]=in.nextInt();
	}
	//sort the array in ascending order using sort
	Arrays.sort(a);
	//print  the elements in descending order
	System.out.println("Array sorted in descending order");
for(int m=(a.length-1);m>=0;m--)

{
System.out.println(a[m]);	

}
	}
}
