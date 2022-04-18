# SASS / SCSS

### Placeholder Selectors:

Placeholder selectors could be defined with % and it will be just scss file, it will not go in css file.


```
.heading {
    color: $color-primary;
    font-size: $font-lg;
    background-color: $color-tertiary;
    text-align: center;
}

.banner h1{
    @extend .heading;
}
```
`.heading` selector is like class selector and .heading will also be available in css even though it's only for SCSS.


You can do instead.

```
%heading {
    color: $color-primary;
    font-size: $font-lg;
    background-color: $color-tertiary;
    text-align: center;
}

.banner h1{
    @extend %heading;
}

