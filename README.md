# Coding Challenge by R 

##Task
Sample streamed characters

Please write a script that receives and processes an input stream consisting of single characters.
The stream is of unknown and possibly very large length and the script should work regardless of the
size of the input.

The script should take one parameter, the sample size, and generate a random representative
sample using that many characters.

As for receiving the data the tool should work with two kinds of inputs:
- Values piped directly into the process using `cat input.txt | yourScript `
- Values generated by using a secure random source from within the language
- Values loaded via HTTP using the API provided by http://www.random.org/clients/http/

Efficiency, memory consumption, testing, and a clean coding style are all important criteria to we
would like to you keep in mind when completing the challenge.

Should something about the challenge be unclear please make an assumption and document it.

##Example

Given a sample size of 5 and the following stream of characters as values:
```
THEQUICKBROWNFOXJUMPSOVERTHELAZYDOG
```

A possible random sample could be:
```
EMETN
```

Desired execution and output for piped processing
```
$ dd if=/dev/urandom count=100 bs=1MB | base64 | yourScript
Random Sample: EMETN
Maximum allocated memory during runtime: … MB
```

Try to keep the maximum allocated memory as low as feasible.
