# LEARN DART

## Content

1. Introduction and Basics
2. Conditions and Loops
3. Functions in Dart
4. Collections in Dart
5. File Handling in Dart
6.OOP in Dart
7.Null Safety In Dart
8.Asynchronous Programming
9.Useful Information
   Final Vs Const
   Datetime In Dart
   Extension In Dart
   Backend in Dart
10.Dart how to
   Convert String to Int
   Generate Random Number
   Capitalize First Character
   Make Http Request in Dart
---

## 1. Introduction and Basics

Dart is a client-optimized, object-oriented, modern programming language to build apps fast for many platforms like Android, iOS, web, desktop, etc.

Currently, Dart is one of the most preferred languages to learn. A solid understanding of Dart is necessary to develop high-quality apps with flutter. According to Github, Dart is one of the most loved programming languages in the world.

If you know languages like C, Java, C#, Javascript, etc., Dart will be easy for you. This tutorial covers Dart from basic to advance.

### Dart Features
- Free and open-source.
- Object-oriented programming language.
- Used to develop Android, iOS, web, and desktop apps fast.
- Can compile to either native code or javascript.
- Offers modern programming features like null safety and asynchronous programming.
- You can even use Dart for servers and backend.

---

## Difference Between Dart & Flutter

- Dart is a client optimized, object-oriented programming language. It is popular nowadays because of Flutter. It is difficult to build complete apps only using Dart because you have to manage many things yourself.
- Flutter is a framework that uses the Dart programming language. With the help of Flutter, you can build apps for Android, iOS, web, desktop, etc. The framework contains ready-made tools to make apps faster.

---

## Dart Concepts Examples

### Example 1: Using for loop condition for repeated print statement

```dart
void main() {
  for (var i = 0; i < 10; i++) {
    print('hello \\${i + 1}');
  }
}
```

**Output:**
```
hello 1
hello 2
hello 3
hello 4
hello 5
hello 6
hello 7
hello 8
hello 9
hello 10
using for loop got print statement as repeatedly for 10 times as limit given in for loop condition.
```

---

### Example 2: Getting 20th fibonacci number

```dart
void main() {
  const i = 20;
  print('fibonacci(\$i) = \\${fibonacci(i)}');
}

/// Computes the nth Fibonacci number.
int fibonacci(int n) {
  return n < 2 ? n : (fibonacci(n - 1) + fibonacci(n - 2));
}
```

**Output:**
```
fibonacci(20) = 6765
```

---

### Example 3: How to declare variables and print variable values

```dart
void main() {
  // declaring variables
  String name = "John";
  String address = "USA";  
  num age = 20; // used to store any types of numbers 
  num height = 5.9;
  bool isMarried = false;
   
  // printing variables value   
  print("Name is \$name");
  print("Address is \$address");
  print("Age is \$age");
  print("Height is \$height");
  print("Married Status is \$isMarried");
}
```

**Output:**
```
Name is John
Address is USA
Age is 20
Height is 5.9
Married Status is false
```

---

## Operators

### Example 4: Using operators made addition, subtraction and division of two numbers.

```dart
void main() {
 // declaring two numbers 
 int num1=10;
 int num2=3;
 
 // performing arithmetic calculation
 int sum=num1+num2;       // addition
 int diff=num1-num2;      // subtraction
 int unaryMinus = -num1;    // unary minus  
 int mul=num1*num2;       // multiplication
 double div=num1/num2;    // division
 int div2 =num1~/num2;     // integer division
 int mod=num1%num2;       // show remainder
 
//Printing info 
 print("The addition is \$sum.");
 print("The subtraction is \$diff.");
 print("The unary minus is \$unaryMinus.");
 print("The multiplication is \$mul.");
 print("The division is \$div.");
 print("The integer division is \$div2.");
 print("The modulus is \$mod."); 
}
```

**Output:**
```
The addition is 13.
The subtraction is 7.
The unary minus is -10.
The multiplication is 30.
The division is 3.3333333333333335.
The integer division is 3.
The modulus is 1.
```

---

## Built-in-types

### Example 5: Using built in type concept used int, double, list as example code.

```dart
void main() {
  print('--- 1. Constructors and Static Methods as Functions ---');

  // Example: int.parse (static method)
  // It takes a String and returns an int.
  final String numString = '123';
  final int parsedInt = int.parse(numString);
  print('Parsed int from "$numString": $parsedInt (Type: ${parsedInt.runtimeType})');

  // Example: double.tryParse (static method)
  // It tries to parse a String to a double, returning null if unsuccessful.
  final String doubleString = '3.14';
  final double? parsedDouble = double.tryParse(doubleString);
  print('Parsed double from "$doubleString": $parsedDouble (Type: ${parsedDouble?.runtimeType})');

  final String invalidDoubleString = 'hello';
  final double? invalidParsedDouble = double.tryParse(invalidDoubleString);
  print('Parsed double from "$invalidDoubleString": $invalidParsedDouble'); // null

  // Example: String.fromCharCode (static method)
  // It takes an int (Unicode code unit) and returns a String.
  final String charA = String.fromCharCode(65); // ASCII for 'A'
  final String smiley = String.fromCharCode(0x1F600); // Unicode for grinning face
  print('Char from code 65: "$charA"');
  print('Char from code 0x1F600: "$smiley"');

  // Example: List.from (named constructor)
  // It takes an Iterable and creates a new List from its elements.
  final Set<int> originalSet = {10, 20, 30};
  final List<int> listFromSet = List.from(originalSet);
  print('List created from Set: $listFromSet (Type: ${listFromSet.runtimeType})');

  // Example: DateTime.now (factory constructor)
  // It creates a new DateTime object representing the current time.
  final DateTime now = DateTime.now();
  print('Current DateTime: $now (Type: ${now.runtimeType})');

  // Example: RegExp (constructor)
  // Creates a regular expression object.
  final RegExp emailRegex = RegExp(r'^\S+@\S+\.\S+$');
  print('Is "test@example.com" a valid email? ${emailRegex.hasMatch('test@example.com')}');
  print('Is "invalid-email" a valid email? ${emailRegex.hasMatch('invalid-email')}');
}
```

**Output:**
```
---- 1. Constructors and Static Methods as Functions ---
Parsed int from "123": 123 (Type: int)
Parsed double from "3.14": 3.14 (Type: double)
Parsed double from "hello": null
Char from code 65: "A"
Char from code 0x1F600: "😀"
List created from Set: [10, 20, 30] (Type: List<int>)
Current DateTime: 2025-10-27 17:17:44.507 (Type: DateTime)
Is "test@example.com" a valid email? true
Is "invalid-email" a valid email? false
```

---

## Collections

### Example 6: In collection used list concept as example

```dart
void main() {
  // 1. Declaring and initializing a List
  // A List of Strings (explicit type)
  List<String> fruits = ['Apple', 'Banana', 'Orange'];
  print('Initial fruits: $fruits');

  // A List of integers (type inferred)
  var numbers = [10, 20, 30, 40];
  print('Initial numbers: $numbers');

  // 2. Adding elements
  fruits.add('Mango'); // Add a single element
  fruits.addAll(['Pineapple', 'Grapes']); // Add multiple elements from another iterable
  print('Fruits after adding: $fruits');

  // 3. Accessing elements by index
  // List indices are 0-based
  print('First fruit: ${fruits[0]}');
  print('Second number: ${numbers[1]}');
  // print(fruits[10]); // This would throw a RangeError if index is out of bounds

  // 4. Getting the length of the list
  print('Number of fruits: ${fruits.length}');

  // 5. Checking if a list contains an element
  print('Does fruits contain "Banana"? ${fruits.contains('Banana')}');
  print('Does fruits contain "Kiwi"? ${fruits.contains('Kiwi')}');

  // 6. Iterating over a list
  print('\n--- Iterating through fruits ---');
  for (String fruit in fruits) {
    print('I love $fruit!');
  }

  print('\n--- Iterating with index ---');
  for (int i = 0; i < numbers.length; i++) {
    print('Number at index $i is ${numbers[i]}');
  }

  // Using forEach (common for simple iteration)
  print('\n--- Using forEach for numbers ---');
  numbers.forEach((number) => print('Value: $number'));


  // 7. Removing elements
  fruits.remove('Orange'); // Remove by value (removes first occurrence)
  print('Fruits after removing "Orange": $fruits');

  fruits.removeAt(0); // Remove by index (removes 'Apple' which was at index 0)
  print('Fruits after removing at index 0: ${fruits}');

  // 8. Checking if a list is empty
  print('Is fruits list empty? ${fruits.isEmpty}');
  print('Is numbers list empty? ${numbers.isEmpty}');

  // 9. Clearing the list
  numbers.clear();
  print('Numbers after clearing: $numbers');
  print('Is numbers list empty now? ${numbers.isEmpty}');

  // 10. Creating a list of mixed types (generally discouraged, use specific types)
  var mixedList = [1, 'hello', true, 3.14];
  print('\nMixed list: $mixedList');
  print('Type of first element: ${mixedList[0].runtimeType}');
}
```

**Output:**
```
Initial fruits: [Apple, Banana, Orange]
Initial numbers: [10, 20, 30, 40]
Fruits after adding: [Apple, Banana, Orange, Mango, Pineapple, Grapes]
First fruit: Apple
Second number: 20
Number of fruits: 6
Does fruits contain "Banana"? true
Does fruits contain "Kiwi"? false

--- Iterating through fruits ---
I love Apple!
I love Banana!
I love Orange!
I love Mango!
I love Pineapple!
I love Grapes!

--- Iterating with index ---
Number at index 0 is 10
Number at index 1 is 20
Number at index 2 is 30
Number at index 3 is 40

--- Using forEach for numbers ---
Value: 10
Value: 20
Value: 30
Value: 40
Fruits after removing "Orange": [Apple, Banana, Mango, Pineapple, Grapes]
Fruits after removing at index 0: [Banana, Mango, Pineapple, Grapes]
Is fruits list empty? false
Is numbers list empty? false
Numbers after clearing: []
Is numbers list empty now? true

Mixed list: [1, hello, true, 3.14]
Type of first element: int
```

---

### Example 7: Sets topic example

