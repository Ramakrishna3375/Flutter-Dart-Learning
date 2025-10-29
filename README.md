# LEARN DART

## Content

1. Introduction and Basics
2. Conditions and Loops
3. Functions in Dart
4. Collections in Dart
5. File Handling in Dart

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

