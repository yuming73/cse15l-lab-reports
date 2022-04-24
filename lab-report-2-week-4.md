# [CSE 15L Lab Report 2](https://yuming73.github.io/cse15l-lab-reports/lab-report-2-week-4.html)  
## Examples of Debugging      

**1. First Example - Runtime Failure**    
* **Bug:** The flaw in the previous code is that the while loop does not check for conditions when there are empty parantheses within the link.
* **Code Changes:** If the difference between the indices of the close and open parentheses is zero, then the parantheses is empty with no links. The program will search for a new index of the close parenthese that contains a valid link, starting from the previously stored value of the `closeParen` variable.
![code change diff 1](lab3_screenshot2.png)   
* **[Test File:](https://github.com/yuming73/markdown-parser/commit/c8a4acc428375c279d1824fb3340ee390fa525dd)** This file contains the failure-inducing input, which caused runtime failure because the program mistakenly took the parantheses within the link to be the outer parantheses that contain the link. 
* **Symptom:** A `java.lang.OutOfMemoryError` is indicated as followed, depicting a runtime failure. Specifically, the error resulted from an infinite loop as the program continue to iterate to find the close paranthese and never break from the while loop. 
![runtime failure](lab3_screenshot1.png)
* *The relationship between the bug, symptom, and failure-inducing input is that .*

---

**2. Second Example - Index Out of Bounds**    
* **Bug:** The flaw in the previous code is that the while loop doesn't check for conditions when there are empty lines, brackets, or parantheses. 
* **Code Changes:**   
![code change diff 2](lab3_screenshot3.png)       
* **[Test File:](https://github.com/AliceFeather/markdown-parser/commit/f1c06b8bcd78118fa2b44f3aef853795e8be72a0)**    
* **Symptom:**    
![index out of bounds](lab3_screenshot4.png)      
* *The relationship between the bug, symptom, and failure-inducing input is that .*

---   

**3. Third Example - Incorrect Output**    
* **Bug:** The flaw in the previous code is that the while loop does not check for conditions when  
* **Code Changes:**     
![code change diff 3](lab3_screenshot5.png)    
* **[Test File:](https://github.com/mdsflyboy/markdown-parser/commit/1d4caabbeca9b12818ed6c6ac9a620f2e69c22a1)**    
* **Symptom:**    
![incorrect output](lab3_screenshot6.png)    
* *The relationship between the bug, symptom, and failure-inducing input is that .* 

---   