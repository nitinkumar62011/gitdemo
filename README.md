1111.Write a Java program to use String/Wrapper class and its methods.
• Program how to wrie the code
import java.lang.*;
import java.util.*;
public class MyClass {
 public static void main(String args[]) {
 String s1="Java";
 char ch[]={'s','t','r','i','n','g','s'};
 String s2= new String(ch);
 String s3="Hello";
 String s4="hello";
 String s5="flag";
 String s6="Hi How are you?";
 String s7="";
 String s8="Hello";
 //String Concatenation function
 s1=s1.concat(" is a programming language ");
 System.out.println(s1);
 //charAt function
 char ch1=s1.charAt(2);
 System.out.println(ch1);
 //length function
 System.out.println("length of s1 is "+s1.length());
 //substring function
 System.out.println(s1.substring(1,2));
 System.out.println(s1.substring(2));
 //equals function
 System.out.println(s3.equals(s4));
 if(s3.equals(s4))
 System.out.println("Both are equal");
 else
 System.out.println("Both are not equal");
 //isEmpty function
 System.out.println(s7.isEmpty());
 System.out.println(s7.isEmpty());
 //equalsIgnoreCase function
 System.out.println(s3.equalsIgnoreCase(s8));
 System.out.println(s1.equalsIgnoreCase(s2));
 //indexOf function
 int index=s6.indexOf("you");
 System.out.println("index of substring (you) in s6 is "+index);
 //lastIndexOf function
 int Lindex=s6.lastIndexOf('o');
 System.out.println("Last index of character (o) in s6 is "+Lindex);
 //trim function
 System.out.println(s1+" javapoint");
 System.out.println(s1.trim()+"javapoint");
 //startsWith function
 System.out.println(s6.startsWith("Hi"));
 //endsWith function
 System.out.println(s6.endsWith("?"));
 //replace function
 System.out.println(s6.replace("Hi","Hello"));
 System.out.println(s6.replace('e','i'));
 //toUpperCase function
 System.out.println(s6.toUpperCase());
 //toLowerCase function
 System.out.println(s6.toLowerCase());
 }
}
• Output
true
true
true
false
index of substring (you) in s6 is 11
Last index of character (o) in s6 is 12
Java is a programming language javapoint
Java is a programming languagejavapoint
true
true
Hello How are you?
Hi How ari you?
HI HOW ARE YOU?
hi how are you?
• Output Screenshot
2. Write a Java program to implement interface through Collection.
• Program
import java.lang.*;
import java.util.*;
public class MyClass {
 public static void main(String args[]) {
 //Array List
 ArrayList<String> al=new ArrayList<String>();
 al.add("ab");
 al.add("bc");
 al.add("ca");
 System.out.println(al);

 //Linked List
 LinkedList<String> ll=new LinkedList<String>();
 ll.add("a");
 ll.add("b");
 ll.add("c");
 ll.addLast("Z");
 ll.addFirst("A");
 System.out.println(ll);

 //Hash Set
 HashSet<String> hs=new HashSet<String>();
 hs.add("B");
 hs.add("A");
 hs.add("D");
 System.out.println(hs);
 
 //Linked Hash Set
 LinkedHashSet<String> lhs=new LinkedHashSet<String>();
 lhs.add("Y");
 lhs.add("M");
 lhs.add("N");
 System.out.println(lhs);

 //Tree Set
 TreeSet<String> ts=new TreeSet<String>();
 ts.add("Ravi");
 ts.add("surya");
 Iterator itr=ts.iterator();
 while(itr.hasNext())
 {
 System.out.println(itr.next());
 }

 //Priority Queue
 PriorityQueue<String> pq=new PriorityQueue<String>();
 pq.add("JAVA");
 pq.add("PROGRAM");
 pq.add("NCET");
 System.out.println("At head of Queue "+pq.element());
 System.out.println("At head of Queue "+pq.peek());
 System.out.println("Iterating element:");
 Iterator it=pq.iterator();
 while(it.hasNext())
 {
 System.out.println(it.next());
 }
 pq.remove();
 pq.poll();
 System.out.println("After removing two element");
 Iterator it2=pq.iterator();
 while(it2.hasNext())
 {
 System.out.println(it2.next());
 }
 }
}
• Output
[ab, bc, ca]
[A, a, b, c, Z]
[A, B, D]
[Y, M, N]
Ravi
surya
At head of Queue JAVA
At head of Queue JAVA
Iterating element:
JAVA
PROGRAM
NCET
After removing two element
PROGRAM
• Output Screenshot
3. Write a Java program to access a collection through an iterator.
• Program
import java.lang.*;
import java.util.*;
public class MyClass {
 public static void main(String args[]) {
 //Array List
 ArrayList<String> al=new ArrayList<String>();
 al.add("ab");
 al.add("bc");
 al.add("ca");
 System.out.println(al);
 //Iterator class
 Iterator itr=al.iterator();
 while(itr.hasNext())
 {
 System.out.println(itr.next()+" ");
 }
 //List Iterator class
 ListIterator litr=al.listIterator();
 while(litr.hasNext())
 {
 System.out.println(litr.next()+" ");
 }
 while(litr.hasPrevious())
 {
 System.out.println(litr.previous()+" ");
 }
 //using for-each
 LinkedList<String> ll=new LinkedList<String>();
 ll.add("a");
 ll.add("b");
 ll.add("c");
 for(String str:ll)
 {
 System.out.println(str+" ");
 }
 }
}
• Output
[ab, bc, ca]
ab
bc
ca
ab
bc
ca
ca
bc
ab
a
b
c
• Output Screenshot
4. Write a Java program to print word count of a file using Stream I/O.
• Program
import java.io.*;
public class MyClass
{
 public static void main(String args[])throws IOException
 {
 String line;
 int count=0;
 //open a file in read mode
 FileReader file=new FileReader("data.text");
 BufferedReader br=new BufferedReader(file);
 //Get each line till end of file
 while((line=br.readLine())!=null)
 {
 String words[]=line.split(" ");
 count=count+words.length;
 }
 System.out.println("Number of words in file is "+count);
 br.close();
 }
}
• Output
Number of words in file is 0
