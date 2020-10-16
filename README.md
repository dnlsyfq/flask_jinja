### Variable filter 
* Filters are used by the template engine to act on template variables. To use them simply follow the variable with the filter name inside the delimiter and separate them with the | character.
* The character | separating the variable and the filter is called a pipe or vertical bar.
```
{{ variable | filter_name }}
```


> title 
acts on a string variable and capitalizes the first letter in every word

python
```
render_template("_.html",template_heading = "my very interesting website")
```

html
```
{{ template_heading |  title }}
```

> default
* output the text in its argument when a variable isn’t passed to the template
* does not work on empty strings "" or None values. 

html
```
{{ no_template_variable | default("I am not from a variable.") }}
```

|filter|descriptions|
|---|---|
|title:| Capitalizes the first letter of each word in a string, known as titlecase|
|capitalize:| Capitalizes the first character of a string, such as in a sentence|
|lower/uppercase:| Makes all the characters in a string lowercase/uppercase|
|int/float:| Changes any number variable to an integer/float|
|default:| Defines a default string if the variable is not defined|
|length: |Calculates the length of a string, list or dictionary variable|
|dictsort:| Sorts a dictionary by its keys|
