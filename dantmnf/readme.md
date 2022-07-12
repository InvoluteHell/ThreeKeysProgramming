## 1. `$$` is PID of interpreter

`$$/$$ = 1`

## 2. magic variables

`$.` and `$_` can be reassigned.

`@_` is a plain instance variable of `main`.

## 3. lambda syntax

```ruby
l1 = lambda {|args| body}
l2 = ->(args){body}

l1.call(args)
l1.(args)
l2[args]

l1<<l2 #=> ->(args){l1[l2[args]]}
```

## 4. %-literals for string:

* `[` and `]`
* `(` and `)`
* `{` and `}`
* `<` and `>`
* **Any other character, as both beginning and ending delimiters.**

`%%% = ''`

## 5. `String#<<`

Append the string with value provided, then return the modified string (self).

`String#<<(Integer)` implies `Integer#chr`.

## 6. `$>`

Defaults to `$STDOUT`.

`io << value` prints `value` to `io` then return `io`.

## 7. Misc

Character `'l'`, `'o'`, `'r'` are kept according to the requirements.
