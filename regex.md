# Regex and rules
## Pattern 
The Pattern class allows you to pre-define regexes and to match 'em against your content. 
```Pattern pattern = Pattern.compile(regexStr);
Matcher matcher = pattern.matcher(stringToCompareTo);
// Displays 'true' or 'false'
System.out.println(matcher.matches());
```

## Groups
One can form groups within our regex, as to then extract content out of matched content. 
```
Pattern datePattern = Pattern.compile("([0-9]{2})\\.([0-9]{2})\\.([0-9]{4})");
Matcher matcher = datePattern.matcher(dateString);
if (dateM.matches()) {
    String day = dateM.group(1);
    String month = dateM.group(2);
    String year = dateM.group(3);
    System.out.println(month + "/" + day + "/" + year);
}
```
## Replacements
One can replace string parts replace through regexes aswell. 
```
String cleanedString = "Satz mit  zu  vielen   Leerzeichen".replaceAll(" {2,}", " ");
// Version without all those unnecessary backspaces
System.out.println(cleanedString);
```
`replaceFirst()` works pretty much the same but only for first occurence. 
