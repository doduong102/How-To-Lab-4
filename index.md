# (Hello one, Hello all)

**4. Log into ieng6**
 <br />
<img width="439" alt="image" src="https://github.com/doduong102/How-To-Lab-4/assets/130004918/f225adc9-8607-4e95-8eca-711f5bfa2116">
 <br />
For this, it was as simple as typing out "ssh cs15lsp23ah@ieng6.ucsd.edu" I could have added the `<shift>` and `<space>` for the @ and the space but it's not very VIM relevant ATM

**5. Clone your fork of the respository from your Github Account**
<br />
<img width="430" alt="image" src="https://github.com/doduong102/How-To-Lab-4/assets/130004918/dbce9c6e-ef45-4810-a98a-f1514d66543c">
<br />
Here I just typed out "git clone" and `<CTRL>` + `<V>` to paste in a previously copied URL from my web browser. Then I hit `<ENTER>` to run it

**6. Run the tests, demonstrating that they fail**
<br />
<img width="636" alt="image" src="https://github.com/doduong102/How-To-Lab-4/assets/130004918/e4edccd5-c786-465b-8eb5-437d7272fb61">
<br />
`ls` to find the file needed to run
<br />
`cd lab7` change into the correct directory
<br />
`ls` list files to see which file I'm running
<br />
`bash test.sh` to run it

**7. Edit ListExamples.java**
<br />
`ls` is a strange habit of mine, I just like seeing the name of the file that I'm going to copy over into the next command line
<br />
`vim ListExamples.java` to open the godforsaken file
<br />
I held down `<down>` until I got to code block that needed fixing, landed here:
<br />
<img width="277" alt="image" src=" https://github.com/doduong102/How-To-Lab-4/assets/130004918/6e45dded-461f-4621-b288-1e78aeb23800">
<br />
`<down>``<down>``<down>` to get to the right line
<br />
`<left>'`<left>'`<left>'`<left>' to change index1 to index2
<br />
`i` to enter insert mode
<br />
 `<BACKSPACE>`
<br />
 `2`
<br />
 `<ESC>` to exit insert mode
<br />
 `:wq` to exit VIM
 <br />

**8. Run RUN RUN (the code)**
`<up>``<up>``<up>``<up>` to access my command line history, then `<ENTER>` to run the newly modified code
<img width="260" alt="image" src="https://github.com/doduong102/How-To-Lab-4/assets/130004918/a5757283-d953-4b57-8527-0eec298be818">
Looks good
 

**9. Commit and Push (the buttons jk)**
