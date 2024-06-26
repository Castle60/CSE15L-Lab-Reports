# Lab Report No. 5 &mdash; Wrapping Up
> ***"This lab report's itinerary: Construct a hypothetical scenario in which a 'student' publishes a post to a Piazza forum for a CS class. A 'TA' will reply with leading questions in light of aiding the student in debugging their program."***

## Part I &ndash; Debugging Enactment

-----

## <ins> ConvertToRadians Assistance </ins>
#### ***question @14***

##### Student:
> *"Hello. I can't seem to achieve the necessary outcome of the class `ConvertToRadians`. I know that it is intended to return the radian value of a degree from range `low` (inclusive) to `high` (exclusive), but its output is erroneous.. it begins at 16 even though the `low` is 15. Furthermore, it is including 31 in the output for some mystic reason. Perhaps I am precluding something? Maybe incorrectly retrieving the values? I am not sure.. I ran `javac Range.java`, followed with `java Main 15 30` to compile and run the program; the symptom is visible below."*

![Symptom](Symptom.png)

##### TA:
> *"After taking a brief glance at the symptom of your bug, it appears that your `low` argument is illogically selected by the program, despite your input of 15. This dilemma would also justify the program including 31 in the output as well: Have you traced over the iterator's retrieval operations that you implemented in the `Range` class to solidify its anticipated performance?*"

##### Student:
> *"Thanks! Turns out the bug was nestled within the `next()` method inside my `RangeIterator` class. `next()` was immediately returning the successor of the first value from `low` - disregarding the value of low itself. This bug had also paid a toll on the `high` value: since the iterator started at one value past `low`, the 'new' `high` became 31.*"

- Amended Terminal Output

 ![Output](Correct-Output.png)

- Bugged Version

 ```java
class RangeIterator implements Iterator<Integer> {
// ...
  public Integer next() {
       currentValue++;
       return currentValue;
   }
}
```
- Debugged Version

 ```java
class RangeIterator implements Iterator<Integer> {
// ...
  public Integer next() {
       // The content of this line was originally absolved; here I am storing a shallow copy of currentValue.
       int current = currentValue;
       // Incremented the currentValue field so that on the next invocation, the value will be updated.
       currentValue++;
       // Returning the current value in the range. Before, I was returning the immediate successor.
       return current;
   }
}
```

-----

## Part II &ndash; Second Appointed Reflection

These past former lab sessions have been definitively insightful and educational. To speak candidly, creating Bash scripts through a series of UNIX commands has been an adventurous expedition; one in which I intend on prolonging so that my wanderlust in scripting grows higher. During a former lab activity, I was burdened with writing an autograding script for Java using Bash. Nonetheless, the autograder project has emboldened me to ponder differently about the domain of scripting.
