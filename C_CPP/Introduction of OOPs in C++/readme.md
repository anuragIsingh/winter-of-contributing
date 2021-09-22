<ul>
<li><b>Defination of OOP:</b></li>
<ol type="i">
<li>"Object oriented programming is an approach that provides a way of modularizing programs for creating copies of such modules on demand."</li>
<li>In object oriented programming, the program is designed around the data being operated upon rather than upon the operations themselves.</li>
<li>It ties data more closely to functions that operate on it. OOP's allows to decompose a problem into a number of entities called objects and then builds data and functions around these entities.
 </li>
<li>When a program is executed, the objects interact by sending messages to one another.</li>
<li>Each object contains data and code to manipulate the data.
</li>
</ol>
<li><b>Features of OOP's:</b></li></li>
<ol type="i">
<li>Emphasis is on data rather than procedure.</li>
<li>Programs are divided into number of objects.</li>
<li>Data is hidden and cannot be accessed by external functions.</li>
<li>New data and functions can be easily added wherever required.</li>
<li>Data structures are designed such that they characterize the objects.</li>
<li>Functions that operate on the data of an object are tied together in the data structure</li>
<li>Objects may communicate with each other through functions.New data and functions can be easily added wherever required.</li>
</ol>
<li><b>Concepts related to OOP's:</b></li>
<ol>
<li><b>Objects:</b></li>
<ol type="a">
<li>Objects are the basic runtime entities in object oriented system or we can say that an object is a variable whose datatype is class.</li>

   ` for eg. they may represent a person, place, a bank account or any item that the program must handle.`
<li>Programming problem is analyzed in terms of objects and the nature of communication between them.</li>
<li>Program objects should be chosen such that they match closely with the real-world objects.</li>
  <li>The objects can be declared as :</li>
 
` for eg. class-name object1-name, object2-name,.... and so on `

  
  <ul>Consider a class item defined as follows:<ul> 
  
    Syntax:
  ```  
    class item
    { 
    
     private:
    int number;
     public:
    int cost;
    void getdata(int a, int b ) //inline function
    {
    number=a;
    cost=b;
    }
    void show (void)
    {
    cout<<a<<b;
    }
    };
    void main()
    {
    item X;
    X.getdata(20,30);
    ..
    }
    
```
  Here item is a class with private variable number and public members cost, getdata (int , int) and show(). The X is an object of item.
`e.g. X.getdata (20, 30);`
  This declaration will apply values 20 and 30 to number and cost respectively.<br>
  Similarly public variables of class can be accessed within main() function.<br>
  But private variable cannot access inside main program, they can be accessed only by public functions of the same class.<br>
    
Instead of using function as X.getdata (20, 30), if directly apply 20 and 30 to number and cost in main program as :<br>
```
X.number = 20; //error
X.cost = 20;
```    

Then, there will be an error in first statement, because number is private member of class while there will be no error in second statement, because cost is public member of class.


</ol>
<li><b>Classes:</b></li>
<ol type="a">
    <li> Class is a way to bind data and its associated functions together.</li>
    <li> The entire set of data and code of an object can be made a user defined data type with the help of a class.</li>
    <li>In fact an object is nothing but a variable, whose data type is class.</li>
    <li>Once a class has been defined, user can define any number of objects belonging to that class.</li>
    <li>A class is a collection of objects of similar type.</li>
    <li>Generally a class specification has two parts :</li>
    <ol type="I">
        <li>Class Declaration.</li>
        <li>Class functions Defination</li>
      The class declaration describes the type of scope of its member whereas the class function definations describes how class functions are implemented.
    </ol>
    <li>Generally a class Declaration would look  like:</li>

       
            class item          //specify a class 
        {
            int number ;    //class data 
            float cost;
            public:
            voiid getdata (int a, float b);
            void put data (void);
        };

    


</ol>
<li><b>Inheritance:</b></li>
<ol type="a">
    <li>The mechanism of deriving a new class from an existing one is called as inheritance.</li>
    <li>Inheritance is the process by which objects of one class can acquire the properties of objects of another class.</li>
    <li>In OOP's's, inheritance stands for reusability. This means that additional features can be added to an existing class without modifying it.</li>
  The old class is referred as base class and new class is referred as derived class. The reuse of a class that has already been tested, debugged and used many times, can save the efforts of developing and testing the same again.
  
  The syntax of declaration of derived class is :
 
  Syntax:
```    
class derived class_name:visibility_mode base_class_name  
  {                                                      
  .....                                                                           
  .....      // Members of derived class                 
  .....                                                  
  };                                                     
  where visibility mode is optional and if present may be either private or public <br>
  
class base                                                   
  {                                                                 
public: void showbase()                                      
  {                                                          
cout<<"This is the base";                                                  
  }                                                          
  };                                                              
class derived : public base   //Declaration of derived class 
{                                                            
  public:                                                    
void showderived (void)                                             
  {                                                              
showbase (); //Base class function used                       
 cout<<"\n This is derived class";                             
  }                                                            
  };           
  
```
  
  
There are five types of inheritances in C++:                  <br>
 
  
  
  (i) Single inheritance :                                     <br>            
A derived class with only one base class is called as single inheritance.
  
  Syntax:
