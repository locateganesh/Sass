# SASS / SCSS

### Mixin:

Mixin is a block of code, which groups a bunch of reusable CSS styles.

```
@mixin headingStyles{
    color: $color-secondary;
    text-align: center;
}
.banner h1{
    font-size: $font-lg;
    @include headingStyles;
}
.footer h3{
    font-size: $font-md;
    @include headingStyles;
}
```

We can use mixing as a function with parameters also.

```
@mixin headingStyles($fontSize){
    font-size: $fontSize;
    color: $color-secondary;
    text-align: center;
}
.banner h1{
    @include headingStyles($font-lg);
}
.footer h3{
    @include headingStyles($font-md);
}
```

**Note:** Parameter should as SCSS variable start with $.


Also, we can define default parameters also.

```
@mixin headingStyles($fontSize: 50px){
    font-size: $fontSize;
    color: $color-secondary;
    text-align: center;
}
```

When mixing arguments are going to multiple arguments separated by a comma then you can use $param... (with …) as a parameter.

```
@mixin transition($param...){
    transition: $param;
}
.footer h3{
    @include headingStyles($font-md);
    @include transition(color .5s ease-in, background-color .3s ease-out);
    &:hover{
        background-color: $color-tertiary;
        color: $color-primary; 
    }
}
```