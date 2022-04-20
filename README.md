# SASS / SCSS

### For Loop:


```
$colors: (
    1: red,
    2: green,
    3: blue,
    4: orange
);

@for $i from 1 through 4 {
    .paragraph-#{$i} {
        background-color: map-get($colors, $i);
    }
}
```

`@for $i from 1 through 4` instead `@for $i from 1 to 4`. You can use `to` also rather `through` only difference with `to` is it will 1 to 3 it will skip last one like normal programming language. 