```  
  
  class A   // base class
{
    ..........
};
class B : acess_specifier A   // derived class
{
    ...........
} ;
```
  
  Here class A is a base class and class B is a chil class and  inherits properties of class A as it is derived from it 

  (ii) Multilevel inheritance :<br>
The mechanism of deriving one class from another derived class is multilevel inheritance.<br>
  
  
Syntax:
```  
 class A // base class
{
     ...........
};
class B : acess_specifier A // derived class
{
     ...........
 } ;
 class C : access_specifier B // derived from derived class B
 {
     ...........
 } ;                         
```
  
  Here class A is the base class and class B is drived from class A (inherits properties of class A)and so on class C is derived from class B(inherits properties of class B and A both as class B is derived from A)
  
  (iii) Multiple inheritance :<br>
When a class is derived from several base classes, it is called as multiple inheritance.<br>
  
Syntax:
```  
  class A
 {
   ..........
 };
 class B
 {
   ...........
  } ;
 class C : acess_specifier A,access_specifier B // derived class from A and B
 {
   ...........
 } ;
 ```
  
  Here there are two base class A and B from which class C is inherited. Therefore, derived class C inherits all the public members of A and B and retains their visibility.
  

(iv) Hierarchical inheritance :<br>
The traits of one class may be inherited by more than one classes. This process hierarchical inheritance.<br>
  
Syntax:
```  
  class A // base class
{
    ..............
};
class B : access_specifier A // derived class from A
{
    ...........
 } ;
 class C : access_specifier A // derived class from A
 {
    ...........
 } ;
 class D : access_specifier A // derived class from A
 {
     ...........
 } ;
 ```  
  Here  There is only one base class A from which three class B , C and D are derived.

All derived class have their own members as well as base class members.
  
(v) Hybrid inheritance :<br>  
 The inheritance which involves more than one inheritances is called as hybrid inheritance.
  
 Syntax:
 ``` 
  class A
{
     .........
};
class B : public A
{
     ..........
} ;
class C
{
     ...........
};
 class D : public B, public C
{
     ...........
};
```
  
  
  Here, class B is derived from class A which is single inheritance and then Class D is inherited from B and class C which is multiple inheritance. So single inheritance and multiple inheritance jointly results in hybrid inheritance.


</ol>
<li><b>Polymorphism:</b></li>
<ol type="a">
<li>Polymorphism is an important OOP's's concept, Polymorphism means ability to take more than one form.</li>
<li>Polymorphism plays an important role in allowing objects having different internal structures to share the same external interface.</li>
<li>This means that a general class of operations may be accessed in the same manner even though specific actions associated with each operation may differ.</li>
<li>Polymorphism is extensively used in implementing inheritance.</li>
  
  ```
  
                                                     Polymorphism
                                                            |
                                 _________________________________________________________         
                                |                                                         |
                                v                                                         v   
             Compile time polymorphism                                              Runtime polymorphism 
             _________________________                                                    _________
             |                        |                                                      |                          
             v                        v                                                      v                    
   Function overloading`         Operator overloading                                  Virtual function
  
  
  ```
### I) Compile Time Polymorphism:
  
1. Function overloading and operator overloading are the examples of compile time polymorphism.<br>
  
  
2. In this case, the overloaded member functions are selected for invoking by matching arguments, both type and number.
  
3. This information is known to the compiler at the compile time and, therefore the compiler is able to select the appropriate function for a particular call at the compile time itself.
  
This is known as compile time polymorphism.
  
4. Compile time polymorphism is also called as early binding or static binding or static linking. Early binding simply means that an object is bound to its function at compile time.
  
### II) Runtime polymorphism :
1. In some situations, it is nice to select appropriate member function to be invoked while the program is running. This is known as runtime polymorphism.<br>
  
  
   `eg consider a situation where the function name and prototype is the same in both the base and derived classes as shown in following class definitions.`
  
  
  ```
  
class A

  {
  int x;               // private by default.
public:
void show (void)       // show() in base class

  {...}
  };
  class B: public A
  {
int y;
  public:
void show (void)    // show() in derived class
  {...}
};
  ```
  
  Here, show() function is used to print values of object of both the classes A and B. The prototype of show() is the same in both the places, the function is not overloaded and therefore static binding does not apply.
  
 3.  In such situations, the appropriate member function can be selected at runtime and it is known as runtime polymorphism. 
 
  4.  To achieve runtime polymorphism, C++ supports mechanism of virtual functions. 
 
  5.  At runtime, it is known what class objects are under consideration, the appropriate version of function is called.
 
  6.  Since the function is linked with a particular class much after its compilation, this process is termed as late binding. It is also called as dynamic binding because the selection of the appropriate function is done dynamically at runtime.
  
 
  
  ### Concept Of Virtial Function <br>
  
1. When user use the  same function name in both the base and derived classes, the function in base class is declared as virtual using the      keyword 'virtual' preceding its normal declaration.
2. When a function is made virtual, C++ determines which function to use at runtime , based on the type of object pointed to by the base pointer.
3. Thus, by making the base pointer to point two different objects, it can execute diffrent versions of the virtual function.
4. Virtual functions can be accessed through the use of a pointer declared as a pointer to the base class.
5. Also, the prototypes of the base class version of a virtual function and all the derived class versions must be identical.
6. If two functions with the same name have different prototype, C++ considers them as overloaded functions, and the virtual function mechanism
   is ignored. 


  

  
  

</ol>
</ol>
</ul>


