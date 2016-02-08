#### obsedawk2
- cp2
in vim,
```
/12/d   //delete line with 12
g/12/d  //delete all line with 12
```

replace
```
s/12/34 //replace once in current line
s/12/34/g   // replace all in current line
g/12/s/12/34/    //replace every line's first occurence
g/12/s/12/34/g   //in every line with string `12`, replace 12 to 34 (all occurences)
g/12/s//34/g      // This is same as above.  if address = to be match
g/12/p       //=grep 12, show all lines with string `12`
```




