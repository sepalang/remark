# Remark

Remark is a function-oriented tool utilizing SCSS. This library provides a set of useful SCSS mixins that assist in making web styling more efficient.

## Usage

### Initialization
This initializes HTML and text styling.
```scss
@import "./_remark_media.scss";
@include remark-setup-html();
@include remark-setup-text();
```

### Media Queries
This sets up and traces media queries.
```scss
@import "./_remark_media.scss";
@include remark-setup-media();
@include remark-trace-media();
```

### Parent Selector Replacement
Apply different styles according to specific selectors.
```scss
@import "./_remark_main.scss";
span.badge {
  @include when("span.badge",".badge-red"){
    color:red;
  }
  @include when("span.badge",".badge-blue"){
    color:blue;
  }
}
```

### Simple Absolute Positioning
Easily set an element's absolute position.
```scss
@import "./_remark_main.scss";
.cover {
  position:relative;
  section {
    @include absolute(right,10px);
  }
}
```

### Icon (Background-based Icon)
Use a background image as an icon.
```scss
@import "./_remark_main.scss";
span {
  @include icon-variant(url(icon.png),10px,10px);
}
```

### Image Text (Inline)
Use an image as inline text.
```scss
@import "./_remark_main.scss";
span {
  @include image-text-variant(url(word.png),20px,10px);
}
```

### Easy Input Style Initialization
Easily initialize the style of input fields.
```scss
input {
  @mixin input-variant(20px,100px){
    color:gray;
    background-color:white;
  }
}
```

Remark provides a multitude of features. Apologies, as we have not been able to document them all yet. Please refer to the source code for more information.