# OOP-exercises

## Exercise 1

1. Create a class called "ConsoleHandler"
2. Give it a method called "askUser" with the parameter "String query"
    - The return value of the method should be the answer to the query
  
```java
  ConsoleHandler consoleHandler = new ConsoleHandler();
  String address = consoleHandler.askUser("Where do you live?"); // Should print string to console and return result of scanner.nextLine();
```
3. In the class ConsoleHandler add a method called "askForInteger" with the parameter "String query"
```java
  ConsoleHandler consoleHandler = new ConsoleHandler();
  String address = consoleHandler.askUser("Where do you live?");
  int age = consoleHandler.askForInteger("How old are you?");
```

### Level up 1.1

In ConsoleHandler implement a method called "askForList" which lets you keep adding items to a list until you write an empty string
```java
  ConsoleHandler consoleHandler = new ConsoleHandler();
  List<String> items = consoleHandler.askForList("What items do you wish to add?"); // Returns a list when user presses enter without entering a next item
```

- - -

## Exercise 2

Create a class called Dice and add following methods. Size represents the maximum numbers of dice eyes.

1. setMaxSize(int maxSize);
2. setMinSize(int minSize);
3. throwDice(int size); // Should be limited by values from min and max size

```java
Dice dice = new Dice();
dice.setMinSize(5);
dice.setMaxSize(10);

dice.throwDice(15); // Should be maximum 10
```

## Level up 2.1

In Dice add a method called "throwDice*s*".
When invoked it should return a list of results from throwing multiple dices
```java
  Dice dice = new Dice();
  List<Integer> result = dice.throwDices(3); // returns a list of results from 3 dice throws
```

- - -

## Exercise 3

1. Create a class human with the properties name, address, phone number - choose suitable datatypes for respective properety.
2. Create a list containting the human datatype.
3. Add a few imaginary humans to the list
4. Create a function that prints every human's name, address and phone number

### Level up 3.1

Create a class responsible for printing details about humans.
Example class name "HumanConsoleWriter".

*Example methods*
```java
void writeNames(List<Human> humanList); //Print all the names in the argument humanList
void writeAll(List<Human> humanList); //Write all details about all humans as in step 4 above.
```
    
### Level up 3.2
    
Create a class responsible for relating people together by either address or phone numbers
Example class name "HumanAgency"

*Example methods*
```java
List<Human> findHumansOnAddress(String address); // Return a list of people at the address
List<Human> findHumansWithPhoneNumber(String phoneNumber); // Return a list of people with the same phone number
```

Extend the program to use the result from HumanAgency to pass it to HumanConsoleWriter which then prints the details of the found people.

  
