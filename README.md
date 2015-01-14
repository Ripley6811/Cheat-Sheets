# Cheat-Sheets
Language style notes

**JavaScript** style based on [Google JavaScript Style Guide](https://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml)

**Python** style based on Guido et. al's [PEP 8 - Style Guide](https://www.python.org/dev/peps/pep-0008/)

##<font color="red">Style Comparison</font>
---
Topic | Python | JavaScript 
---|---|---
Doc Gen|[SPHINX]|[JSDoc] ([2])
Strings|      |use `'` not `"` ([1])
Constants|`NAMES_LIKE_THIS`|`NAMES_LIKE_THIS`
Functions|`names_like_this`|`namesLikeThis`
Variables|    |`namesLikeThis`
Classes|`NamesLikeThis` |`NamesLikeThis`
Enums|     |`NamesLikeThis`
Methods|`names_like_this`|`namesLikeThis`
Non-Public|`_before_name`|`after_name_`
Filenames|`shortalllower.py`|`filenameslikethis.js`
Block Comments| use `"""` not `'''` | 




##<font color="red">Method Translation</font>
---

Topic | Python | JavaScript 
---|---|---
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


##Python Style
---
>Limit to **79** characters for line length.
>Limit to **72** characters for comment blocks.

>The docstring is a phrase ending in a period. It prescribes the function or method's effect as a command ("Do this", "Return that"), not as a description; e.g. **don't** write "Returns the pathname ...". ([PEP-257])

>Write docstrings for all public modules, functions, classes, and methods. Docstrings are not necessary for non-public methods, but you should have a comment that describes what the method does. This comment should appear after the def line. ([PEP-8])

>_single_leading_underscore : weak "internal use" indicator. E.g. from M import * does not import objects whose name starts with an underscore. ([PEP-8])

>Avoid in-place incrementation with *strings* like `a += b`, use `a = a + b`. ([PEP-8])

>**Raising exceptions** use `raise ValueError('message')` and **not** `raise ValueError, 'message'`.


>When catching exceptions, mention specific exceptions whenever possible instead of using a bare except: clause. For example, use:

```python
try:
    import platform_specific_module
except ImportError:
    platform_specific_module = None
```
>A bare `except:` clause will catch SystemExit and KeyboardInterrupt exceptions, making it harder to interrupt a program with Control-C, and can disguise other problems. If you want to catch all exceptions that signal program errors, use `except Exception:` (bare except is equivalent to `except BaseException:` ).

>Additionally, for all try/except clauses, limit the try clause to the absolute minimum amount of code necessary. Again, this avoids masking bugs.

```python
try:
    value = collection[key]
except KeyError:
    return key_not_found(key)
else:
    return handle_value(value)
```



[1]:https://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml?showone=Strings#Strings
[2]:https://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml?showone=Comments#Comments
[Sphinx]:http://sphinx-doc.org/
[JSDoc]:http://usejsdoc.org/
[PEP-257]:https://www.python.org/dev/peps/pep-0257/
[PEP-8]:https://www.python.org/dev/peps/pep-0008/