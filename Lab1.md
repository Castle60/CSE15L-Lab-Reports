## Lab Report No. 1 &mdash; Remote Access and FileSystem

> #### *"This laboratory report's itinerary: the bash commands `cd`, `cat`, `ls`, and their functionality."*



### <ins>Usage Cases</ins>

#### Using `cd` &rarr; *"Change Directory"*

```bash
$ cd /workspaces/lecture1/messages
# Directory
```

  - ##### OUTPUT:
    ```yaml
    @Castle60 ➜ /workspaces/lecture1 (main) $ cd /workspaces/lecture1/messages
    @Castle60 ➜ /workspaces/lecture1/messages (main) $
    ```
  - ##### PRIOR WORKING DIRECTORY: `/workspaces/lecture1`
  - ##### NEW WORKING DIRECTORY: `/workspaces/lecture1/messages`
  - ##### EXPLANATION:

    `cd`, as it is an abbreviation for "change directory", will relocate the current working directory to the one denoted by the first given argument.

     In this demonstration of `cd`, I am relocating the working directory by supplementing the absolute path to the new working directory: in this case, to the `messages` directory.

     ***There are no errors with this output.***


------

```bash
$ cd /workspaces/lecture1/Hello.java
# File
```
 - ##### OUTPUT:
   ```yaml
   @Castle60 ➜ /workspaces/lecture1 (main) $ cd /workspaces/lecture1/Hello.java
    bash: cd: /workspaces/lecture1/Hello.java: Not a directory
   ```
 - ##### PRIOR WORKING DIRECTORY: `/workspaces/lecture1`
 - ##### NEW WORKING DIRECTORY: `None`
 - ##### EXPLANATION:

    When an argument is supplied to `cd`, and the argument entails a file such as `Hello.java`, an error is thrown indicating that `Hello.java` is not a viable directory.

    Directories embody an arsenal of files and subdirectories, so to actuate `cd` with a path to a `java` file is erroneous as the working directory cannot be transferred to a file.

    ***There is 1 error with this output. &ndash;*** The formal syntax for `cd` is `cd <path>`, where `<path>` must be supplemented with either a relative or absolute path to some directory; `Hello.java` is not a directory.


------

```bash
$ cd
# No args
```
- ##### OUTPUT:
  ```yaml
  @Castle60 ➜ /workspaces/lecture1 (main) $ cd
  @Castle60 ➜ ~ $
  ```
- ##### PRIOR WORKING DIRECTORY: `/workspaces/lecture1`
- ##### NEW WORKING DIRECTORY: `/home/codespace`
- ##### EXPLANATION:

  When `cd` is utilized without the presence of any arguments (no args), it will not spew any errors; in lieu, it will relocate the current working directory to the *home* directory... also coined as the *file system directory.*

  For instance, on the Mac OS, the *home* directory is located at `/Users/`. On Github Codespaces, it unveils to be `/home/codespace` as this is the file system directory appointed by Github.

  ***There are no errors with this output.***

------

- #### Using `cat` &rarr; *"Concatenate"*

```bash
$ cat /workspaces/lecture1/messages
```
- ##### OUTPUT:
  ```yaml
  @Castle60 ➜ /workspaces/lecture1 (main) $ cat messages
  cat: messages: Is a directory
  ```
- ##### PRIOR WORKING DIRECTORY: `/workspaces/lecture1`
- ##### NEW WORKING DIRECTORY: `None`
- ##### EXPLANATION:

  `cat` is a terminal command that takes two arguments, with the second argument being customary. Its responsibility is to transmute the given file(s) in the arguments and *concatenate*, or print, their contents.

  Under the current circumstance, the path that was imparted was that of a directory; `cat` **cannot articulate the contents of a directory, as it harbors multiple objects and would prove inconvenient to disregard specificity.**

  ***There is 1 error with this output. &ndash;*** `cat` takes paths to files as an argument to properly parse its contents. `/workspaces/lecture1/messages` is a path to a directory. 

