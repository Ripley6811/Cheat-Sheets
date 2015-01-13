# Cheat-Sheets
Language style notes

##<font color="red">Style Comparison</font>
---
Topic | Python | JavaScript 
---|---
Doc Gen|[SPHINX]|[JSDoc] ([2])
Strings|      |use `'` not `"` ([1])
Constants|`NAMES_LIKE_THIS`|`NAMES_LIKE_THIS`
Functions|`names_like_this`|`namesLikeThis`
Variables|    |`namesLikeThis`
Classes|`NamesLikeThis` |`NamesLikeThis`
Enums|     |`NamesLikeThis`
Methods|`names_like_this`|`namesLikeThis`
Non-Public|`_before_name`|`after_name_`
Filenames|  |`filenameslikethis.js`




##<font color="red">Method Equivalence</font>
---
Topic | Python | JavaScript 
---|---
Str joins| `"&".join(list)` | `list.join("&")`
Object/Dict|`{'key': 'value'}`<br>`dict(key='value')`|`{key: 'value'}`<br>`{'key': 'value'}`
Array/List|`['a', 'b', 'c']`|`['a', 'b', 'c']`
Extending<br>Arrays|`arr.append(item)`|`arr.push(item)`
Get Length|`len(arr)`|`arr.length`
Get Slice|`arr[begin:]`<br>`arr[begin:end]`|`arr.slice(begin)`<br>`arr.slice(begin, end)`


##JavaScript Style
---
>Assignments end with semicolon.

```javascript
var foo = function() {
  return true;
};  // semicolon here.

function foo() {
  return true;
}  // no semicolon here.
```
>If - Else example

```javascript
if (something) {
  // ...
} else {
  // ...
}
```
>Array and object spacing.

```
var arr = [1, 2, 3];  // No space after [ or before ].
var obj = {a: 1, b: 2, c: 3};  // No space after { or before }.
```
>Blank lines to organize logical groups.

```
doSomethingTo(x);
doSomethingElseTo(x);
andThen(x);

nowDoSomethingWith(y);

andNowWith(z);
```







[1]:https://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml?showone=Strings#Strings
[2]:https://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml?showone=Comments#Comments
[Sphinx]:http://sphinx-doc.org/
[JSDoc]:http://usejsdoc.org/