```dart
import 'dart:collection'; // Needed for UnmodifiableSetView, though Set.unmodifiable is built-in.

void main() {
  print("--- Demonstrating Dart Sets ---");

  // 1. Declaration and Initialization
  // Sets are declared using curly braces {}
  // If you declare an empty Set using {}, Dart infers it as a Map by default.
  // To declare an empty Set, you must specify the type explicitly.

  // A Set of Strings with initial values
  Set<String> fruits = {'Apple', 'Banana', 'Orange', 'Apple'}; // 'Apple' will only be stored once
  print("\n1. Initial Set of fruits: $fruits"); // Output: {Apple, Banana, Orange} (order not guaranteed)

  // An empty Set of Integers
  Set<int> numbers = {}; // This is a correct way to declare an empty Set
  print("   Initial empty Set of numbers: $numbers");

  // You can also create a Set from a List, which will automatically remove duplicates
  List<int> numbersWithDuplicates = [1, 2, 3, 2, 4, 1, 5];
  Set<int> uniqueNumbers = numbersWithDuplicates.toSet();
  print("   Set created from list [1, 2, 3, 2, 4, 1, 5]: $uniqueNumbers"); // Output: {1, 2, 3, 4, 5}

  // 2. Adding elements to a Set
  numbers.add(10);
  numbers.add(20);
  numbers.add(30);
  print("\n2. Numbers after adding 10, 20, 30: $numbers");

  // Adding an existing element has no effect (Sets only store unique values)
  numbers.add(20);
  print("   Numbers after trying to add 20 again: $numbers (no change)");

  // 3. Adding multiple elements using addAll()
  Set<String> moreFruits = {'Grape', 'Pineapple', 'Apple'}; // 'Apple' is a duplicate
  fruits.addAll(moreFruits);
  print("\n3. Fruits after adding moreFruits (Grape, Pineapple, Apple): $fruits");
  print("   Note: 'Apple' was only added once, 'Orange' might have changed position.");

  // 4. Checking if an element exists using contains()
  print("\n4. Does fruits contain 'Banana'? ${fruits.contains('Banana')}");
  print("   Does fruits contain 'Mango'? ${fruits.contains('Mango')}");

  // 5. Removing elements using remove()
  fruits.remove('Orange');
  print("\n5. Fruits after removing 'Orange': $fruits");
  fruits.remove('Mango'); // Removing a non-existent element has no effect
  print("   Fruits after trying to remove 'Mango': $fruits (no change)");

  // 6. Iterating through a Set
  print("\n6. Iterating through fruits:");
  for (String fruit in fruits) {
    print("   - $fruit");
  }

  // 7. Set Operations: union, intersection, difference
  Set<int> setA = {1, 2, 3, 4, 5};
  Set<int> setB = {4, 5, 6, 7, 8};
  print("\n7. Set Operations:");
  print("   Set A: $setA");
  print("   Set B: $setB");

  // Union: All unique elements from both sets
  Set<int> unionSet = setA.union(setB);
  print("   Union (A union B): $unionSet"); // Output: {1, 2, 3, 4, 5, 6, 7, 8}

  // Intersection: Elements common to both sets
  Set<int> intersectionSet = setA.intersection(setB);
  print("   Intersection (A intersect B): $intersectionSet"); // Output: {4, 5}

  // Difference: Elements in setA but not in setB
  Set<int> differenceSetAB = setA.difference(setB);
  print("   Difference (A minus B): $differenceSetAB"); // Output: {1, 2, 3}

  // Difference: Elements in setB but not in setA
  Set<int> differenceSetBA = setB.difference(setA);
  print("   Difference (B minus A): $differenceSetBA"); // Output: {6, 7, 8}

  // 8. Set Properties: length, isEmpty, isNotEmpty
  print("\n8. Set Properties:");
  print("   Number of fruits: ${fruits.length}");
  print("   Is fruits set empty? ${fruits.isEmpty}");
  print("   Is fruits set not empty? ${fruits.isNotEmpty}");

  Set<String> emptySet = {};
  print("   Is emptySet empty? ${emptySet.isEmpty}");

  // 9. Clearing a Set
  fruits.clear();
  print("\n9. Fruits after clearing: $fruits");
  print("   Is fruits set empty now? ${fruits.isEmpty}");

  // 10. Unmodifiable Set (Read-only)
  // You can create a set that cannot be modified after creation.
  // Attempts to modify it will result in an UnsupportedError.
  Set<String> constantFruits = Set.unmodifiable({'Apple', 'Banana', 'Cherry'});
  print("\n10. Unmodifiable Set: $constantFruits");
  // Uncomment the line below to see the error:
  // constantFruits.add('Date'); // Throws UnsupportedError at runtime

  // You can also create an unmodifiable view of an existing (mutable) set.
  // Changes to the underlying mutable set *will* be reflected in the view,
  // but the view itself cannot be used to modify the set.
  Set<String> mutableSet = {'A', 'B'};
  Set<String> unmodifiableView = UnmodifiableSetView(mutableSet);
  print("   Mutable Set: $mutableSet");
  print("   Unmodifiable view of mutableSet: $unmodifiableView");

  mutableSet.add('C'); // Modify the underlying mutable set
  print("   Mutable Set after adding 'C': $mutableSet");
  print("   Unmodifiable view after mutableSet change: $unmodifiableView (reflects 'C')");

  // Uncomment the line below to see the error:
  // unmodifiableView.add('D'); // Throws UnsupportedError
}
```

**Output:**
```
--- Demonstrating Dart Sets ---

1. Initial Set of fruits: {Apple, Banana, Orange}
   Initial empty Set of numbers: {}
   Set created from list [1, 2, 3, 2, 4, 1, 5]: {1, 2, 3, 4, 5}

2. Numbers after adding 10, 20, 30: {10, 20, 30}
   Numbers after trying to add 20 again: {10, 20, 30} (no change)

3. Fruits after adding moreFruits (Grape, Pineapple, Apple): {Apple, Banana, Orange, Grape, Pineapple}
   Note: 'Apple' was only added once, 'Orange' might have changed position.

4. Does fruits contain 'Banana'? true
   Does fruits contain 'Mango'? false

5. Fruits after removing 'Orange': {Apple, Banana, Grape, Pineapple}
   Fruits after trying to remove 'Mango': {Apple, Banana, Grape, Pineapple} (no change)

6. Iterating through fruits:
   - Apple
   - Banana
   - Grape
   - Pineapple

7. Set Operations:
   Set A: {1, 2, 3, 4, 5}
   Set B: {4, 5, 6, 7, 8}
   Union (A union B): {1, 2, 3, 4, 5, 6, 7, 8}
   Intersection (A intersect B): {4, 5}
   Difference (A minus B): {1, 2, 3}
   Difference (B minus A): {6, 7, 8}

8. Set Properties:
   Number of fruits: 4
   Is fruits set empty? false
   Is fruits set not empty? true
   Is emptySet empty? true

9. Fruits after clearing: {}
   Is fruits set empty now? true

10. Unmodifiable Set: {Apple, Banana, Cherry}
   Mutable Set: {A, B}
   Unmodifiable view of mutableSet: {A, B}
   Mutable Set after adding 'C': {A, B, C}
   Unmodifiable view after mutableSet change: {A, B, C} (reflects 'C')
```

---

### Example 8: Using map collection showing example code to add, remove, update etc of keys and values.

```dart
void main() {
  // 1. Declaring and Initializing a Map
  // Syntax: Map<KeyType, ValueType> mapName = {key1: value1, key2: value2};
  // Here, keys are String (product names) and values are double (prices).
  Map<String, double> productPrices = {
    'Laptop': 1200,
    'Mouse': 25.50,
    'Keyboard': 75,
    'Monitor': 300,
  };

  print('--- Initial Product Prices ---');
  print(productPrices);
  print('Number of products: ${productPrices.length}');

  // 2. Accessing elements
  // You access values using their corresponding keys, similar to array indexing.
  print('\n--- Accessing Elements ---');
  print('Price of Laptop: \$${productPrices['Laptop']}');
  print('Price of Keyboard: \$${productPrices['Keyboard']}');

  // If a key doesn't exist, it returns null.
  print('Price of Speakers (non-existent): ${productPrices['Speakers']}');

  // 3. Adding new elements
  // You can add new key-value pairs by assigning a value to a new key.
  print('\n--- Adding New Elements ---');
  productPrices['Webcam'] = 50;
  productPrices['External SSD'] = 150;
  print('After adding Webcam and External SSD:');
  print(productPrices);

  // 4. Updating an existing element
  // If you assign a value to an existing key, it updates the old value.
  print('\n--- Updating an Existing Element ---');
  productPrices['Mouse'] = 29.99; // Mouse price increased!
  print('After updating Mouse price:');
  print(productPrices);

  // 5. Removing an element
  // Use the `remove()` method with the key you want to remove.
  print('\n--- Removing an Element ---');
  productPrices.remove('Keyboard');
  print('After removing Keyboard:');
  print(productPrices);
  print('Number of products now: ${productPrices.length}');

  // 6. Checking if a key or value exists
  print('\n--- Checking for Keys/Values ---');
  print('Does "Laptop" exist as a key? ${productPrices.containsKey('Laptop')}');
  print('Does "Speakers" exist as a key? ${productPrices.containsKey('Speakers')}');
  print('Does any product cost \$150.00? ${productPrices.containsValue(150.00)}');
  print('Does any product cost \$1000.00? ${productPrices.containsValue(1000.00)}');

  // 7. Getting all keys and values
  print('\n--- Getting all Keys and Values ---');
  print('All Product Names (Keys): ${productPrices.keys}');
  print('All Prices (Values): ${productPrices.values}');

  // 8. Iterating over a Map
  print('\n--- Iterating Over a Map ---');

  // Method 1: Using forEach with a lambda function
  print('Using forEach:');
  productPrices.forEach((productName, price) {
    print('$productName costs \$${price.toStringAsFixed(2)}');
  });

  // Method 2: Using a for-in loop with `entries`
  print('\nUsing for-in loop with entries:');
  for (var entry in productPrices.entries) {
    print('${entry.key}: \$${entry.value.toStringAsFixed(2)}');
  }

  // Method 3: Iterating over keys and then accessing values
  print('\nUsing for-in loop over keys:');
  for (String product in productPrices.keys) {
    print('$product: \$${productPrices[product]!.toStringAsFixed(2)}');
    // The `!` (null assertion operator) is used here because productPrices[product]
    // is guaranteed not to be null when iterating over existing keys.
  }

  // 9. Creating an empty map
  print('\n--- Creating an Empty Map ---');
  Map<String, int> inventory = {}; // Or Map<String, int> inventory = new Map();
  print('Empty inventory map: $inventory');
  inventory['Apples'] = 10;
  inventory['Bananas'] = 15;
  print('Inventory after adding items: $inventory');
  print('Is inventory empty? ${inventory.isEmpty}');
  inventory.clear(); // Clears all entries from the map
  print('Inventory after clearing: $inventory');
  print('Is inventory empty now? ${inventory.isEmpty}');
}
```

