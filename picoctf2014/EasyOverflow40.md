#Easy Overflow - 40

Netcatting to vuln2014.picoctf.com 50000 prompts us with the question, "Your number is 2896378. Can you make it negative by adding a positive integer?". It is obvious that this is going to be an interget overflow attack. 

Feeding it a very large number returns "I'm unable to parse your number. It might be too large (the largest java int is 2147483647), or just not a number." Trying again with 2147483647 (the largest java integer) returned the key as seen below.

```
Your number is 7850501. Can you make it negative by adding a positive integer?
2147483647
Congratulations! The sum is -2139633148. Here is the flag: That_was_easssy!
```