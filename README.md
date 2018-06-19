sassy-media-queries
==================
**Description**

Easy mixins for sass based on Rupture (stylus).

Add the media.sass to your project and include into your main sass or scss file to start using the convenient mixins.
------------------------------
    @import "(../)node_modules/sassy-media-queries/src/media.scss";
------------------------------

Mixins
------
**Between( start, end )**

Sass: `+between(1,2)`

Scss: `@include between(1,2)`

> **For example**
> `@include between(2,4)`
> Based on a breakpoint scale of 0, 600px, 768px, 1024px, 1280px this would generate the following media query:
> `(max-width: 1023px) and (min-width: 600px)`

**from( start )**

Sass: `+from(1)`

Scss: `@include from(1)`

> **For example**
> `@include from(4)`
> Based on a breakpoint scale of 0, 600px, 768px, 1024px, 1280px this would generate the following media query:
> `(min-width: 1024px)`

**to( end )**

Sass: `+to(3)`

Scss: `@include to(3)`

> **For example**
> `@include to(4)`
> Based on a breakpoint scale of 0, 600px, 768px, 1024px, 1280px this would generate the following media query:
> `(max-width: 1023px)`

**at( start, end )**

Sass: `+at(1)`

Scss: `@include at(1)`

> **For example**
> `@include from(4)`
> Based on a breakpoint scale of 0, 600px, 768px, 1024px, 1280px this would generate the following media query:
> `(max-width: 599px) and (min-width: 0)`


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