**Output:**
```
---- Initial Product Prices ---
{Laptop: 1200, Mouse: 25.5, Keyboard: 75, Monitor: 300}
Number of products: 4

--- Accessing Elements ---
Price of Laptop: $1200
Price of Keyboard: $75
Price of Speakers (non-existent): null

--- Adding New Elements ---
After adding Webcam and External SSD:
{Laptop: 1200, Mouse: 25.5, Keyboard: 75, Monitor: 300, Webcam: 50, External SSD: 150}

--- Updating an Existing Element ---
After updating Mouse price:
{Laptop: 1200, Mouse: 29.99, Keyboard: 75, Monitor: 300, Webcam: 50, External SSD: 150}

--- Removing an Element ---
After removing Keyboard:
{Laptop: 1200, Mouse: 29.99, Monitor: 300, Webcam: 50, External SSD: 150}
Number of products now: 5

--- Checking for Keys/Values ---
Does "Laptop" exist as a key? true
Does "Speakers" exist as a key? false
Does any product cost $150.00? true
Does any product cost $1000.00? false

--- Getting all Keys and Values ---
All Product Names (Keys): (Laptop, Mouse, Monitor, Webcam, External SSD)
All Prices (Values): (1200, 29.99, 300, 50, 150)

--- Iterating Over a Map ---
Using forEach:
Laptop costs $1200.00
Mouse costs $29.99
Monitor costs $300.00
Webcam costs $50.00
External SSD costs $150.00

Using for-in loop with entries:
Laptop: $1200.00
Mouse: $29.99
Monitor: $300.00
Webcam: $50.00
External SSD: $150.00

Using for-in loop over keys:
Laptop: $1200.00
Mouse: $29.99
Monitor: $300.00
Webcam: $50.00
External SSD: $150.00

--- Creating an Empty Map ---
Empty inventory map: {}
Inventory after adding items: {Apples: 10, Bananas: 15}
Is inventory empty? false
Inventory after clearing: {}
Is inventory empty now? true
```

---

## Control Flow Statements

### Branches: if, if-case, switch

### Example 9: Using if stament showing grades according to percentage.

```dart
void main() {
  print("--- Grading System (using only 'if' statements) ---");
  print("This program demonstrates how to replace an 'if-else if-else' chain");
  print("with multiple independent 'if' statements by making each condition mutually exclusive.\n");

  // Test scores
  processScore(95);   // Should be A
  processScore(82);   // Should be B
  processScore(70);   // Should be C
  processScore(65);   // Should be D
  processScore(55);   // Should be F
  processScore(100);  // Should be A (edge case)
  processScore(0);    // Should be F (edge case)
  processScore(-5);   // Should be Invalid Score
  processScore(105);  // Should be Invalid Score
}

/// Processes a given score and prints its corresponding grade.
/// This function exclusively uses 'if' statements for conditional logic.
void processScore(int score) {
  // Initialize grade with a default value.
  // This value will be updated by one of the 'if' statements below
  // if a matching condition is met.
  String grade = "Grade Not Determined";

  // --- Start of logic using ONLY 'if' statements ---

  // Handle invalid scores first.
  // This 'if' checks if the score is outside the valid range [0, 100].
  if (score < 0 || score > 100) {
    grade = "Invalid Score";
  }

  // Check for 'A' grade. This 'if' will only execute if the score is in the A range.
  // It implicitly assumes valid score range from the previous 'if' if no 'Invalid Score' was set.
  // Explicitly checking the upper bound (score <= 100) ensures it's within the overall valid range.
  if (score >= 90 && score <= 100) {
    grade = "A";
  }

  // Check for 'B' grade. The condition (score < 90) makes it mutually exclusive with 'A'.
  if (score >= 80 && score < 90) {
    grade = "B";
  }

  // Check for 'C' grade. The condition (score < 80) makes it mutually exclusive with 'B'.
  if (score >= 70 && score < 80) {
    grade = "C";
  }

  // Check for 'D' grade. The condition (score < 70) makes it mutually exclusive with 'C'.
  if (score >= 60 && score < 70) {
    grade = "D";
  }

  // Check for 'F' grade. The condition (score < 60) makes it mutually exclusive with 'D'.
  // We also explicitly check for (score >= 0) to ensure it's within the valid lower bound
  // for a non-invalid score.
  if (score >= 0 && score < 60) {
    grade = "F";
  }

  // --- End of logic using ONLY 'if' statements ---

  print("Score: $score => Grade: $grade");
}
```

**Output:**
```
Grading System (using only 'if' statements)
This program demonstrates how to replace an 'if-else if-else' chain
with multiple independent 'if' statements by making each condition mutually exclusive.

Score: 95 => Grade: A
Score: 82 => Grade: B
Score: 70 => Grade: C
Score: 65 => Grade: D
Score: 55 => Grade: F
Score: 100 => Grade: A
Score: 0 => Grade: F
Score: -5 => Grade: Invalid Score
Score: 105 => Grade: Invalid Score
```

---

### Example 10: A function that checks if a given number is positive, negative, or zero using if-else condition
### and prints an appropriate message using an if-else if-else structure.

```dart
void checkNumberSign(int number) {
  if (number > 0) {
    print('$number is a positive number.');
  } else if (number < 0) {
    print('$number is a negative number.');
  } else {
    // This block executes if 'number' is neither greater than 0 nor less than 0
    print('$number is zero.');
  }
}

/// A function that determines if a person is old enough to vote (assuming 18 is the legal age).
/// It uses a simple if-else statement.
String checkVotingEligibility(int age) {
  if (age >= 18) {
    return 'Eligible to vote!';
  } else {
    return 'Not eligible to vote yet.';
  }
}

void main() {
  print('--- Checking Number Signs ---');
  checkNumberSign(10);
  checkNumberSign(-5);
  checkNumberSign(0);
  checkNumberSign(100);

  print('\n--- Checking Voting Eligibility ---');
  int personAge1 = 20;
  String eligibilityStatus1 = checkVotingEligibility(personAge1);
  print('Age $personAge1: $eligibilityStatus1');

  int personAge2 = 16;
  String eligibilityStatus2 = checkVotingEligibility(personAge2);
  print('Age $personAge2: $eligibilityStatus2');

  int personAge3 = 18;
  String eligibilityStatus3 = checkVotingEligibility(personAge3);
  print('Age $personAge3: $eligibilityStatus3');

  print('\n--- Example with a simple condition (even/odd) ---');
  void checkEvenOrOdd(int num) {
    if (num % 2 == 0) {
      print('$num is an even number.');
    } else {
      print('$num is an odd number.');
    }
  }

  checkEvenOrOdd(4);
  checkEvenOrOdd(7);
}
```

**Output:**
```
--- Checking Number Signs ---
10 is a positive number.
-5 is a negative number.
0 is zero.
100 is a positive number.

--- Checking Voting Eligibility ---
Age 20: Eligible to vote!
Age 16: Not eligible to vote yet.
Age 18: Eligible to vote!

--- Example with a simple condition (even/odd) ---
4 is an even number.
7 is an odd number.
```

---

### Example 11: A function that uses if-else if-else to determine a student's grade

```dart
String getGrade(int score) {
  // Validate input (optional but good practice)
  if (score < 0 || score > 100) {
    return "Invalid Score";
  }

  // Use if-else if-else to assign a grade based on the score
  if (score >= 90) {
    return "A";
  } else if (score >= 80) {
    return "B";
  } else if (score >= 70) {
    return "C";
  } else if (score >= 60) {
    return "D";
  } else {
    // If none of the above conditions are met, it's a failing grade
    return "F";
  }
}

// The main function where the program execution begins
void main() {
  print("--- Student Grade Calculator ---");

  // Example 1: Score that falls into the 'A' category
  int student1Score = 95;
  String student1Grade = getGrade(student1Score);
  print("A student with score $student1Score gets a grade: $student1Grade"); // Output: A

  // Example 2: Score that falls into the 'B' category
  int student2Score = 82;
  String student2Grade = getGrade(student2Score);
  print("A student with score $student2Score gets a grade: $student2Grade"); // Output: B

  // Example 3: Score that falls into the 'C' category
  int student3Score = 70;
  String student3Grade = getGrade(student3Score);
  print("A student with score $student3Score gets a grade: $student3Grade"); // Output: C

  // Example 4: Score that falls into the 'D' category
  int student4Score = 65;
  String student4Grade = getGrade(student4Score);
  print("A student with score $student4Score gets a grade: $student4Grade"); // Output: D

  // Example 5: Score that falls into the 'F' category (else block)
  int student5Score = 48;
  String student5Grade = getGrade(student5Score);
  print("A student with score $student5Score gets a grade: $student5Grade"); // Output: F

  // Example 6: Edge case - invalid score
  int invalidScore = 105;
  String invalidScoreGrade = getGrade(invalidScore);
  print("A student with score $invalidScore gets a grade: $invalidScoreGrade"); // Output: Invalid Score

  int negativeScore = -5;
  String negativeScoreGrade = getGrade(negativeScore);
  print("A student with score $negativeScore gets a grade: $negativeScoreGrade"); // Output: Invalid Score
}
```

**Output:**
```
--- Student Grade Calculator ---
A student with score 95 gets a grade: A
A student with score 82 gets a grade: B
A student with score 70 gets a grade: C
A student with score 65 gets a grade: D
A student with score 48 gets a grade: F
A student with score 105 gets a grade: Invalid Score
A student with score -5 gets a grade: Invalid Score
```

---

### Example 12: A simple function that uses a switch statement to classify a given number.

```dart
void main() {
  var dayOfWeek = 5;
  switch (dayOfWeek) {
    case 1:
        print("Day is Sunday.");
        break;
    case 2:
        print("Day is Monday.");
      break;
    case 3:
      print("Day is Tuesday.");
      break;
    case 4:
        print("Day is Wednesday.");
      break;
    case 5:
        print("Day is Thursday.");
      break;
    case 6:
        print("Day is Friday.");
      break;
    case 7:
        print("Day is Saturday.");
      break;
    default:
        print("Invalid Weekday.");
      break;
  }
}
```

**Output:**
```
Day is Thursday.
```

---

## Loops

### for, while, do-while, break, continue

### Example 13: main function where the program execution begins for loop

