# SASS / SCSS

### Interpolation:

Sass interpolation works like a ES6 template literals. Assign a variable and use it inside strings.

```
$b: "border";
$c: "color";

h1{
    box-sizing: #{$b}-box;
    #{$b}: 1px solid blue;
    #{$c}: #fff;
    background-#{$c}: tomato;
}
```

