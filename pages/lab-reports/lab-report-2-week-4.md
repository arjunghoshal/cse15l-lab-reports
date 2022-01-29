# Lab Report 2 Week 4  
  
## Code Change #1: Nested Parentheses  
One of the bugs that we found with our initial code was that if there were more than one set of parentheses in the link url, we would get an incorrect output. For example:  
  
`[link](https://google.com/(())a()shd)`  
`[another link](https://something()test())`  
  
Here is the [test file](/cse15l-lab-reports/pages/labs/lab-3/breaking_tests.md) with the failure inducing input.  
When we ran the test, we would find the following symptom:  
  
![Symptom 1-1](/cse15l-lab-reports/images/lab-report-2-symptom-1-1.PNG)  
  

We fixed the bug by making the following code change:  

The input had more than one pair of parentheses in the link url. Since the code was initially looking for the first closing parentheses after the link's opening parentheses, it would return only up to the first closing parentheses. This caused the symptom of having the returned link cut short. The bug was that the code was not accounting for nested parentheses, causing the symptom of an incorrectly parsed link. As can be seen from the code, we fixed the bug by counting any extra pairs of parentheses in the link url until we found the matching closing parentheses for the link.
## Code Change #2: Ending Text  
The next bug we found was that if there was any extra text after the last link in the test file, the program would enter an infinite loop. For example:  
  