```dart
void main() {
  print("--- Example 1: Printing numbers using a for loop ---");
  // Call the function with an argument
  printNumbers(5); 

  print("\n--- Example 2: Iterating through a list using for-in loop ---");
  List<String> fruits = ["Apple", "Banana", "Cherry", "Date"];
  printListElements(fruits);
}

/// Function that uses a traditional 'for' loop to print numbers.
///
/// Takes an integer 'limit' and prints numbers from 1 up to 'limit' (inclusive).
void printNumbers(int limit) {
  print("Numbers from 1 to $limit:");
  // The 'for' loop structure:
  // 1. Initialization: 'int i = 1;' (Executed once at the beginning)
  // 2. Condition: 'i <= limit;' (Checked before each iteration; loop continues as long as true)
  // 3. Increment/Decrement: 'i++' (Executed after each iteration)
  for (int i = 1; i <= limit; i++) {
    print("Number: $i");
  }
}

/// Function that demonstrates a 'for-in' loop to iterate over a collection.
/// This is often preferred for iterating over lists, sets, etc.
void printListElements(List<String> items) {
  print("Elements in the list:");
  // The 'for-in' loop structure:
  // It iterates over each 'item' in the 'items' collection.
  for (String item in items) {
    print("Fruit: $item");
  }
}
```

**Output:**
```
--- Example 1: Printing numbers using a for loop ---
Numbers from 1 to 5:
Number: 1
Number: 2
Number: 3
Number: 4
Number: 5

--- Example 2: Iterating through a list using for-in loop ---
Elements in the list:
Fruit: Apple
Fruit: Banana
Fruit: Cherry
Fruit: Date
```

---

### Example 14: Using while and do-while concept example 

```dart
/// Main function where the program execution begins.
void main() {
  print("Welcome to the Loop Demonstration Program!\n");
  print("Calling the function 'showSmallExample()':\n");

  // Call the function that contains our loop examples
  showSmallExample();

  print("\nLoop demonstration complete.");
}

/// A function to showcase simple examples of while and do-while loops.
void showSmallExample() {
  // --- Example 1: The 'while' loop ---
  print("--- While Loop Example ---");
  int countWhile = 0; // Initialize a counter

  // The 'while' loop checks its condition *before* executing its block.
  // If the condition is initially false, the block will not execute at all.
  while (countWhile < 3) {
    print("  While loop iteration: $countWhile");
    countWhile++; // Increment the counter to eventually satisfy the loop exit condition
  }
  print("While loop finished. Final countWhile value: $countWhile\n");


  // --- Example 2: The 'do-while' loop ---
  print("--- Do-While Loop Example ---");
  int countDoWhile = 0; // Initialize another counter

  // The 'do-while' loop executes its block *at least once*,
  // then checks the condition. If the condition is true, it repeats.
  do {
    print("  Do-While loop iteration: $countDoWhile");
    countDoWhile++; // Increment the counter
  } while (countDoWhile < 3); // Condition is checked *after* the first execution
  print("Do-While loop finished. Final countDoWhile value: $countDoWhile\n");


  // --- Illustrating the key difference ---
  print("--- Key Difference Highlight ---");

  // While loop with a condition that is initially false
  print("\nWhile loop with an initially false condition (will not run):");
  int neverRunWhile = 5;
  while (neverRunWhile < 3) { // 5 < 3 is false from the start
    print("  This line will NOT be printed by the 'while' loop.");
    neverRunWhile++;
  }
  print("  'while' loop skipped execution as expected. neverRunWhile: $neverRunWhile");


  // Do-while loop with a condition that is initially false
  print("\nDo-While loop with an initially false condition (will run once):");
  int runOnceDoWhile = 5;
  do {
    print("  This line WILL be printed AT LEAST ONCE by the 'do-while' loop.");
    runOnceDoWhile++;
  } while (runOnceDoWhile < 3); // 6 < 3 is false after the first run, so it stops.
  print("  'do-while' loop executed once as expected. runOnceDoWhile: $runOnceDoWhile");
}
```

**Output:**
```
Welcome to the Loop Demonstration Program!

Calling the function 'showSmallExample()':

--- While Loop Example ---
  While loop iteration: 0
  While loop iteration: 1
  While loop iteration: 2
While loop finished. Final countWhile value: 3

--- Do-While Loop Example ---
  Do-While loop iteration: 0
  Do-While loop iteration: 1
  Do-While loop iteration: 2
Do-While loop finished. Final countDoWhile value: 3

--- Key Difference Highlight ---

While loop with an initially false condition (will not run):
  'while' loop skipped execution as expected. neverRunWhile: 5

Do-While loop with an initially false condition (will run once):
  This line WILL be printed AT LEAST ONCE by the 'do-while' loop.
  'do-while' loop executed once as expected. runOnceDoWhile: 6

Loop demonstration complete.
```
---

### Example 15: Using break and continue statements example 

```dart
// import 'dart:io'; // 'dart:io' is not supported by DartPad. Removed.

/// Demonstrates the use of 'break' and 'continue' keywords within loops.
void showBreakAndContinueExample() {
  print("--- Demonstrating 'continue' ---");
  print("Printing odd numbers from 1 to 10:");

  // Use a StringBuffer to collect output that was originally using stdout.write
  // to keep numbers on a single line, as stdout.write does not add newlines.
  StringBuffer oddNumbersOutput = StringBuffer();
  for (int i = 1; i <= 10; i++) {
    // If the number is even, skip the rest of this iteration
    // and move to the next iteration of the loop.
    if (i % 2 == 0) {
      continue; // Jumps to the next iteration (i++).
    }
    // stdout.write('$i '); // Replaced with buffer write
    oddNumbersOutput.write('$i '); // Only odd numbers will be added to the buffer
  }
  // Print the collected numbers. .trimRight() removes the trailing space.
  print(oddNumbersOutput.toString().trimRight());
  // The original print statement had an initial newline `\n`, which would result in a blank line.
  // We simulate that blank line here.
  print('');
  print('(Even numbers were skipped using "continue")');
  print('----------------------------------\n');

  print("--- Demonstrating 'break' ---");
  print("Searching for the number 5 in a sequence from 1 to 10:");

  for (int i = 1; i <= 10; i++) {
    // Original: stdout.write('Checking number $i... '); followed by another print.
    // To keep them on the same line, we combine the messages into one print statement.
    if (i == 5) {
      print('Checking number $i... Found 5! Exiting loop using "break".');
      break; // Immediately exits the 'for' loop.
    }
    print('Checking number $i... Not 5, continuing search.');
  }
  print('(The loop stopped when 5 was found, using "break")');
  print('----------------------------------\n');

  print("--- Another 'break' example: Finding first prime up to 20 ---");
  for (int i = 2; i <= 20; i++) {
    bool isPrime = true;
    for (int j = 2; j < i; j++) {
      if (i % j == 0) {
        isPrime = false;
        // Optimization: if we find any divisor, it's not prime,
        // no need to check further for this 'i'. Break inner loop.
        break;
      }
    }
    if (isPrime) {
      print('First prime number found: $i');
      // Once we find the first prime, we can stop the outer loop.
      break;
    }
  }
  print('----------------------------------\n');
}

void main() {
  print("Starting the program to show break and continue examples.");
  showBreakAndContinueExample();
  print("Program finished.");
}
```

**Output:**
```
Starting the program to show break and continue examples.
--- Demonstrating 'continue' ---
Printing odd numbers from 1 to 10:
1 3 5 7 9

(Even numbers were skipped using "continue")
----------------------------------

--- Demonstrating 'break' ---
Searching for the number 5 in a sequence from 1 to 10:
Checking number 1... Not 5, continuing search.
Checking number 2... Not 5, continuing search.
Checking number 3... Not 5, continuing search.
Checking number 4... Not 5, continuing search.
Checking number 5... Found 5! Exiting loop using "break".
(The loop stopped when 5 was found, using "break")
----------------------------------

--- Another 'break' example: Finding first prime up to 20 ---
First prime number found: 2
----------------------------------

Program finished.
```

---

## File Handling in dart

### Example 16: using file handling in dart concept how we can read, write and delete file.

```dart
import 'dart:collection'; // For HashMap if needed, though a simple Map is usually fine.

/// The name of the file we'll be working with.
const String fileName = 'my_example_file.txt';

// --- Simulation of a file system in memory for DartPad ---
// DartPad does not support 'dart:io' for actual file system operations.
// We will simulate file operations using an in-memory map.
final Map<String, String> _inMemoryFileSystem = {};

void main() async {
  print('--- Dart File Handling Example (Simulated for DartPad) ---');
  print('NOTE: Actual file system operations using dart:io are not supported in DartPad.');
  print('This example simulates file operations using an in-memory map.');

  // 1. Write to a new file
  print('\n=== Step 1: Writing initial content ===');
  await writeFile(fileName, 'Hello, Dart File System!\nThis is the first line.');
  await readFile(fileName); // Read to confirm write

  // 2. Update (Append) content to the file
  print('\n=== Step 2: Appending more content ===');
  await appendToFile(fileName, '\nAppended: Adding a new line to the file.');
  await readFile(fileName); // Read to confirm append

  // 3. Overwrite the file with new content
  print('\n=== Step 3: Overwriting the file ===');
  await writeFile(fileName, 'This content completely replaces the old content.\nNew start!');
  await readFile(fileName); // Read to confirm overwrite

  // 4. Delete the file
  print('\n=== Step 4: Deleting the file ===');
  await deleteFile(fileName);

  // 5. Try to read the file after deletion (expected to fail/show not found)
  print('\n=== Step 5: Attempting to read after deletion ===');
  await readFile(fileName);

  print('\n--- File Handling Example Completed ---');
}

/// Writes (or overwrites) content to a specified file.
/// If the file does not exist, it will be created.
/// If the file exists, its content will be replaced.
Future<void> writeFile(String path, String content) async {
  try {
    final bool fileExisted = _inMemoryFileSystem.containsKey(path);
    _inMemoryFileSystem[path] = content; // Simulate writing/overwriting
    if (fileExisted) {
      print('✅ Successfully overwrote (simulated) "$path"');
    } else {
      print('✅ Successfully created and wrote to (simulated) "$path"');
    }
  } catch (e) {
    print('❌ Error writing to (simulated) "$path": $e');
  }
}

/// Appends content to a specified file.
/// If the file does not exist, it will be created.
/// If the file exists, the new content will be added to the end.
Future<void> appendToFile(String path, String content) async {
  try {
    if (_inMemoryFileSystem.containsKey(path)) {
      _inMemoryFileSystem[path] = (_inMemoryFileSystem[path] ?? '') + content; // Simulate appending
      print('✅ Successfully appended to existing (simulated) "$path"');
    } else {
      _inMemoryFileSystem[path] = content; // Create if not exists and append
      print('✅ Successfully created and appended to (simulated) "$path"');
    }
  } catch (e) {
    print('❌ Error appending to (simulated) "$path": $e');
  }
}

/// Reads and prints the content of a specified file.
Future<void> readFile(String path) async {
  try {
    if (_inMemoryFileSystem.containsKey(path)) {
      String content = _inMemoryFileSystem[path]!; // Simulate reading
      print('📖 Content of (simulated) "$path":\n---START---\n$content---END---');
    } else {
      print('⚠️ (Simulated) File "$path" does not exist.');
    }
  } catch (e) {
    print('❌ Error reading from (simulated) "$path": $e');
  }
}

/// Deletes a specified file.
Future<void> deleteFile(String path) async {
  try {
    if (_inMemoryFileSystem.containsKey(path)) {
      _inMemoryFileSystem.remove(path); // Simulate deleting
      print('🗑️ Successfully deleted (simulated) "$path"');
    } else {
      print('⚠️ (Simulated) File "$path" does not exist, nothing to delete.');
    }
  } catch (e) {
    print('❌ Error deleting (simulated) "$path": $e');
  }
}
```

