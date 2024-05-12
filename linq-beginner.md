### **LINQ Basics**
- **Select** (Projection): Transforms each element in a collection.
  ```csharp
  var uppercaseNames = names.Select(name => name.ToUpper());
  ```
- **Where** (Filtering): Filters a sequence based on a predicate.
  ```csharp
  var evenNumbers = numbers.Where(num => num % 2 == 0);
  ```
- **OrderBy** / **OrderByDescending** (Sorting): Sorts elements in ascending or descending order.
  ```csharp
  var sortedNames = names.OrderBy(name => name);
  var sortedNumbersDesc = numbers.OrderByDescending(num => num);
  ```

### **Element Operations**
- **First** / **FirstOrDefault**: Returns the first element, or a default value if the sequence is empty.
  ```csharp
  var firstNumber = numbers.First();
  var firstOrDefault = numbers.FirstOrDefault();
  ```
- **Single** / **SingleOrDefault**: Expects a single element and throws an exception if there is more than one.
  ```csharp
  var singleNumber = numbers.Single();
  var singleOrDefault = numbers.SingleOrDefault();
  ```

### **Aggregation**
- **Count**: Counts the elements that satisfy a condition.
  ```csharp
  var numberOfEvens = numbers.Count(num => num % 2 == 0);
  ```
- **Sum**: Computes the sum of a sequence.
  ```csharp
  var total = numbers.Sum();
  ```
- **Average**: Computes the average of a sequence.
  ```csharp
  var average = numbers.Average();
  ```

### **Set Operations**
- **Distinct**: Removes duplicate elements.
  ```csharp
  var distinctNumbers = numbers.Distinct();
  ```
- **Union**: Produces the set union of two sequences.
  ```csharp
  var combinedNumbers = firstList.Union(secondList);
  ```
- **Intersect**: Produces the set intersection of two sequences.
  ```csharp
  var commonNumbers = firstList.Intersect(secondList);
  ```
- **Except**: Produces the set difference of two sequences.
  ```csharp
  var uniqueToFirstList = firstList.Except(secondList);
  ```

### **Conversion**
- **ToArray**: Converts a sequence to an array.
  ```csharp
  var array = numbers.ToArray();
  ```
- **ToList**: Converts a sequence to a list.
  ```csharp
  var list = numbers.ToList();
  ```
- **ToDictionary**: Converts a sequence to a dictionary.
  ```csharp
  var dictionary = numbers.ToDictionary(num => num, num => num * num);
  ```

### **Quantifiers**
- **Any**: Checks if any elements satisfy a condition.
  ```csharp
  var hasEvens = numbers.Any(num => num % 2 == 0);
  ```
- **All**: Checks if all elements satisfy a condition.
  ```csharp
  var allPositive = numbers.All(num => num > 0);
  ```

### **Generation**
- **Range**: Generates a sequence of numbers within a specified range.
  ```csharp
  var range = Enumerable.Range(1, 10);
  ```
- **Repeat**: Generates a sequence that contains one repeated value.
  ```csharp
  var repeated = Enumerable.Repeat("Hello", 5);
  ```

This cheat sheet covers the essentials, but LINQ is a powerful tool with many more methods and nuances.
