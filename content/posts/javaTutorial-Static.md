---
title: "#JavaBeginnerToAdvanced: 1- Static Keyword!"
date: 2023-03-31T23:23:00-03:00
draft: false
cover: 
    image: img/javaBeginerToAdvanced.jpg
    alt: 'This is a post image'
    caption: 'this is the caption'
---

---
#  Static Keyword!
### Understanding this keyword once and for all!

The static keyword is used for memory management. It can be used with variables methods, blocks and nested classes. The static keyword belongs to the class than an instance of the class. 
Variable static of the class has the same value for any object. You don’t need to creat object  to access it. It doesnt depends of a instance variable.
Static variables have a relationship with a class as a whole, while variables that are not static are associated with a specific class instance (object) and can manipulate as the object's instance variable.

The static variable can be used to refer to the common property of all objects (which is not unique for each object), for example, the company name of employees, college name of students, etc. 

The static variable gets memory only once in the class area at the time of class loading. It makes your program memory efficient 

Example 1:                                                                                                                
In this example, we have created an instance variable named count which is incremented in the constructor. Since instance variable gets the memory at the time of object creation, each object will have the copy of the instance variable. If it is incremented, it won't reflect other objects. So each object will have the value 1 in the count variable. 



       //Java Program to demonstrate the use of an instance variable  
       //which get memory each time when we create an object of the class.  
       class Counter{  
       int count=0;//will get memory each time when the instance is created  
         
       Counter(){  
       count++;//incrementing value  
       System.out.println(count);  
         
       
       public static void main(String args[]){  
       //Creating objects  
       Counter c1=new Counter();  
       Counter c2=new Counter();  
       Counter c3=new Counter();    

        
        Output: 
        1
        1
        1


As we have mentioned above, static variable will get the memory only once, if any object changes the value of the static variable, it will keep its value. 

       //Java Program to illustrate the use of static variable which  
       //is shared with all objects.  
       class Counter2{  
       static int count=0;//will get memory only once and retain its value  
         
       Counter2(){  
       count++;//incrementing the value of static variable  
       System.out.println(count);  
         
         
       public static void main(String args[]){  
       //creating objects  
       Counter2 c1=new Counter2();  
       Counter2 c2=new Counter2();  
       Counter2 c3=new Counter2();  
       }  
       }  
        output:
        1
        2
        3

Example 2:

Since static variables belong to a class, we can access them directly using the class name. So, we don't need any object reference.

        public class ClasseAuxilio {
            public static int resultado(int num1, int num2){
                return (num1 + num2);
            }
            static int danilo = 8;
        }}

MAIN:

        System.out.println("Hello, World1!" + ClasseAuxilio.danilo);