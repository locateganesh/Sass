# SASS / SCSS

### Variable:

Sass variable is like a container, **it used to store information that can be used thoughtout the stylesheet when you need**. You can store things like colors, font stacks, or any CSS value according to your future reusability. The $ symbol is used to make something a variable.


### Global & local variable:

* Defined as top are normally global scopes.
    * `$color-secondary: green;`
  
* If a variable is defined inside curly braces ({} or selector) then it is local scope.
`h1 {
  color: $color-secondary;
}`

* You can define global scope variable in local and make it global by !global tag.
`h1 {
  $color-secondary: red !global;
  color: $color-secondary;
}`
