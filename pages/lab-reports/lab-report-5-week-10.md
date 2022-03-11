# Lab Report 5 Week 10  
  
## Test #1: 22.md  
I used diff to find the differences in output between my code and the Lab 9 provided code.  
Expected output: `[/bar\* "ti\*tle"]`  
Lab 9 output: `[]`  
My output: `[/bar\* "ti\*tle"]`  
  
The bug was in the Lab 9 code. The code does not properly account for spaces in the link. The implementation simply skips any links that have a space in them depite them being vaid links according to [Commonmark](https://spec.commonmark.org/dingus/). The buggy code is shown below.  
![Test 1 Buggy Code](/cse15l-lab-reports/images/lab-report-5-buggy-code-1.PNG)  
As can be seen from the image, a section of the Lab 9 code throws away potential links if they have a space in the link.
  
## Test #2: 201.md  
I used diff to find the differences in output between my code and the Lab 9 provided code.  
Expected output: `[]`  
Lab 9 output: `[baz]`  
My output: `[]`  
  
The bug was in the Lab 9 code. The code does not properly account for extra text between the closing square bracket and the opening parentheses, which would prevent the creation of a link according to [Commonmark](https://spec.commonmark.org/dingus/). The buggy code is shown below.  
![Test 2 Buggy Code](/cse15l-lab-reports/images/lab-report-5-buggy-code-2.PNG)  
As can be seen from the image, the Lab 9 code lacks a check to see if the closing bracket and opening parentheses are next to each other.