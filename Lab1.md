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


---

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


---

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

---

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

  

```bash
$ cat /workspaces/lecture1/messages/ru.txt /workspaces/lecture1/messages/en-us.txt
```

```bash
$ cat
```

- #### Using `ls` &rarr; *"List"*

```bash
$ ls /workspaces/lecture1
```

```bash
$ ls /workspaces/lecture1/messages/ru.txt
```

```bash
$ ls
```









