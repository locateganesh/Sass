# SASS / SCSS

### Functions:

Functions allows us to run code over and over again when we call it.

```
@function fontSize($size){
    @return $size * 2;
}
.banner p{
    font-size: fontSize($font-sm);
}
```

You can define default parameter also.

```
@function fontSize($size: 25px){
    @return $size * 2;
}
.footer p{
    font-size: fontSize();
}
```

SCSS function has some pre-defined funtions:

```
.nav{
    background: lighten($color-primary, 20%);
}
// or
.nav{
    background: darken($color-primary, 40%);
}
```

