# Shell Data Processing Cheat Sheet
## Commands Used
* mkdir - To create a directory 
* cd - To change the directory
* ni - To create a new file
* ls - To view list of files in a directory

## Git Bash commands Used
## commands used to get the page text
 bash
 curl ""http://shakespeare.mit.edu/romeo_juliet/full.html"

## commands used to get the page text and output to a "data.txt" file

curl "http://shakespeare.mit.edu/romeo_juliet/full.html" -O "data.txt"

- The curl command will return the source for that URL - not the displayed page contents. 


## The command you used to find the most common words, sorted.
- tr transforms the file content - tr (bash) commands 
## Transform each space ' ' into a return character '\12' (aka ASCII line feed)

tr ' ' '\12' < returnedfile

## Pipe the output to sort (send the results of one command as input into another command)

tr ' ' '\12' < returnedfile | sort

## Pipe the sorted output to uniq -c to count

tr ' ' '\12' < returnedfile | sort | uniq -c

## Pipe the reduced output to sort with -nr flag

tr ' ' '\12' < returnedfile | sort | uniq -c | sort -nr

## Redirect the output to result.txt

tr ' ' '\12' < result.txt | sort | uniq -c | sort -nr > result.txt


## Data file
[data.txt](https://github.com/srkvodnala/shell-data-processing/blob/master/data.txt)

## Result file
[result.txt](https://github.com/srkvodnala/shell-data-processing/blob/master/result.txt)