# SASS / SCSS

### Import and Partials:

Sass keep the code DRY. One way to write DRY code is to keep related code in separate files. You can create small files css snippets in other sass files. Eg. rest file, variables, colors, fonts, etc.

#### Sass Partials:

Sass transpiles all the .scss files directly. However you want to import a file, you do not need the file to be transpiled directly. For that reason underscore (_) used in file.

```
_reset.scss
```

#### Sass Import:

The `@import` directive allows you to include the content of one file in another.

```
@import "reset";
```

*No need to write _ and .scss extension. It's recognized by transpiler.*