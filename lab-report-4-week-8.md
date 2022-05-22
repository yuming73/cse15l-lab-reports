# [CSE 15L Lab Report 4](https://yuming73.github.io/cse15l-lab-reports/lab-report-4-week-8.html)    
## Snippet Code Reviews    

**[My Repository Link](https://github.com/yuming73/markdown-parser.git)**   
**[Reviewed Repository Link](https://github.com/Sking56/markdown-parser.git)**   

**Expected Output of the Snippets:**    
1. Snippet 1: the expected output is ``[`google.com, google.com, ucsd.edu]``   
![expected output1](lab7-screenshot4.png)   
2. Snippet 2: the expected output is `[a.com(()), example.com]`   
![expected output2](lab7-screenshot5.png)   
3. Snippet 3: the expected output is `[https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]`   
![expected output3](lab7-screenshot6.png)   

**Tests in `MarkdownParseTest.java`**   
![snippet tests](lab7-screenshot2.png)   
*I created a new file for each snippet and added the tests for each snippet file.*

### My `MarkdownParse` Implementation    
* 