# SASS / SCSS

### For Loop:


```
$colors: red green blue orange;
//$colors: red, green, blue, orange; // Sass list both will work space or comma separator.

@each $color in $colors {
    .paragraph-#{$color} {
        color: $color;
    }
}
```

`@for $i from 1 through 4` instead `@for $i from 1 to 4`. You can use `to` also rather `through` only difference with `to` is it will 1 to 3 it will skip last one like normal programming language. 

