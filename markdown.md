[Wiki Homepage](index.md)
## Fore's Markdown Cheatsheet
---
---
### Horizontal Rule 

\* Use three or more of dashes, asterisks, or underscores.  
The symbols can have spaces between them if desired.

    ---
---
    ******
******

    _ _ _ _
_ _ _ _

### Emphasis
    *Single surrounding asterisks make the interior text italicized*  
*Single surrounding asterisks make the interior text italicized*  
   
    _A single underscore produces the same effect_  
_A single underscore produces the same effect_  

    **Two asterisks produce bold**  
**Two asterisks produce bold**  

    __Similarly, two underscores do the same thing__  
__Similarly, two underscores do the same thing__  

    ~~Two tildes create strikethrough text~~
~~Two tildes create strikethrough text~~

    **These effects can ~~'t~~ be *combined* if desired**  
    _These effects can ~~'t~~ be **combined** if desired_
**These effects can ~~'t~~ be *combined* if desired**  
_These effects can ~~'t~~ be **combined** if desired_


---
### Links
    http://www.google.com
http://www.google.com

    <http://www.google.com>
<http://www.google.com>

    [Google](http://www.google.com)
[Google](http://www.google.com)

    [Google](http://www.google.com "This link goes to Google.com")
[Google](http://www.google.com "This link goes to Google.com")

	[Google][Link 1]
	[Yahoo][Link 2]

	[Link 1]: http://www.google.com
	[Link 2]: http://www.yahoo.com "This link goes to Yahoo."

[Google][Link 1]  
[Yahoo][Link 2]

[Link 1]: http://www.google.com
[Link 2]: http://www.yahoo.com "This link goes to Yahoo."

---
### Images
    ![Random Image](http://lorempixel.com/400/200)
![Random Image](http://lorempixel.com/400/200)

    [![Link to Google](http://lorempixel.com/600/200 "This image is a link to Google")](http://www.google.com)
[![Link to Google](http://lorempixel.com/600/200 "This image is a link to Google")](http://www.google.com)

---
### Blockquotes

    According to the source:
    > This is a quote from the source document.
According to the source:
> This is a quote from the source document.

---
### Lists
#### Unordered Lists
    * Item 1
      * sub-bullet a
      * sub-bullet b
        * sub-sub-bullet i
        * sub-sub-bullet ii
      * sub-bullet c
    * Item 2
    * Item 3

* Item 1
  * sub-bullet a
  * sub-bullet b
    * sub-sub-bullet i
    * sub-sub-bullet ii
  * sub-bullet c
* Item 2
* Item 3

\* Bullets can be denoted with either a \+, \-, or \* (plus a space).  These symbols can be mixed if desired, i.e.
```markdown
* Item a
+ Item b
- Item c
```
yields


* Item a
+ Item b
- Item c


#### Ordered Lists
    1. First Item
    2. Second Item
    3. Third Item

1. First Item
2. Second Item
3. Third Item

---
### Code
```markdown
The simplest way to format text as code is to indent 4 spaces.
```

    Text `inside tick marks` is considered code.
Text `inside tick marks` is considered code.

    ```markdown
    Code can be "fenced" by placing three tick marks above and below.
    Putting the name of the language after the first three tick marks will (depending on the engine you're using) format the code.  For example, the lines below will be formatted as markdown.  
        This is a comment.
	*Italics*
	**Bold**
	##### Heading 5
    [Link to Google](http://www.google.com)
	```

```markdown
Code can be "fenced" by placing three tick marks above and below.
Putting the name of the language after the first three tick marks will (depending on the engine you're using) format the code.  For example, the lines below will be formatted as markdown.  
    This is a comment.
*Italics*
**Bold**
##### Heading 5
[Link to Google](http://www.google.com)
```
---
### Headers
    # Header 1
# Header 1

    Header 1
    ========
Header 1
========

    ## Header 2 _with some italics_
## Header 2 _with some italics_

    Header 2
    --------
Header 2
--------

    ###### Header 6 **with bold letters**
###### Header 6 **with bold letters**

---
### Tables

\*Note: tables are not part of the original set of Markdown instructions and may or may not be rendered correctly depending on the interpreter.

```markdown
This|is a|table
:---|:--:|---:
Left justified|center justified|right justified
```

This|is a|table
:---|:--:|---:
Left justified|center justified|right justified

---
### Miscellaneous

The overall philosophy of markdown is that it should be "publishable as-is, in plain text, without looking like it's been marked up with tags or formatting instructions." 

---
##### References
[Markdown Tutorial](https://www.markdowntutorial.com)  
[Markdown Creator's Site](https://daringfireball.net/projects/markdown)

---
This page was last updated: Sun 29 Oct 2017 08:40:39 AM EDT 
