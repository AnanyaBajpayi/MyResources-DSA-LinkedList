A class is the blueprint of an object.\endl
In intellij idea,create a maven project.Inside it if you want to add any class,go to src->main->java, create a Java class using 'currentpackagename.Main1'(org.studyeasy.Main1).
In the new class suppose you create a class 'Car' with instance variables.if the variable is public then you can access in other classes.If the variable is private you cannot access in any other class.
In order to create getter and setter methods ,go to Code section at the top,click on generate,you have the option of getter and setter.
If you create an instance variable and a parameter variable with same name and you dont use this keyword,then even after initializing your instance variable via a setter method,if u print its value using a getter method ,youll get its default values only.
Instance variables have a default value.But a variable created inside a block doesnt.So if you create an instance variable public int a; it is fine but if you create a normal variable inside any method like int a; and do not initialize it and try to print it,it will give error.This is because a default constructor initializes the instance variables.
this.doors=doors;//this keyword symbolises the instance variable
It is preferred to initialize the instance variable using a constructor.
Default constructor is created if we do not specifically create a constructor.
3 types of constructor:default,parameterized,non parameterized.If we dont have a constructor,java will insert.If we have any type of constructer,java wont insert.
Inheritence:Child classes inherit data member and member objects from the parent class.
eg we have a parent class called Vehicles,it has three child classes-Bike,Car and Truck.To use it we use extends(eg Bike extends Vehicles).super method passses the value assigned in some child class constructor to parent class.
tostring() helps in directly printing the information.If you also want parent class info then use toString()+superTostring() from drop down of tostring.
In case of method conflict ,i.e, same name classes in child and parent class,the child class wins.
Types of inheritence:Single inheritence(A->B),Multiple inheritence(A->C & B->C)(Not allowed in java),Multilevel inheritence(A->B->C),Heirchichal inheritence(A->B,A->C,A->D),Hybrid inheritence.
A composition is a complex object of multiple components.For example we create a class called Car.It has several properties like no of seats,no of wheels,engine info,battery info,etc.Now no of seats and wheels is a simple property and can be denoted by a variable.But engine info and battery info is a class.
