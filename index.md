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
Here I just typed out "git clone" and `<CNTRL>` + `<V>` to paste in a previously copied URL from my web browser. Then I hit `<ENTER>` to run it

**6. RUn the tests, demonstrating that they fail**

**7. Edit ListExamples.java**

**8. Run RUN RUN (the code)**

**9. Commit and Push (the buttons jk)**

Input:
```
./runme.sh poem.txt 'Contains=haiku'
```
Expected:
```
Compiled successfully, now running...
Also a haiku
```
Actual:
```
Compiled successfully, now running...
This is a short file
It contains text and this is
Also a haiku
```

**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.**

My program is based off of last quarter's cse11 PA7. Specifically, StringSearchMilestone3.
This is StringSearch.java's contents
```
import java.nio.file.*;
import java.io.*;
import java.util.Scanner;

class FileHelper {
    static String[] getLines(String path) {
        try {
            return Files.readAllLines(Paths.get(path)).toArray(String[]::new);
        }
        catch(IOException e) {
            System.err.println("Error reading file " + path + ": " + e);
            return new String[]{"Error reading file " + path + ": " + e};
        }
    }
}

interface Query {
    boolean matches(String s);
}

interface Transform {
    String transform(String s);
}

class ContainsQuery implements Query {
    private String query;

    public ContainsQuery(String query) {
        this.query = query;
    }

    public boolean matches(String s) {
        return s.contains(this.query);
    }

    public String toString() {
        return query;
    }
}

