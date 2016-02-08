#### obsedawk2
- cp2
in vim,
```
/12/d   //delete line with 12
g/12/d  //delete all line with 12
```

others:
```
1d //delete first line
$d //last line
/^$/d //empty line
1,/^$/d    //delete line1 to first emptyline
```

replace  (in sed command, the beginning g is not required)
```
s/12/34 //replace once in current line
s/12/34/g   // replace all in current line
g/12/s/12/34/    //replace every line's first occurence  
g/12/s/12/34/g   //in every line with string `12`, replace 12 to 34 (all occurences)
g/12/s//34/g      // This is same as above.  if address = to be match
g/12/p       //=grep 12, show all lines with string `12`
```



basic sed  
; or -e
```
sed 's/ 12/, 34/; s/ 56/, 78/' list
```
same as
```
sed -e 's/ 12/, 34/' -e 's/ 56/, 78/' list
```

By default, it prints all lines. We can supress and print out lines only replaced.  
-n 	Suppress automatic output of input lines.
```
sed -n -e 's/12/34/p' list
```


some other replacement
```
s/•/>/2        //dot = tabkey
```
The result
```
Column1•Column2•Column3•Column4 -> Column1•Column2>Column3•Column4
```




