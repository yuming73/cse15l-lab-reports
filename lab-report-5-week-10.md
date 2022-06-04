# [CSE 15L Lab Report 5](https://yuming73.github.io/cse15l-lab-reports/lab-report-5-week-10.html)    
## Comparing Implementations      

**[My Repository Link](https://github.com/yuming73/markdown-parser.git)**   
**[Provided Repository Link](https://github.com/nidhidhamnani/markdown-parser.git)**   

### Different Output #1    
1. [**Link to Test File:** `510.md`](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/510.md)   
2. **Expected Output:** `[]`   
![expected output1](lab9-screenshot4.png)   
3. **Actual Output:** my repository -`[]` ; provided repository - `[/uri]`   
*Found by using `vimDiff` on the result of running a bash for loop with the command `bash script.sh`. The correct implementation based on the result is my repository.*
![different output1](lab9-screenshot3.png)     
4. **Explanation of Bug:** The incorrect output is because the code in the provided repository did not account for spaces between `nextCloseBracket` and the `openParen`. The current code only checks whether any of the indices are out of bounds and the only condition that determines a valid link is whether the link contains any spaces or new lines. To resolve the bug, at line 73, the code should incorporate an if statement to check whether there are spaces between `nextCloseBracket` and `openParen`, and if so, the link should not consider as a valid link.    
![code change1](lab9-screenshot6.png)

---   

### Different Output #2    
1. [**Link to Test File:** `511.md`](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/511.md)   
2. **Expected Output:** `[/uri]`  
![expected output1](lab9-screenshot5.png)   
3. **Actual Output:** my repository -`[]` ; provided repository - `[/uri]`   
*Found by using `vimDiff` on the result of running a bash for loop with the command `bash script.sh`. The correct implementation based on the result is the provided repository.*   
![different output1](lab9-screenshot3.png)   
4. **Explanation of Bug:** The incorrect output is because the code in my repository did not account for brackets within the brackets that contain the description of the link. With the current code at lines 41 to 43, after a close bracket is found after the current `closeBracket` index, it only increments the `closeBracket` reference by one, which is not sufficient when there are more than one additional close bracket. This caused the if statement at line 56 to fail because the difference between `openParen` and `closeBracket` is not equal to one, in turn causing the link to not be added to the arraylist despite being a valid link.    
![code change1](lab9-screenshot7.png)

---   