**Output:**
```
--- Dart File Handling Example (Simulated for DartPad) ---
NOTE: Actual file system operations using dart:io are not supported in DartPad.
This example simulates file operations using an in-memory map.

=== Step 1: Writing initial content ===
✅ Successfully created and wrote to (simulated) "my_example_file.txt"
📖 Content of (simulated) "my_example_file.txt":
---START---
Hello, Dart File System!
This is the first line.---END---

=== Step 2: Appending more content ===
✅ Successfully appended to existing (simulated) "my_example_file.txt"
📖 Content of (simulated) "my_example_file.txt":
---START---
Hello, Dart File System!
This is the first line.
Appended: Adding a new line to the file.---END---

=== Step 3: Overwriting the file ===
✅ Successfully overwrote (simulated) "my_example_file.txt"
📖 Content of (simulated) "my_example_file.txt":
---START---
This content completely replaces the old content.
New start!---END---

=== Step 4: Deleting the file ===
🗑️ Successfully deleted (simulated) "my_example_file.txt"

=== Step 5: Attempting to read after deletion ===
⚠️ (Simulated) File "my_example_file.txt" does not exist.

--- File Handling Example Completed ---
```
---
## OOP In Dart
Object-oriented programming (OOP) is a programming method that uses objects and their interactions to design and program applications. It is one of the most popular programming paradigms and is used in many programming languages, such as Dart, Java, C++, Python, etc.

In OOP, an object can be anything, such as a person, a bank account, a car, or a house. Each object has its attributes (or properties) and behavior (or methods). For example, a person object may have the attributes name, age and height, and the behavior walk and talk.

### Advantages
It is easy to understand and use.
It increases reusability and decreases complexity.
The productivity of programmers increases.
It makes the code easier to maintain, modify and debug.
It promotes teamwork and collaboration.
It reduces the repetition of code.

#### Features Of OOP
1.Class
2.Object
3.Encapsulation
4.Inheritance
5.Polymorphism
6.Abstraction
---

