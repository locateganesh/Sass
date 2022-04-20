# SASS / SCSS

### If Directive:


```
h1 {
    @if (2 > 4){
        color:red;
    } @else {
        color:blue
    }
}

@mixin headerSizes($size) {
    font: {
        @if($size == large){
            size: 45px;
        } @else if($size == medium) {
            size: 30px;
        } @else {
            size: 15px;
        }
    }
}

h2 {
    @include headerSizes(medium);
}
```


