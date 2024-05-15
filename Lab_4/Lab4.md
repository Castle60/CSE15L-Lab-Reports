# Lab Report No. 4 &mdash; Vi-IMproved (VIM)
> #### *"This laboratory report's itinerary: Hone in on the Vim editor; master the editor via practicing its exotic user commands."*
>> ***Vim is an open-sourced ubiquitous text editing application developed by Bram Moolenaar.***

## <ins>Rectifying a Bug using Vim</ins>

#### For each numbered step, commit the following:
 - Take a screenshot
 - Analytically log which keys were pressed to fulfill a step
 - Summarize the commands ran and the results of using the above keystrokes

-----

#### Step 4 &ndash; Connecting to a Remote Server
 - Img
 - `ssh castle60@ieng6.u.edu` was ran to establish a remote connection; no eminent keystrokes were actuated.
 - `ssh` was the single command executed to establish a remote connection to the ieng6 server.

#### Step 5 &ndash; Cloning a Forked Repository using a SSH link
 - Img
 - `git clone git@github.com:Castle60/Lab.git` was ran to clone a forked repository using the generated SSH link.
 - `git clone` will create a deep copy of all directories, sub-directories, and contained files of the provided repository link.

#### Step 6 &ndash; Running Tests (X1)
 - Img
   - `cd lab7fork`
   - `bash test.sh`
 - Incipiently, I had to traverse into a nested directory that was created from the product of `git clone`. Thereafter, I ran the test script `test.sh` to prove that `ListExamples.java` harbors a bug via the test's failure.

#### Step 7 &ndash; Amending a Java File through Vim
 - Img
   - `vim ListExamples.java`
   - `<UP>` &rarr; `<UP>` &rarr; `<UP>` &rarr; `<UP>` &rarr; `<LEFT>` &rarr; `<LEFT>` &rarr; `<LEFT>` &rarr; `<X>` &rarr; `<I>` &rarr; `<2>` &rarr; `<ESC>` 
 - I accessed the contents of `ListExamples.java` through `vim`, which opened the java file in the Vim editing interface. Thereafter, the keys pressed above demonstrates the sequence of keystrokes pressed to amend a line of code.

#### Step 8 &ndash; Running Tests (X2) 
 - Img
   - `:wq`
   - `bash test.sh`
 - The first command is endemic to Vim: it saves and exits a file. `test.sh` is reintroduced to run the tests another time: illustrating success.

#### Step 9 &ndash; Committing & Pushing Adjustments
 - Img
   - `git add .`
   - `git commit`
   - `git push origin main`
 - `git add` to transfer all amendments to the staging area, `git commit` to initiate and save these modifications, `git push` to publish all commitments to the GitHub repository.
