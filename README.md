# IT314

NAME : SHIV BARIA

I'D  : 202001222

GOAL : The goal of this lab is to learn how to use JUnit to write unit tests for java programs.

The primary goal of unit testing is to take the smallest piece of testable software in an
application, isolate it from the remainder of the code, and determine whether or not it behaves
the way you expect it to behave. Each unit is tested separately before integrating it into the
rest of the program. In other words, classes should be tested in isolation from other classes
(test the methods of a class before you use the class elsewhere). Unit testing has proven its
value in that a large percentage of defects are identified during unit testing.

Lab Exercises

1. Create a new Eclipse project, and within the project create a package.

2. Create a class for a Boa. Here’s the code you can use (you may copy/paste):



![image](https://user-images.githubusercontent.com/124240818/233329716-c1d547b7-8df3-43d6-a463-c51d111cf20b.png)



3. Follow the instructions in the JUnit tutorial in the section “Creating a JUnit Test Case in
Eclipse”.i created a test case for the class Boa.select test method stubs, select both isHealthy() and fitsInCage(int).

4. Now it’s time to write some unit tests. Notice that the BoaTest class that JUnit created
for contains stubs for several methods. The first stub (for the method setUp()) is
annotated with @Before. The @Before annotation denotes that the method setUp()
will be run prior to the execution of each test method. setUp() is typically used to
initialize data needed by each test. Modify the setUp() method so that it creates a
couple of Boa objects, as follows:



![image](https://user-images.githubusercontent.com/124240818/233331296-f6d619d8-e840-48c8-943c-8854e8ace479.png)



5. JUnit also provided stubs for two test methods, each annotated with @Test. Work on
the testIsHealthy() method first. The purpose of this method is to check that the
isHealthy() method in the Boa class behaves the way it’s supposed to. In the JUnit
tutorial, read the section on “Writing Tests”. Modify the testIsHealthy() method so that
it checks the results of activating the isHealthy() method on the two Boa objects you
created in setup().

6. Now running test cases.



![image](https://user-images.githubusercontent.com/124240818/233332465-f3b59e63-efef-496f-8bfd-452dadf241c0.png)



7. Add a new method to the Boa class, with this purpose and signature:
// produces the length of the Boa in inches
public int lengthInInches(){
// you need to write the body of this method
}
Add a new test case to the BoaTest class that tests the lengthInInches() method.



![image](https://user-images.githubusercontent.com/124240818/233333473-62877621-4f5b-4c8c-86e0-0897be1b474f.png)



8. Here are some other things you should know about unit testing and JUnit:

Each method annotated with @Test will be run, but the order of the tests is not
guaranteed.

Any method annotated with @Before will be run before each test executes.

Any method annotated with @After will be run after each test executes.



