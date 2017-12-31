sass-media-queries
==================
**Content**

Easy mixins for sass based on Rupture (stylus).

Add the media.sass to your project and include into your main sass or scss file to start using the convenient mixins.

Mixins
------
**Between( start, end )**

Sass: `+between(1,2)`

Scss: `@include between(1,2)`

**from( start )**

Sass: `+from(1)`

Scss: `@include from(1)`

**to( end )**

Sass: `+to(3)`

Scss: `@include to(3)`

**at( start, end )**

Sass: `+at(1,2)`

Scss: `@include at(1,2)`


Examples
------------------------------
    .body
      color: red
      +from(3)
        color: blue

      p
        font-size: 12px;

        +between(3,5)
          font-size: 16px;


Override breakpoint definition
------------------------------
Add the following override to your main sass file (root level where you import the mixins):

    $media-scale: ( 0, 400px, 768px, 1024px, 1280px)

This will force the mixins to use your definition;


Change log
----------
Version 1.1

*Fixed `at` mixin and correct bug with $media-scale variable

Version 1.0

*First  version of mixin definition*