# Remark

[![Greenkeeper badge](https://badges.greenkeeper.io/sepalang/remark.svg)](https://greenkeeper.io/)

function-oriented scss tool

## function
### trace-media-query
```scss
@include remark-media-trace();
```

### parent select replace
```scss
span.badge {
  @include when("span.badge",".badge-red"){
    color:red;
  }
  @include when("span.badge",".badge-blue"){
    color:blue;
  }
}

### simple focus
```scss
div {
  @include focus(red);
}
```

### simple absoulte
```scss
cover {
  position:relative;
  section {
    @include absolute(right,10px);
  }
}

```

### scroll bar style (only webkit)
```scss
screen {
  @include scrollbar-variant
}
```


### media setting
```scss
@import 'remark';
@include remark-media-width(480px,768px,992px,1200px);

body > section {
  @include media-mobile {
    width:400px;
  }
  @include media-tablet {
    width:700px;
  }
  @include media-desktop {
    width:1028px;
  }
}
```


### response column
```scss

.like-bootstrap-row.no-media {
  // gap 10px;
  @include response-section(10px);
  .like-bootstrap-col {
    //3column
    @include response-column(100%/3);
  }
}


.like-bootstrap-row.with-media {
  // gap 10px;
  @include response-section(10px);
  .like-bootstrap-col {
    //1column
    @include media-mobile {
      @include response-column(100%);
    }
    //2column
    @include media-tablet {
      @include response-column(50%);
    }
    //4column
    @include media-desktop {
      @include response-column(50%);
    }
  }
}
```

### icon (background base icon)
```scss
span {
  @include icon-variant(url(icon.png),10px,10px);
}
```

### image text (inline)
```scss
span {
  @include image-text-variant(url(word.png),20px,10px);
}
```


### easy input style defaultlize
```scss
input {
  @mixin input-variant(20px,100px){
    color:gray;
    background-color:white;
  }
}
```

## Basic custom tag
- modal
- stage
- controls


### modal
```html
<modal>
  <dialog></dialog>
</modal>

```

### stage
```html
<dialog>
  <header></header>
  <stage></stage>
  <footer></footer>
</dialog>
```

### controls
```html
<header>
  <h3>Welcome</h3>
  <controls>
    <a href="">back</a>
    <a href="">next</a>
  </controls>
</header>
```

```html
<dialog>
  <header></header>
  <stage></stage>
  <footer>
    <controls>
      <button>cancle</button>
      <button>ok</button>
    </controls>
  </footer>
</dialog>
```