------

```bash
$ cat /workspaces/lecture1/messages/ru.txt /workspaces/lecture1/messages/en-us.txt
```
- ##### OUTPUT:
  ```yaml
  @Castle60 ➜ /workspaces/lecture1 (main) $ cat /workspaces/lecture1/messages/ru.txt /workspaces/lecture1/messages/en-us.txt
  Привет, мир!Hello World!
  ```
- ##### PRIOR WORKING DIRECTORY: `/workspaces/lecture1`
- ##### NEW WORKING DIRECTORY: `None`
- ##### EXPLANATION:

  Here, I imparted two arguments whose contents I want to parse and concatenate. Since `ru.txt` and `en-us.txt` are both feasible file types and not directories, the expected and evident output was the contents of both files stringed (concatenated) together with no special formatting.

  ***There are no errors with this output.***
  
------

```bash
$ cat
```
- ##### OUTPUT:
  ```yaml
  @Castle60 ➜ /workspaces/lecture1 (main) $ cat
  Hi World! # User Input
  Hi World!
  Lorem Ipsum # User Input
  Lorem Ipsum
  ```
- ##### PRIOR WORKING DIRECTORY: `/workspaces/lecture1`
- ##### NEW WORKING DIRECTORY: `None`
- ##### EXPLANATION:

  `cat` with no arguments imparted serve as a method of inputting information to the terminal, and retrieving its printed contents as output.

  While it appears impractical to absolve any arguments provided this definition, using `cat` with no arguments can be resourceful when transmuting data with other commands.

  ***There are no errors with this output.***
  
------

- #### Using `ls` &rarr; *"List"*

```bash
$ ls /workspaces/lecture1
```
- ##### OUTPUT:
  ```yaml
  @Castle60 ➜ /workspaces/lecture1 (main) $ ls /workspaces/lecture1
  Hello.class  Hello.java  README  messages
  ```
- ##### PRIOR WORKING DIRECTORY: `/workspaces/lecture1`
- ##### NEW WORKING DIRECTORY: `None`
- ##### EXPLANATION:

  Another intuitive command that's applied ubiquitously is `ls`. This command takes a *path to a directory* as an argument, and prints any identifying information: the names of its corresponding child objects and their extensions (if it is a file).

  In this demonstration, I provided the absolute path `/workspaces/lecture1`. The outcome is the names of each file, their appropriate extensions, and the name of the `messages` directory.

  ***There are no errors with this output.***
  
------

```bash
$ ls /workspaces/lecture1/messages/ru.txt
```
- ##### OUTPUT:
  ```yaml
  @Castle60 ➜ /workspaces/lecture1/messages (main) $ ls /workspaces/lecture1/messages/ru.txt
  /workspaces/lecture1/messages/ru.txt
  ```
- ##### PRIOR WORKING DIRECTORY: `/workspaces/lecture1/messages`
- ##### NEW WORKING DIRECTORY: `None`
- ##### EXPLANATION:

  When a file is provided as the argument to list, `ls` frankly prints the path that was provided as the argument. This is due to the datum that a file does not contain a child object as a directory would.

  ***There are no errors with this output.***
------

```bash
$ ls
```
- ##### OUTPUT:
  ```yaml
  @Castle60 ➜ /workspaces/lecture1/messages (main) $ ls
  en-us.txt  es-mx.txt  ru.txt  zh-cn.txt
  ```
- ##### PRIOR WORKING DIRECTORY: `/workspaces/lecture1/messages`
- ##### NEW WORKING DIRECTORY: `None`
- ##### EXPLANATION:

  Disregarding the arguments, `ls` as a standalone command will print the identifying information (listed two examples above) of the *current working directory*.

  Alas, when `ls` was executed while the current working directory was `/workspaces/lecture1/messages`, the child objects storaged within and their identifying information was printed to the terminal.









