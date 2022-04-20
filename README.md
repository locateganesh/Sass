# SASS / SCSS

### Sass Data Types:

There 7 data types:

* Numbers
  ```
  .numbers {
    font-weight: 400;
    line-height: 1.5;
    font-size: 20px; // rem, em, % 
  }
  ```
  These are number type even number with px is also a number value of sass.
  
* Strings
  ```
  .strings {
    font-familty: "Helvetica", arial, sans-sarif;
    font-weight: bold;
    font-style: italic;
  }
  ```
  The text inside quotes are string and without quotes are also string for example arial, sans-sarif, bold etc.
  
* Colors
  ```
  .colors {
    color: red;
    background-color: #ff0000;
    border-color: rgb(255, 0, 0);
    outline-color: hsl(0, 100%, 50%);
  }
  ```
* Lists
  ```
  .lists {
    margin: 10px 15px 5px 20px; // number data list
    font-family: 'Raleway', 'Dosis', 'Lato'; // string data list
    border: 1px solid red;  // multiple data list
  }
  ```
  When any element has mutiple properties known as list in sass.
  
* Maps
  ```
  $colors: (
    primary: red,
    "secondaty": green, // works with quotes
    3: blue // works with number too
  );

  h1 {
     color: map-get($colors, primary);
     background-color: map-get($colors, secondaty);
     border: 10px solid map-get($colors, 3);
  }
  ```
* Booleans
  ```
  @mixin button-format($rounded: false, $size: 100px) {
    color: #fff;
    background-color: $color-primary;
    padding: 10px;
    
        @if $rounded {
            border-radius: $size
        }
    }
    .rounded-btn {
        @include button-format(true, 30px);
    }
    .button-normal{
        @include button-format(false);
    }
  ```
* Null
  ```
  $fonts: (
    "sarif": "Helvetica"
  );

  h3 {
    font: {
        size: 18px;
        weight: bold;
        family: map-get($fonts, "sans"); // This is not defined so it will be a null vallue and font-family won't generate in css.
    }
  }
  
  // CSS
  
  h3 {
    font-size: 18px;
    font-weight: bold; 
  }
  ```
