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

---

```bash
$ cd
# No args
```

---

- #### Using `cat` &rarr; *"Concatenate"*

```bash

$ cat /workspaces/lecture1/messages
```

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









