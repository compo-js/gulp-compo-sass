# gulp-compo-sass

**Gulp** plugin for using the **Sass** preprocessor in **[CompoJS](http://compojs.ru/)**

## Install

```
npm i gulp-compo-sass -D
```

## Using

```js
const compoSass = require('gulp-compo-sass')

function components() {
  return gulp.src('src/components/**/*.htm')
    .pipe(compoSass()) // SCSS Syntax
    .pipe(concat('components.htm'))
    .pipe(gulp.dest('dist'))
}

// or

function components() {
  return gulp.src('src/components/**/*.htm')
    .pipe(compoSass(true)) // SASS Syntax
    .pipe(concat('components.htm'))
    .pipe(gulp.dest('dist'))
}
```

## Example

**[SCSS Syntax](https://sass-lang.com/documentation/syntax#scss)**

```html
<c-component1>
  <h1>
    <span>${ message }</span>
  </h1>
  
  <div>Повседневная практика показывает, что реализация намеченных плановых заданий представляет собой интересный эксперимент проверки модели развития.</div>

  <style>
    h1 {
      span {
        color: red;
      }
    }
  </style>

  <style>
    div {
      padding: 15px;
      background: #ddd;
    }
  </style>
    
  <script>
    this.message = 'Компонент 1'
  </script>
</c-component1>
```
<br>

**[SASS Syntax](https://sass-lang.com/documentation/syntax#the-indented-syntax)**

```html
<c-component1>
  <h1>
    <span>${ message }</span>
  </h1>
  
  <div>Повседневная практика показывает, что реализация намеченных плановых заданий представляет собой интересный эксперимент проверки модели развития.</div>

  <style>
    h1
      span
        color: red
  </style>

  <style>
    div
      padding: 15px
      background: #ddd
  </style>
    
  <script>
    this.message = 'Компонент 1'
  </script>
</c-component1>
```

## Download

- **[new-sass.zip](http://compojs.ru/dist/files/new-sass.zip)**


## Author

- **[compojs.ru](http://www.compojs.ru)**

## Contacts

- **[https://vk.com/compojs](https://vk.com/compojs)**
- **[compo.js@mail.ru](mailto:compo.js@mail.ru)**