### Example 17: Find Simple Interest Using Class and Objects.
```dart
class SimpleInterest{
  //properties of simple interest
  double? principal;
  double? rate;
  double? time;
  
  //functions of simple interest
  double interest(){
    return (principal! * rate! * time!)/100;
  }
}
void main(){
  //object of simple interest created
  SimpleInterest simpleInterest = SimpleInterest();
  
  //setting properties for simple interest
  simpleInterest.principal=1000;
  simpleInterest.rate=10;
  simpleInterest.time=2;
  
  //functions of simple interest called
  print("Simple Interest is ${simpleInterest.interest()}.");
}
```
**Output:**
```
Simple Interest is 200.
```
---
### Example 18:How To Declare Constructor In Dart
```dart
class Student {
  String? name;
  int? age;
  int? rollNumber;

  // Constructor
  Student(String name, int age, int rollNumber) {
    print(
        "Constructor called"); // this is for checking the constructor is called or not.
    this.name = name;
    this.age = age;
    this.rollNumber = rollNumber;
  }
}

void main() {
  // Here student is object of class Student.
  Student student = Student("John", 20, 1);
  print("Name: ${student.name}");
  print("Age: ${student.age}");
  print("Roll Number: ${student.rollNumber}");
}
```
**Output:**
```
Constructor called
Name: John
Age: 20
Roll Number: 1
```
---
### Example 19:-Named Constructor In Dart
```dart
class Student {
  String? name;
  int? age;
  int? rollNumber;

  // Default Constructor
  Student() {
    print("This is a default constructor");
  }

  // Named Constructor
  Student.namedConstructor(String name, int age, int rollNumber) {
    this.name = name;
    this.age = age;
    this.rollNumber = rollNumber;
  }
}

void main() {
  // Here student is object of class Student.
  Student student = Student.namedConstructor("John", 20, 1);
  print("Name: ${student.name}");
  print("Age: ${student.age}");
  print("Roll Number: ${student.rollNumber}");
}
```
**Output:**
```
This is a default constructor
Name: John
Age: 20
Roll Number: 1
```
---
### Example 20:-Constant Constructor In Dart
```dart
class Student {
  final String? name;
  final int? age;
  final int? rollNumber;

  // Constant Constructor
  const Student({this.name, this.age, this.rollNumber});
}

void main() {
  // Here student is object of Student.
  const Student student = Student(name: "John", age: 20, rollNumber: 1);
  print("Name: ${student.name}");
  print("Age: ${student.age}");
  print("Roll Number: ${student.rollNumber}");
}
```
**output:**
```
Name: John
Age: 20
Roll Number: 1
```
---
## Encapsulation In Dart
In Dart, Encapsulation means hiding data within a library, preventing it from outside factors. It helps you control your program and prevent it from becoming too complicated.
---
### Example 21:- Encapsulation In Dart using Getter method and Setter method 
```dart
class Employee {
  // Private properties
  int? _id;
  String? _name;

// Getter method to access private property _id
  int getId() {
    return _id!;
  }
// Getter method to access private property _name
  String getName() {
    return _name!;
  }
// Setter method to update private property _id
  void setId(int id) {
    this._id = id;
  }
// Setter method to update private property _name
  void setName(String name) {
    this._name = name;
  }
  
}

void main() {
  // Create an object of Employee class
  Employee emp = new Employee();
  // setting values to the object using setter
  emp.setId(1);
  emp.setName("John");

  // Retrieve the values of the object using getter
  print("Id: ${emp.getId()}");
  print("Name: ${emp.getName()}");
}
```
**output:**
```
Id: 1
Name: John
```
---
## Getter In Dart
Getter is used to get the value of a property. It is mostly used to access a private property’s value. Getter provide explicit read access to an object properties.
---
### Example 22:-Getter In Dart With Data Validation
```dart
class NoteBook {
  // Private properties
  String _name;
  double _prize;

  // Constructor
  NoteBook(this._name, this._prize);

  // Getter to access private property _name
  String get name {
    if (_name == "") {
      return "No Name";
    }
    return this._name;
  }

  // Getter to access private property _prize
  double get price {
    return this._prize;
  }
}

void main() {
  // Create an object of NoteBook class
  NoteBook nb = new NoteBook("Apple", 1000);
  print("First Notebook name: ${nb.name}");
  print("First Notebook price: ${nb.price}");
  NoteBook nb2 = new NoteBook("", 500);
  print("Second Notebook name: ${nb2.name}");
  print("Second Notebook price: ${nb2.price}");
}
```
**output:**
```
First Notebook name: Apple
First Notebook price: 1000.0
Second Notebook name: No Name
Second Notebook price: 500.0
```
---
### Setter In Dart
Setter is used to set the value of a property. It is mostly used to update a private property’s value. Setter provide explicit write access to an object properties.
---
### Example 23:-Setter In Dart
```dart
class Student {
  // Private properties
  String? _name;
  int? _classnumber;

  // Setter to update the value of name property
  set name(String name) => this._name = name;

  // Setter to update the value of classnumber property
  set classnumber(int classnumber) {
    if (classnumber <= 0 || classnumber > 12) {
      throw ('Classnumber must be between 1 and 12');
    }
    this._classnumber = classnumber;
  }

  // Method to display the values of the properties
  void display() {
    print("Name: $_name");
    print("Class Number: $_classnumber");
  }
}
void main() {
  // Create an object of Student class
  Student s = new Student();
  // setting values to the object using setter
  s.name = "John Doe";
  s.classnumber = 12;

  // Display the values of the object
  s.display();

  // This will generate error
  //s.setClassNumber(13);
}
```
**output:**
```
Name: John
Class Number: 10
```
---
## Getter And Setter
Getter and Setter provide explicit read and write access to an object properties. In dart, get and set are the keywords used to create getter and setter. Getter read the value of property and act as accessor. Setter update the value of property and act as mutator.
---
### Example 24:-In this example below, there is a class named Student with three private properties _firstName, _lastName and _age. There are two getters fullName and age to get the value of the properties. There are also three setters firstName, lastName and age to update the value of the properties. If age is less than 0, it will throw an error.
```dart
class Student {
  // Private Properties
  String? _firstName;
  String? _lastName;
  int? _age;

  // Getter to get full name
  String get fullName => this._firstName! + " " + this._lastName!;

  // Getter to read private property _age
  int get age => this._age!;

  // Setter to update private property _firstName
  set firstName(String firstName) => this._firstName = firstName;

  // Setter to update private property _lastName
  set lastName(String lastName) => this._lastName = lastName;

  // Setter to update private property _age
  set age(int age) {
    if (age < 0) {
      throw new Exception("Age can't be less than 0");
    }
    this._age = age;
  }
}

void main() {
  // Create an object of Student class
  Student st = new Student();
  // setting values to the object using setter
  st.firstName = "John";
  st.lastName = "Doe";
  st.age = 20;
  // Display the values of the object
  print("Full Name: ${st.fullName}");
  print("Age: ${st.age}");
}
```
**output:**
```
Full Name: John Doe
Age: 20
```
---
## Inheritance In Dart
Inheritance is a sharing of behaviour between two classes. It allows you to define a class that extends the functionality of another class. The extend keyword is used for inheriting from parent class.
---
### Example 25:-In this example, here is parent class Car and child class Toyota. The Toyota class inherits the properties and methods of the Car class.
```dart
class Car{
  String color;
  int year;

  void start(){
    print("Car started");
  }  
}

class Toyota extends Car{
  String model;
  int price;

  void showDetails(){
    print("Model: $model");
    print("Price: $price");
  }
}

void main(){
  var toyota = Toyota();
  toyota.color = "Red";
  toyota.year = 2020;
  toyota.model = "Camry";
  toyota.price = 20000;
  toyota.start();
  toyota.showDetails();
}
```
**output:**
```
Car started
Model: Camry
Price: 20000
```
---
## Super in Dart
Super is used to refer to the parent class. It is used to call the parent class’s properties and methods.
---
### Example 26:-In this example below, the Manager class constructor calls the Employee class constructor using the super keyword.
```dart
class Employee {
  // Constructor
  Employee(String name, double salary) {
    print("Employee constructor");
    print("Name: $name");
    print("Salary: $salary");
  }
}

class Manager extends Employee {
  // Constructor
  Manager(String name, double salary) : super(name, salary) {
    print("Manager constructor");
  }
}

void main() {
  Manager manager = Manager("John", 25000.0);
}
```
**output:**
```
Employee constructor
Name: John
Salary: 25000.0
Manager constructor
```
---
## Polymorphism In Dart
Poly means many and morph means forms. Polymorphism is the ability of an object to take on many forms. As humans, we have the ability to take on many forms. We can be a student, a teacher, a parent, a friend, and so on. Similarly, in object-oriented programming, polymorphism is the ability of an object to take on many forms.
---
### Example 27:-In this example below, there is a class named Employee with a method named salary(). The salary() method is overridden in two child classes named Manager and Developer.
```dart
class Employee{
  void salary(){
    print("Employee salary is \$1000.");
  }
}

class Manager extends Employee{
  @override
  void salary(){
    print("Manager salary is \$2000.");
  }
}

class Developer extends Employee{
  @override
  void salary(){
    print("Developer salary is \$3000.");
  }
}

void main(){
  Manager manager=Manager();
  Developer developer=Developer();
  
  manager.salary();
  developer.salary();
}
```
**output:**
```
Manager salary is $2000.
Developer salary is $3000.
```
---
## Static In Dart
If you want to define a variable or method that is shared by all instances of a class, you can use the static keyword. Static members are accessed using the class name. It is used for memory management.
---
### Example 28:-In this example below, there is a class named Student. The class has a static variable schoolName to store the name of the school. If every student belongs to the same school, then it is better to use a static variable.
```dart
class Student {
  int id;
  String name;
  static String schoolName = "ABC School";
  Student(this.id, this.name);
  void display() {
    print("Id: ${this.id}");
    print("Name: ${this.name}");
    print("School Name: ${Student.schoolName}");
  }
}

void main() {
  Student s1 = new Student(1, "John");
  s1.display();
  Student s2 = new Student(2, "Smith");
  s2.display();
}
```
**output:**
```
Id: 1
Name: John
School Name: ABC School
Id: 2
Name: Smith
School Name: ABC School
```
---
## Enum In Dart
An enum is a special type that represents a fixed number of constant values. An enum is declared using the keyword enum followed by the enum’s name.
---
### Example 29:-In this example below, there is enum type named days. It contains seven constants days. The days enum type is used in the main() function.
```dart
enum days {
  Sunday,
  Monday,
  Tuesday,
  Wednesday,
  Thrusday,
  Friday,
  Saturday
}

void main() {
  var today = days.Friday;
  switch (today) {
    case days.Sunday:
      print("Today is Sunday.");
      break;
    case days.Monday:
      print("Today is Monday.");
      break;
    case days.Tuesday:
      print("Today is Tuesday.");
      break;
    case days.Wednesday:
      print("Today is Wednesday.");
      break;
    case days.Thursday:
      print("Today is Thursday.");
      break;
    case days.Friday:
      print("Today is Friday.");
      break;
    case days.Saturday:
      print("Today is Saturday.");
      break;
  }
}
```
**output:**
```
Today is Friday.
```
---
## Abstract Class
Abstract classes are classes that cannot be initialized. It is used to define the behavior of a class that can be inherited by other classes. An abstract class is declared using the keyword abstract.
---
### Example 30:-In this example below, there is an abstract class Vehicle with two abstract methods start() and stop(). The subclasses Car and Bike implement the abstract methods and override them to print the message.
```dart
abstract class Vehicle {
  // Abstract method
  void start();
  // Abstract method
  void stop();
}

class Car extends Vehicle {
  // Implementation of start()
  @override
  void start() {
    print('Car started');
  }

  // Implementation of stop()
  @override
  void stop() {
    print('Car stopped');
  }
}

class Bike extends Vehicle {
  // Implementation of start()
  @override
  void start() {
    print('Bike started');
  }

  // Implementation of stop()
  @override
  void stop() {
    print('Bike stopped');
  }
}

void main() {
  Car car = Car();
  car.start();
  car.stop();

  Bike bike = Bike();
  bike.start();
  bike.stop();
}
```
**output:**
```
Car started
Car stopped
Bike started
Bike stopped
```
---
## Interface In Dart
An interface defines a syntax that a class must follow. It is a contract that defines the capabilities of a class. It is used to achieve abstraction in the Dart programming language. When you implement an interface, you must implement all the properties and methods defined in the interface. Keyword implements is used to implement an interface.
---
### Example 31:-In this example below, two abstract classes are named Area and Perimeter. The Area class has an abstract method area() and the Perimeter class has an abstract method perimeter(). The Shape class implements both the Area and Perimeter classes. The Shape class has to implement the area() and perimeter() methods.
```dart
// abstract class as interface
abstract class Area {
  void area();
}
// abstract class as interface
abstract class Perimeter {
  void perimeter();
}
// implements multiple interfaces
class Rectangle implements Area, Perimeter {
    // properties
  int length, breadth;

 // constructor
  Rectangle(this.length, this.breadth);

// implementation of area()
  @override
  void area() {
    print('The area of the rectangle is ${length * breadth}');
  }
// implementation of perimeter()
  @override
  void perimeter() {
    print('The perimeter of the rectangle is ${2 * (length + breadth)}');
  }
}

void main() {
  Rectangle rectangle = Rectangle(10, 20);
  rectangle.area();
  rectangle.perimeter();
}
```
**output:**
```
The area of the rectangle is 200
The perimeter of the rectangle is 60
```
---
Key Points To Remember
An interface is a contract that defines the capabilities of a class.
Dart has no keyword interface, but you can use class or abstract class to declare an interface.
Use abstract class to declare an interface.
A class can extend only one class but can implement multiple interfaces.
Using the interface, you can achieve multiple inheritance in Dart.
It is used to achieve abstraction.
---
## Mixin In Dart
Mixins are a way of reusing the code in multiple classes. Mixins are declared using the keyword mixin followed by the mixin name. Three keywords are used while working with mixins: mixin, with, and on. It is possible to use multiple mixins in a class.
---
### Example 32:-In this example below, there are two mixins named CanFly and CanWalk. The CanFly mixin has a method fly() and the CanWalk mixin has a method walk(). The Bird class uses both the CanFly and CanWalk mixins. The Human class uses the CanWalk mixin.
```dart
mixin CanFly {
  void fly() {
    print('I can fly');
  }
}

mixin CanWalk {
  void walk() {
    print('I can walk');
  }
}

class Bird with CanFly, CanWalk {
 
}

class Human with CanWalk {
 
}

void main() {
  var bird = Bird();
  bird.fly();
  bird.walk();

  var human = Human();
  human.walk();
}
```
**output:**
```
I can fly
I can walk
I can walk
```
---
## Factory Constructor In Dart
A factory constructor gives more flexibility to create an object. Generative constructors only create an instance of the class. But, the factory constructor can return an instance of the class or even subclass. It is also used to return the cached instance of the class.
---
### Example 33:-In this example below, factory constructor is used to validate the input. If the input is valid, it will return a new class instance. If the input is invalid, then it will throw an exception.
```dart
class Area {
  final int length;
  final int breadth;
  final int area;

  // private constructor
  const Area._internal(this.length, this.breadth) : area = length * breadth;

  // Factory constructor
  factory Area(int length, int breadth) {
    if (length < 0 || breadth < 0) {
      throw Exception("Length and breadth must be positive");
    }
    // redirect to private constructor
    return Area._internal(length, breadth);
  }
}

void main() {
  // This works
  Area area = Area(10, 20);
  print("Area is: ${area.area}");

  // notice that here is negative value
  Area area2 = Area(-10, 20);
  print("Area is: ${area2.area}");
}
```
**Output:**
```
Area is: 200
Unhandled exception:
Exception: Length and breadth must be positive
```
---
## Generics In Dart
Generics is a way to create a class, or function that can work with different types of data (objects). If you look at the internal implementation of List class, it is a generic class. It can work with different data types like int, String, double, etc. For example, List<int> is a list of integers, List<String> is a list of strings, and List<double> is a list of double values.
---
### Example 34:-In this example below, you will learn to create a generic method with multiple parameters.
```dart
// Define generic method
T genericMethod<T, U>(T value1, U value2) {
  return value1;
}

void main() {
  // call the generic method
  print(genericMethod<int, String>(10, "Hello"));
  print(genericMethod<String, int>("Hello", 10));
}
```
**Output:**
```
10
Hello
```
---
## Null Safety
Null safety is a feature in the Dart programming language that helps developers to avoid null errors. This feature is called Sound Null Safety in dart. This allows developers to catch null errors at edit time.
Advantage Of Null Safety
Write safe code.
Reduce the chances of application crashes.
Easy to find and fix bugs in code.
---
### Example 35:-You can use nullable variables in many ways. Some of them are shown below:
You can use if statement to check whether the variable is null or not.
You can use ! operator, which returns null if the variable is null.
You can use ?? operator to assign a default value if the variable is null.
```dart
void main(){
// Declaring a nullable variable by using ?
String? name;
// Assigning John to name
name = "John";
// Assigning null to name
name = null;
// Checking if name is null using if statement
if(name == null){
print("Name is null");
}
// Using ?? operator to assign a default value
String name1 = name ?? "Stranger";
print(name1);
// Using ! operator to return null if name is null
String name2 = name!;
print(name2);
}
```
**Output:**
```
Name is null
Stranger
Uncaught TypeError: Cannot read properties of null (reading 'toString')Error: TypeError: Cannot read properties of null (reading 'toString')
```
---
### Example 36:-Working With Nullable Class Properties
In the example below, the Profile class has two nullable properties: name and bio. The printProfile method prints the name and bio of the profile. If the name or bio is null, it prints a default value instead.
```dart
class Profile {
  String? name;
  String? bio;

  Profile(this.name, this.bio);

  void printProfile() {
    print("Name: ${name ?? "Unknown"}");
    print("Bio: ${bio ?? "None provided"}");
  }
}

void main() {
  // Create a profile with a name and bio
  Profile profile1 = Profile("John", "Software engineer and avid reader");
  profile1.printProfile();

  // Create a profile with only a name
  Profile profile2 = Profile("Jane", null);
  profile2.printProfile();

  // Create a profile with only a bio
  Profile profile3 = Profile(null, "Loves to travel and try new foods");
  profile3.printProfile();

  // Create a profile with no name or bio
  Profile profile4 = Profile(null, null);
  profile4.printProfile();
}
```
**Output:**
```
Name: John
Bio: Software engineer and avid reader
Name: Jane
Bio: None provided
Name: Unknown
Bio: Loves to travel and try new foods
Name: Unknown
Bio: None provided
```
---
## Type Promotion In Dart
Type promotion in dart means that dart automatically converts a value of one type to another type. Dart does this when it knows that the value is of a specific type.
---
### Example 37:-Type Promotion With Nullable Type To Non-Nullable Type
In this example, the variable value contains a value of type String or null. The variable value is promoted to a non-nullable type String in the if block. If the variable value is null, then the else block is executed.
```dart
// importing dart:math library
import 'dart:math';
// creating a class DataProvider
class DataProvider{
    // creating a method stringorNull
    String? get stringorNull => Random().nextBool() ? "Hello" : null;

    // creating a method myMethod
    void myMethod(){
        String? value = stringorNull;
        // checking if value String or not
        if(value is String){
            print("The length of value is ${value.length}");
        }else{
            print("The value is not string.");
        }

    }
}
// main method
void main() {
    DataProvider().myMethod();
}
```
**Output:**
```
The length of value is 5
```
---
## Late Keyword In Dart
In dart, late keyword is used to declare a variable or field that will be initialized at a later time. It is used to declare a non-nullable variable that is not initialized at the time of declaration.
---
### Example 38:-In this example, there is Person class with a name field. The name field is declared as a late variable.
```dart
class Person {
  // late variable
  late String name;

  void greet() {
    print("Hello $name");
  }
}

void main() {
  Person person = Person();
  // late variable is initialized here
  person.name = "John";
  person.greet();
}
```
**Output:**
```
Hello John
```
---
## What Is Lazy Initialization
Lazy initialization is a design pattern that delays the creation of an object, the calculation of a value, or some other expensive process until the first time you need it.
---
### Example 39:-In this example, the provideCountry function is not called when the value variable is declared. The provideCountry function is called only when the value variable is used. Lazy initialization is used to avoid unnecessary computation.
```dart
// function
String provideCountry() {
  print("Function is called");
  return "USA";
}

void main() {
  print("Starting");
  // late variable
  late String value = provideCountry();
  print("End");
  print(value);
}
```
**Output:**
```
Starting
End
Function is called
USA
```
---
### Example 40:-Late Keyword In Class
In this example, the heavyComputation function is called when the description variable is used. If you remove the late keyword from the description variable, the heavyComputation function will be called when the Person class is instantiated.
```dart
// Person class
class Person {
  final int age;
  final String name;
  late String description = heavyComputation();

// constructor
  Person(this.age, this.name) {
    print("Constructor is called");
  }
// method
  String heavyComputation() {
    print("heavyComputation is called");
    return "Heavy Computation";
  }
}

void main() {
  // object of Person class
  Person person = Person(10, "John");
  print(person.name);
  print(person.description); 
}
```
**Output:**
```
Constructor is called
John
heavyComputation is called
Heavy Computation
```
---
### Example 41:-Late Final Keyword In Dart
In this example, there is class Student with a name field. The name field is declared as a late final variable. The name field is initialized in the Student constructor. The name field is assigned a value only once. If you try to assign a value to the name field again, you will get an error.
```dart
// Student class
class Student {
  // late final variable
  late final String name;

  // constructor
  Student(this.name);
}

void main() {
  // object of Student class
  Student student = Student("John");
  print(student.name);
  student.name = "Doe"; // Error
}
```
**Output:**
```
John
Unhandled exception:
LateInitializationError: Field 'name' has already been initialized.
```
---
## Asynchronous Programming In Dart
Asynchronous Programming is a way of writing code that allows a program to do multiple tasks at the same time. Time consuming operations like fetching data from the internet, writing to a database, reading from a file, and downloading a file can be performed without blocking the main thread of execution.
In Asynchronous programming, program execution continues to the next line without waiting to complete other work. It simply means, Don’t wait. It represents the task that doesn’t need to solve before proceeding to the next one.
---
### Example 42:-In this example, you can see that it will print Second Big Operation at last. It is taking 3 seconds to load and Third Operation and Last Operation don’t need to wait for 3 seconds. This is the problem solved by Asynchronous Programming. A Future represents a value that is not yet available, you will learn about Future in the next section.
```dart
void main() {
  print("First Operation");   
  Future.delayed(Duration(seconds:3),()=>print('Second Big Operation'));
  print("Third Operation"); 
  print("Last Operation"); 
}
```
**Output:**
```
First Operation
Third Operation
Last Operation
Second Big Operation
```
---
## Future In Dart
In dart, the Future represents a value or error that is not yet available. It is used to represent a potential value, or error, that will be available at some time in the future.
---
### Example 43:-You can use future in dart by using then() method. Here the function will return Future<String> after 5 seconds.
```dart
// function that returns a future
Future<String> getUserName() async {
  return Future.delayed(Duration(seconds: 2), () => 'Mark');
}

// main function
void main() {
  print("Start");
  getUserName().then((value) => print(value));
  print("End");
}
```
**Output:**
```
Start
End
Mark
```
---
### Example 44:-In this example below, we are creating a function middleFunction() that returns a future. The function will return Future<String> after 5 seconds.
Note: In this example, First, it prints Start, secondly it prints End, and after 5 seconds Hello will be printed.
```dart
void main() {
  print("Start");
  getData();
  print("End");
}

void getData() async{
  String data = await middleFunction();
  print(data);
}

Future<String> middleFunction(){
  return Future.delayed(Duration(seconds:5), ()=> "Hello");
}
```
**Output:**
```
Start
End
Hello
```
---
## Async And Await In Dart
Async/await is a feature in Dart that allows us to write asynchronous code that looks and behaves like synchronous code, making it easier to read.

