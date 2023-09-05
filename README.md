# my2-Battu 
# VANI BATTU
###### Favourite spot - 
Paris nicknamed the **"City of light"** is the capital city of France, and the largest city in France.**Eiffel Tower** to picture-perfect pleasures like a picnic on the bank of the Seine River, Paris offers something for everyone. 
---
#### Acitvities at Paris
1. Sightseeing.
2. Sky diving.
3. Scuba diving.
#### Food 
- macaron
- onion soup
- crocons

[my link](https://github.com/Battu2002Vani/my2-Battu/blob/main/MyStats.md) 

--- 
##### Sports

Sports are very crucial in day to day life. Below mentioned are the regular sports activities that are recommended.

|Name|Reason|Hours|
|----| -----|-----|    
|cricket|mind|2 |
|rugbee| Body | 1 |
| chess| peace | 3 |

---
### quotes
*Kurt Vonnegut*

> "Science is magic that works.” 

*Robert A. Heinlein*

> “Everything is theoretically impossible until it is done.” 

---
> Pass argument to Sass BEM mixin to @extend parent

[link](https://stackoverflow.com/questions/38852317/pass-argument-to-sass-bem-mixin-to-extend-parent)

```

.block {
    /* CSS declarations for `.block` */

    &__element {
        /* CSS declarations for `.block__element` */
    }

    &--modifier {
        /* CSS declarations for `.block--modifier` */

        &__element {
            /* CSS declarations for `.block--modifier__element` */
        }
    }
}
/// Block Element
/// @access public
/// @param {String} $element - Element's name
@mixin element($element) {
    &__#{$element} {
        @content;
    }
}

/// Block Modifier
/// @access public
/// @param {String} $modifier - Modifier's name
@mixin modifier($modifier) {
    &--#{$modifier} {
        @content;
    }
}
.block {
    /* CSS declarations for `.block` */

    @include element('element') {
        /* CSS declarations for `.block__element` */
    }

    @include modifier('modifier') {
        /* CSS declarations for `.block--modifier` */

        @include element('element') {
            /* CSS declarations for `.block--modifier__element` */
        }
    }
}
/// @alias element
@mixin e($element) {
    @include element($element)  {
        @content;
    }
}

/// @alias modifier
@mixin m($modifier) {
    @include modifier($modifier) {
        @content;
    }
}
.block {
    /* CSS declarations for `.block` */

    @include e('element') {
        /* CSS declarations for `.block__element` */
    }

    @include m('modifier') {
        /* CSS declarations for `.block--modifier` */

        @include e('element') {
            /* CSS declarations for `.block--modifier__element` */
        }
    }
}


```

[ans](https://css-tricks.com/snippets/sass/bem-mixins/)
