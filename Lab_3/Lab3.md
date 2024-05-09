# Lab Report No. 3 &mdash; Bugs & Bash Commands

> #### *"This laboratory report's itinerary: Peruse the process of debugging: rectify bugs, their symptoms, and scout for failure-inducing input. Additionally, one bash command will be elected for thorough research on its plethora of flag options."*

----

## <ins>Part I &ndash; Rectifying a Bug</ins>

----

### Failure-Inducing Input

- **A partial aggregate from a more expansive program relating to List operations; contains a bug**

  ```java
  import java.util.ArrayList;
  import java.util.List;
  import static org.junit.Assert.*;
  import org.junit.*;
  import java.util.Arrays;
  
  class ListExamples {

  // Returns a new list that has all the elements of the input list for which
  // the StringChecker returns true, and not the elements that return false, in
  // the same order they appeared in the input list
  
  static List<String> filter(List<String> list, StringChecker sc) {
    List<String> result = new ArrayList<>();
    for(String s: list) {
      if(sc.checkString(s)) {
        result.add(0, s);
      }
    }
    return result;
  }
  ```

1. A test case that is imparted a ***failure-inducing input*** for this program

    ```java
    @Test
    public void testFilterFailure() {
      List<String> strLst = Arrays.asList("Felder", "Corpi", "Magnum", "Delegate");
      List<String> expectedStrLst = Arrays.asList("Felder", "Magnum");

      assertArrayEquals(expectedStrLst.toArray(), this.filter(strLst, <StringChecker Object...>).toArray());
    ```
     > **This test case will fail and detect incongruence between the `expected` and `actual` inputs due to the bug revealed in due time.**
     
2. A test case that passes with ***no failure-inducing input***

   ```java
    @Test
    public void testFilterSuccess() {
      List<String> strLst = Arrays.asList("Felder", "Corpi", "Magnum", "Delegate");
      List<String> expectedStrLst = Arrays.asList("Magnum", "Felder");

      assertArrayEquals(expectedStrLst.toArray(), this.filter(strLst, <StringChecker Object...>).toArray());
   ```
   > **This test case passes with no inequalities between `expected` and `actual` input.**

# UNFINISHED
      




