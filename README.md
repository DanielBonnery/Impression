# Impression
Bash commands for printing

Definition of function that will convert pdf to booklet. Then modify papersize
```
 eeee () {  pdfbook $1.pdf;gs  -o $1.pdf  -sDEVICE=pdfwrite  -sPAPERSIZE=11x17  -dFIXEDMEDIA  -dPDFFitPage  -dCompatibilityLevel=1.4   $1-book.pdf; rm $1-book.pdf; }
#eeee test


 eeee () {  pdfjam --booklet 'true' --landscape --suffix book --papersize '{11in,17in}'  -- test.pdf}

#pdfbook  test.pdf  1,4-5,9-11,31,31

#gs  -o output.pdf  -sDEVICE=pdfwrite  -sPAPERSIZE=11x17  -dFIXEDMEDIA  -dPDFFitPage  -dCompatibilityLevel=1.4   test-1\,4-5\,9-11\,31\,31-book.pdf


```
