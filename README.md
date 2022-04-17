# SASS / SCSS

### Extend:

Extend allows one selector to inherit the styles of another selector. it groups the selectors which have the same styles.
Example:
    
    ```
    h1{
        color: #000;
        font-size: 30px;
    }
    h2{
        color: #222;
        font-size: 24px;
    }
    p{
        color: #222;
        font-size: 16px;
    }
    
    /** What extend will do **/
    h1{
        color: #000;
        font-size: 30px;
    }
    h2{
        font-size: 24px;
    }
    p{
        font-size: 16px;
    }
    /** Extend gorups same styles. **/
    h2, p{
        color: #222;
    }
    
    ```

Extend Example: 

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
.footer h3{
    @extend .heading;
}
```

**Caveat:** extend can't work with multi layer selectors (@extend .banner h1), you can do it only with single selector (@extend h1).
