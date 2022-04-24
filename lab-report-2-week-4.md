# [CSE 15L Lab Report 2](https://yuming73.github.io/cse15l-lab-reports/lab-report-2-week-4.html)  
## Examples of Debugging      

**1. First Example - Runtime Failure**    
* **Code Changes:** If the difference between the indices of the close and open parentheses is zero, then the parantheses is empty with no links. The program will search for the actual index of the close parenthese, starting from the previously stored index of the close paranthese.
![code change diff 1](lab3_screenshot2.png)   
* **[Test File:](https://github.com/yuming73/markdown-parser/commit/c8a4acc428375c279d1824fb3340ee390fa525dd)** This file contains the failure-inducing input, which caused runtime failure because the program mistakenly took the parantheses within the link to be the outer parantheses embodying the link. 
* **Symptom:** A `java.lang.OutOfMemoryError` is indicated as followed, depicting a runtime failure. Specifically, the error resulted from an infinite loop as the program continue to iterate to find the close paranthese and never break from the while loop. 
![runtime failure](lab3_screenshot1.png)
* *The relationship between the bug, symptom, and failure-inducing input is that .*

---

**2. Second Example - Index Out of Bounds**    
* **Code Changes:**   
![code change diff 2](lab3_screenshot3.png)       
* **[Test File:](https://github.com/AliceFeather/markdown-parser/commit/f1c06b8bcd78118fa2b44f3aef853795e8be72a0)**    
* **Symptom:**    
![index out of bounds](lab3_screenshot4.png)    
* *The relationship between the bug, symptom, and failure-inducing input is that .*

---   

**3. Third Example -**    

---   