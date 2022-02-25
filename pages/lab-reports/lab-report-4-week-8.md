# Lab Report 4 Week 8  

## My Implementation:  
Link to repository: [My Repository](https://github.com/arjunghoshal/markdown-parse)  
  
### Test Snippet #1:  
The correct output according to [CommonMark](https://spec.commonmark.org/dingus/) is:  
```  
[`google.com, google.com, ucsd.edu]  
```  
Test Code:  
![Snippet 1 Test Code](/cse15l-lab-reports/images/lab-report-4-test-code-1-1.PNG)  
My Output:  
![Snippet 1 Test Output](/cse15l-lab-reports/images/lab-report-4-test-output-1-1.PNG)  
In order to account for inline code with backticks, we would have to make a fairly involved change to the code. We would have to cover all the edge cases and account for the behavior of links in code blocks. This means that it will take more than a small code change to fix this error.  
  
### Test Snippet #2:  
The correct output according to [CommonMark](https://spec.commonmark.org/dingus/) is:  
```  
[a.com, a.com(()), example.com]  
```  
Test Code:  
![Snippet 2 Test Code](/cse15l-lab-reports/images/lab-report-4-test-code-1-2.PNG)  
My Output:  
![Snippet 2 Test Output](/cse15l-lab-reports/images/lab-report-4-test-output-1-2.PNG)  
In order to fix this issue, a small change can be made to the code that checks for backslashes before the brackets. This would fix the issue in the third link where the code recognizes the escaped closing bracket as the end of the link.
  
### Test Snippet #3:  
The correct output according to [CommonMark](https://spec.commonmark.org/dingus/) is:  
```  
[https://ucsd-cse15l-w22.github.io/]  
```  
Test Code:  
![Snippet 3 Test Code](/cse15l-lab-reports/images/lab-report-4-test-code-1-3.PNG)  
My Output:  
![Snippet 3 Test Output](/cse15l-lab-reports/images/lab-report-4-test-output-1-3.PNG)  
In order to fix this issue, a small change can be made to the code that looks for new line characters in the link. This would fix the issue that made `https://twitter.com` be added to the output, and also fix the formatting error with the output.  
  
## Review Implementation:  
Link to repository: [Review Repository](https://github.com/tylercyang/markdown-parse)  
  
### Test Snippet #1:  
The correct output according to [CommonMark](https://spec.commonmark.org/dingus/) is:  
```  
[`google.com, google.com, ucsd.edu]  
```  
Test Code:  
![Snippet 1 Test Code](/cse15l-lab-reports/images/lab-report-4-test-code-2-1.PNG)  
The Output:  
![Snippet 1 Test Output](/cse15l-lab-reports/images/lab-report-4-test-output-2-1.PNG)  
In order to account for inline code with backticks, we would have to make a fairly involved change to the code. We would have to cover all the edge cases and account for the behavior of links in code blocks. This means that it will take more than a small code change to fix this error.  
  
### Test Snippet #2:  
The correct output according to [CommonMark](https://spec.commonmark.org/dingus/) is:  
```  
[a.com, a.com(()), example.com]  
```  
Test Code:  
![Snippet 2 Test Code](/cse15l-lab-reports/images/lab-report-4-test-code-2-2.PNG)  
The Output:  
![Snippet 2 Test Output](/cse15l-lab-reports/images/lab-report-4-test-output-2-2.PNG)  
In order to fix this issue, a small change can be made to the code that checks for backslashes before the brackets. This would fix the issue in the third link where the code recognizes the escaped closing bracket as the end of the link. We can also add another small change to account for nested parentheses properly such that the second link is correct.
  
### Test Snippet #3:  
The correct output according to [CommonMark](https://spec.commonmark.org/dingus/) is:  
```  
[https://ucsd-cse15l-w22.github.io/]  
```  
Test Code:  
![Snippet 3 Test Code](/cse15l-lab-reports/images/lab-report-4-test-code-2-3.PNG)  
The Output:  
![Snippet 3 Test Output](/cse15l-lab-reports/images/lab-report-4-test-output-2-3.PNG)  
In order to fix this issue, a small change can be made to the code that looks for new line characters in the link. This would fix the issue that made `https://twitter.com` be added to the output, and also fix the formatting error with the output. In addition, the same code for nested parentheses from snippet 2 could be used to fix the issue where `github.com` appears in the output since the code as of right now does not account for not having a closing parenthesis.