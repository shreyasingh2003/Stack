# Stack
![image](https://user-images.githubusercontent.com/97290356/169874743-b90dee3f-9868-4ed5-9574-7c125cfff509.png)
*************************************************************************************************************************************************************************
import java.io.*;
class stck
{
private int arr[];
private int tos = -1;
stck(int x)
{
arr = new int[x];
}

void push(int x)
{
try{
if(tos == (arr.length)-1)
throw new Exception ("Overflow");
arr[++tos]=x;
System.out.println("Push operation is sucessfull");
}
catch(Exception o1)
{
System.out.println("Stack is full");
}
}
int pop()
{
try
{
if(tos<0)
throw new Exception("Underflow");
System.out.println("Element poped successfully");
return arr[tos--];

}
catch(Exception o1)
{
       
System.out.print("Underflow");
return -1;
}
}
void display()
{
System.out.println("The element present in the stack");
for(int i=tos;i>=0;i--)
{
System.out.println(arr[i]);
}
}
}
public class stack {

public static void main(String[] args)throws IOException
{
BufferedReader br1 = new BufferedReader(new InputStreamReader(System.in));
String ch = "y";
stck s1;
s1 = new stck(5);
System.out.println("***********MENU*********");
System.out.println("1. PUSH");
System.out.println("2. PULL");
System.out.println("3. DISPLAY");

do
{
System.out.println("Enter 1,2,3 from above menu");
int x = Integer.parseInt(br1.readLine());
switch(x)
{
case 1 : System.out.println("Enter the element to push");
        int elem =  Integer.parseInt(br1.readLine());
        s1.push(elem);
        break;
case 2: s1.pop();
       break;
case 3: s1.display();
       break;
}
System.out.print("Do you want to continue(y/n)");
ch = br1.readLine();
}while(ch.equals("y"));

}
}