When a function is marked async, it signifies that it will carry out some work that could take some time and will return a Future object that wraps the result of that work.

The await keyword, on the other hand, allows you to delay the execution of an async function until the awaited Future has finished. This enables us to create code that appears to be synchronous but is actually asynchronous.

The async and await keywords both provide a declarative way to define an asynchronous function and use their results. You can use the async keyword before a function body to make it asynchronous. You can use the await keyword to get the completed result of an asynchronous expression.
---
### Example 45:-In this example, async handles the states of the program where any part of the program can be executed.async always comes with await because await holds the part of the program until the rest of the program executed.
```dart
void main() {
  print("Start");
  getData();
  print("End");
}

void getData() async{
  String data = await middleFunction();
  print(data);
}

Future<String> middleFunction(){
  return Future.delayed(Duration(seconds:5), ()=> "Hello");
}
```
**Output:**
```
Start
End
Hello
```
---
## Handling Errors
You can handle errors in the dart async function by using try-catch. You can write try-catch code the same way you write synchronous code.
---
### Example 46:-In this example, try-catch handles the exception that could come after the program is executed.
```dart
main() {
  print("Start");
  getData();
  print("End");
}


void getData() async{
    try{
        String data = await middleFunction();
        print(data);
    }catch(err){
        print("Some error $err");
    }
 
}

Future<String> middleFunction(){
  return Future.delayed(Duration(seconds:5), ()=> "Hello");
}
```
**Output:**
```
Start
End
Hello
```
---
## Streams In Dart
A stream is a sequence of asynchronous events representing multiple values that will arrive in the future. Stream class deals with sequences of events instead of single events. Stream has one or more listeners, and all listeners will receive the same value.
---
### Example 47:-You can use stream in dart by using await for loop.
```dart
// function that returns a stream
Stream<String> getUserName() async* {
  await Future.delayed(Duration(seconds: 1));
  yield 'Mark';
  await Future.delayed(Duration(seconds: 1));
  yield 'John';
  await Future.delayed(Duration(seconds: 1));
  yield 'Smith';
}

// main function
void main() async {
  // you can use await for loop to get the value from stream
  await for (String name in getUserName()) {
    print(name);
  }
}
```
**Output:**
```
Mark
John
Smith
```
---
### Example 48:-Example Of async
```dart
Future<int> doSomeLongTask() async {
  await Future.delayed(const Duration(seconds: 2));
  return 21;
}main() async {
  int result = await doSomeLongTask();
  print(result); // prints '42' after waiting 2 second
}
```
**Output:**
```
21
```
---
### Example 49:-Example Of async In Dart*
```dart
Stream<int> countForOneMinute() async* {
  for (int i = 1; i <= 5; i++) {
    await Future.delayed(const Duration(seconds: 1));
    yield i;
  }
} main() async {
  await for (int i in countForOneMinute()) {
    print(i); // prints 1 to 5, one integer per second
  }
}
```
**OUTPUT:**
```
1
2
3
4
5
```
---
### Example 50:-Example Of yield In Dart*
In this example, you have printed only an even number from 10 to 2 using stream. It will print the number after 2 sec.
```dart
Stream<int> str(int n) async* {
 if (n > 0) {  
   await Future.delayed(Duration(seconds: 2));
   yield n;
   yield* str(n - 2);
 }
}

void main() {
 str(10).forEach(print);
}
```
**Output:**
```
10
8
6
4
2
```
---
## Final Vs Const In Dart
If you do not want to change the value of a variable, then you can use either final or const in dart.
---
### Example 51:-
```dart
void main() {
  final finalName = "Final John Doe";
  const constName = "Const John Doe";

  finalName = "Raj"; // Not Possible
  constName = "Anu"; // Not Possible

  print("Final name is " + finalName);
  print("Const name is " + constName);
}
```
**Output:**
```
main.dart:5:3: Error: Can't assign to the final variable 'finalName'.
  finalName = "Raj"; // Not Possible
  ^^^^^^^^^
main.dart:6:3: Error: Can't assign to the const variable 'constName'.
  constName = "Anu"; // Not Possible
```
---
## Const In Dart
If you need to calculate value at compile-time, it is a good idea to choose const over
final. A const variable is a compile-time constant. They must be created from data that
can be calculated at compile time. 100+1 is valid const expression but const date
DateTime.now(); is not.

What Is Compile Time
When you run code in the dart, it will be compiled into the format that the machine can 
understand. This time is called compile time. Const value should be known at compile time.

What Is Run Time
Runtime is the time when your compiled code is started running. It generally occurs after the compile time.
Example:- const total = 50+50; // Possible
          const date = DateTime.now(); // Not Possible
## Final In Dart
If the value is calculated at runtime, you can choose final for it. For. e.g if you want to calculate date on run time, you can use final date = DateTime.now(); but not const date = DateTime.now();.
final date = DateTime.now(); // Possible
const date = DateTime.now(); // Not Possible
---
## DateTime In Dart
Date and time are often used in our day-to-day activities. As a programmer you need to know how to find a date and time? How to format date? and how to perform different calculation in date?
How To Get Date And Time
Use the following code to get the current date and time in the dart.
void main() {
  print(DateTime.now());
}
---
## Get Year, Month, Day Of Datetime In Dart
---
### Example 52:-Here is the way to get a year, month, day, hour, minutes, and seconds in Dart. You can convert DateTime to String by using the toString() method.
```dart
void main() {
  DateTime datetime = DateTime.now();
  print("Year is " + datetime.year.toString());
  print("Month is " + datetime.month.toString());
  print("Day is ${datetime.day}"); // If you don't want to use .toString
  print("Hour is " + datetime.hour.toString());
  print("Minutes is " + datetime.minute.toString());
  print("Second is " + datetime.second.toString());
}
```
**Output:**
```
Year is 2025
Month is 10
Day is 31
Hour is 15
Minutes is 36
Second is 7
```
---
## How To Convert Datetime To String In Dart
---
### Example 53:-Use the following code to convert DateTime to String in the dart.
```dart
void main() {
  String datetime = DateTime.now().toString();
  print(datetime);
}
```
**Output:**
```
2025-10-31 15:39:29.422
```
---
## How To Convert String To DateTime
---
### Example 54:-You cannot get year, months, or day directly and cannot perform date calculation using a String if that String contains the correct DateTime value. In such a situation, you first need to convert String to DateTime.
```dart
void main() {
  String myDateInString = "2022-05-01";
  DateTime myConvertedDate = DateTime.parse(myDateInString);
  print("Year is " + myConvertedDate.year.toString());
  print("Month is " + myConvertedDate.month.toString());
  print("Day is " + myConvertedDate.day.toString());
}
```
**Output:**
```
Year is 2022
Month is 5
Day is 1

```
---
## Methods Supported By Datetime In Dart
You can use DateTime methods if you want to add days, hours, or minutes to DateTime. Let us suppose you have created a DateTime object named mybirthday. DateTime mybirthday = DateTime.parse("1997-05-14");

Method	                                  Example
add(Duration)	              myBirthday.add(Duration(days: 1));
subtract(Duration)	        myBirthday.subtract(Duration(days: 1));

Note: You can set a duration to days, hours, minutes, seconds, milliseconds, and microseconds. To understand it more, look at the example below.
---
### Example 55:-Add Date In Dart
```dart
void main() {
  DateTime myBirthday = DateTime.parse("1997-05-14");
  myBirthday = myBirthday.add(Duration(days: 1));
  print("Year is " + myBirthday.year.toString());
  print("Month is " + myBirthday.month.toString());
  print("Day is " + myBirthday.day.toString());
}
```
**Output:**
```
Year is 1997
Month is 5
Day is 15
```
---
### Example 56:-Subtract Date In Dart
```dart
void main() {
  DateTime myBirthday = DateTime.parse("1997-05-14");
  myBirthday = myBirthday.subtract(Duration(days: 1));
  print("Year is " + myBirthday.year.toString());
  print("Month is " + myBirthday.month.toString());
  print("Day is " + myBirthday.day.toString());
} 
```
**Output:**
```
Year is 1997
Month is 5
Day is 13
```
---
## DateTime Comparision Methods
---
### Example 57:-If you want to compare two dates, then you can use comparison methods.
Method Name	                                    Description
IsAfter(DateTime)	                     Returns true or false. bool
IsBefore(DateTime)	                   Returns true or false. bool
IsAtTheSameMoment(DateTime)	           Returns true or false. bool
```dart
void main() {
  DateTime myBirthday = DateTime.parse("1997-05-14");
  DateTime today = DateTime.now();

  if (myBirthday.isBefore(today)) {
    print("My Birthday is before today.");
  } else if (myBirthday.isAfter(today)) {
    print("My Birthday is after today.");
  } else if (myBirthday.isAtSameMomentAs(today)) {
    print("My Birthday date and today's date is same.");
  }
}
```
**Output:**
```
My Birthday is before today.
```
---
## Dart Extension Method
In Dart, you can extend the functionality of a class by using extension. It is a new feature in Dart 2.7.0. It is similar to extension methods in C# and Kotlin. It is also similar to the concept of mixins in Dart.
---
### Example 58:-How To Use Extension In Dart
Here we are extending the functionality of String class. We are adding a new method capitalize to the String class. We are using extension keyword to extend the functionality of String class.
```dart
void main(){
  String name = "john";
  print(name.capitalize());
}

extension StringExtension on String{
  String capitalize(){
    return "${this[0].toUpperCase()}${this.substring(1)}";
  }
}
```
**Output:-**
```
John
```
---
## Dart how to 
Convert String To Int In Dart
The String is the textual representation of data, whereas int is a numeric representation without a decimal point. While coding in must of the case, you need to convert data from one type to another type. In dart, you can convert String to int by using the int.parse() method.
int.parse("String");
You can replace String with any numeric value and convert String to int. Make sure you have numeric value there. To know more see the example below.
---
### Example 59:-This program converts String to int. You can view type of variable with .runtimeType.
```dart
void main(){
String value = "10";
int numericValue = int.parse(value);
print("Type of value is ${value.runtimeType}");
print("Type of numeric value is ${numericValue.runtimeType}");
}
```
**Output:**
```
Type of value is String
Type of numeric value is int
```
---
## With Try Catch
---
### Example 60:-This program throws an exception because you can’t convert “hello” to int. In this situation, you can use the try-catch exception to display your custom message.
```dart
void main(){
try {
String value = "hello";
int numericValue = int.parse(value);
print("Type of numeric value is ${numericValue.runtimeType}");

  }
catch(ex){
print("Something went wrong.");
}

}
```
**Output:**
```
Something went wrong.
```
---
## Generate Random Number In Dart
This tutorial will teach you how to generate random numbers in dart programming. You will learn to generate random numbers between a range, and also generate a list of random numbers.
Why You Need To Generate Random Number
Random Number Game: You can use random numbers to create a random number game.
Card Game: You can use random numbers to shuffle the cards.
---
### Example 61:-Generate Random Number In Dart
This example shows how to generate random numbers from 0 - 9 and also 1 to 10. After watching this example, you can generate a random number between your choices.
In this program, random.nextInt(10) function is used to generate a random number between 0 and 9 in which the value is stored in a variable randomNumber.
The random.nextInt(10)+1 function is used to generate random number between 1 to 10 in which the value is stored in a variable randomNumber2.
```dart
import 'dart:math';
void main()
{
Random random = new Random();
int randomNumber = random.nextInt(10); // from 0 to 9 included
print("Generated Random Number Between 0 to 9: $randomNumber");
  
int randomNumber2 = random.nextInt(10)+1; // from 1 to 10 included  
print("Generated Random Number Between 1 to 10: $randomNumber2"); 
}
```
**Output:**
```
Generated Random Number Between 0 to 9: 8
Generated Random Number Between 1 to 10: 8
```
---
## How To Capitalize First Letter Of String In Dart
---
### Example 62:-If you want to capitalize the first letter of a String in Dart, you can use the following code:
```dart
void main() { 
  String text = "hello world"; 
  print("Capitalized first letter of String: ${text[0].toUpperCase()}${text.substring(1)}"); 
}
```
**Output:**
```
Capitalized first letter of String: Hello world
```
---
### Example 63:-To Capitalize First Letter Of String Using Extension Method
In this example, we will use the extension method to capitalize the first letter of a String. You can learn more about extension method here.
```dart
extension StringExtension on String {
  String capitalize() {
    return "${this[0].toUpperCase()}${this.substring(1)}";
  }
}

void main() {
  String text = "hello world";
  print("Capitalized first letter of String: ${text.capitalize()}");
}
```
**Output:**
```
Capitalized first letter of String: Hello world
```
---
## Make Http Request in Dart
Introduction
HTTP request means sending a request to a server and getting a response from the server. In this tutorial, we will learn how to make http request in dart with examples.
---
### Example 64:-Make HTTP Get Request
When you want to get data from the server, you need to make a get request. To make HTTP get request in dart, you can use get() method on the http client instance.
Note: If the status code is 200, it means the request is successful and you can get the response body otherwise the request is failed and you can get error message.
```dart
// import http package
import 'package:http/http.dart' as http;
void main() async {
  var url = Uri.parse('https://jsonplaceholder.typicode.com/posts/1');
  // make http get request
  var response = await http.get(url);
  // check the status code for the result  
  if (response.statusCode == 200) {
    print(response.body);
  } else {
    print('Request failed with status: ${response.statusCode}.');
  }  

}
```
**Output:**
```
{
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
  "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}
```
---
### Example 65:-Make HTTP Post Request
When you want to send data to the server, you need to make a post request. To make HTTP post request in dart, you can use post() method on the http client instance.
```dart
// import http package
import 'package:http/http.dart' as http;
void main() async {
  var url = Uri.parse('https://jsonplaceholder.typicode.com/posts');
  // make http post request
  var response = await http.post(url, body: {'title': 'foo', 'body': 'bar', 'userId': '1'});
  // check the status code for the result  
  if (response.statusCode == 201) {
    print(response.body);
  } else {
    print('Request failed with status: ${response.statusCode}.');
  }  
}
```
**Output:**
```
{
  "title": "foo",
  "body": "bar",
  "userId": "1",
  "id": 101
}
```
---
### Example 66:-Make HTTP Patch Request
When you want to update a part of data on the server, you need to make a patch request. To make HTTP patch request in dart, you can use patch() method on the http client instance.
```dart
// import http package
import 'package:http/http.dart' as http;

void main() async {
  var url = Uri.parse('https://jsonplaceholder.typicode.com/posts/1');
  // make http patch request
  var response = await http.patch(url, body: {'title': 'Ramki'});
  // check the status code for the result  
  if (response.statusCode == 200) {
    print(response.body);
  } else {
    print('Request failed with status: ${response.statusCode}.');
  }  

}
```
**Output:**
```
{
  "userId": 1,
  "id": 1,
  "title": "Ramki",
  "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}
```
---
### Example 67:-Make HTTP Delete Request
When you want to delete data from the server, you need to make a delete request. To make HTTP delete request in dart, you can use delete() method on the http client instance.
```dart
// import http package
import 'package:http/http.dart' as http;

void main() async {
  var url = Uri.parse('https://jsonplaceholder.typicode.com/posts/1');
  // make http delete request
  var response = await http.delete(url);
  // check the status code for the result  
  if (response.statusCode == 200) {
    print(response.body);
  } else {
    print('Request failed with status: ${response.statusCode}.');
  }  

}
```
**Output:**
```
{}
```
---

