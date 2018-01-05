# Pure-CSS-loaders

A scss project with some pure css loaders and spinners.

* The tricolor one will work without an SVG but will look worse
* The google spinner won't work without SVG. Still working on making one without it, i have one
  working but it just doesn't look right
  [Here's the codepen to show them](https://codepen.io/db1996/pen/VrNoBJ). Shown with normal CSS
  because the file got way too long

## Contents

[Update](#update)

[Mixins](#mixins)

* [wave](#wave)
* [square-wave](#square-wave)
* [dots](#dots)
* [dots-horizontal](#dots-horizontal)
* [google-spinner](#google-spinner)
* [gooey-loader](#gooey-loader)

[Credits](#credits)

## Update

* Added another loader, the windows 10 horizontal dots (moving from left to right)
* All of the loaders now work with Mixins

## Mixins

Note: There's an example with description for all of the mixins in the `_settings.scss` file

### wave

    create-wave-elem($c, $am, $w, $max-h, $min-h, $gap, $bcolor, $anim-l)

`$c`: classname (string). Whatever classname you use should be the same as the wrapper of all the
individual waves. If the classname `loading-waves` the HTML should look like this:

    <div class="loading-waves">
        <div class="loading-waves__wave"></div>
        <div class="loading-waves__wave"></div>
        <div class="loading-waves__wave"></div>
        <div class="loading-waves__wave"></div>
        <div class="loading-waves__wave"></div>
    </div>

`$am`: Amount of `<div class="loading-waves__wave"></div>` elements.

`$w`: The width of each individual `<div class="loading-waves__wave"></div>` element.

`$max-h`: The height each `<div class="loading-waves__wave"></div>` will grow to at max.

`$min-h`: The height each `<div class="loading-waves__wave"></div>` will shrink to at min.

`$gap`: The gap between each `<div class="loading-waves__wave"></div>`.

`$bcolor`: The color of the waves.

`anim-l`: time it takes for each wave to shrink and grow (i cycle)

### square-wave

    create-square-wave-elem($c, $am, $w, $h, $g, $bcol, $al, $jdy, $jdx, $mop)

`$c`: classname (string). Whatever classname you use should be the same as the wrapper of all the
individual waves. If the classname `loading-square-waves` the HTML should look like this:

    <div class="loading-square-waves">
        <div class="loading-square-waves__square"></div>
        <div class="loading-square-waves__square"></div>
        <div class="loading-square-waves__square"></div>
        <div class="loading-square-waves__square"></div>
        <div class="loading-square-waves__square"></div>
    </div>

`$am`: Amount of `<div class="loading-square-waves__square"></div>` elements.

`$w`: The width of each individual `<div class="loading-square-waves__square"></div>` element.

`$h`: The height of each individual `<div class="loading-square-waves__square"></div>` element.

`$gap`: The gap between each `<div class="loading-square-waves__square"></div>`.

`$bcol`: The color of the squares.

`al`: The time it takes each square to jump and fall (one cycle)

`jdy`: The distance each square jumps up (or down)

`jdx`: The distance each square jumps right (or left)

`mop`: The minimum opacity of each square, set this to 1 if you don't want any opacity

### dots

    create-dots-elem ($c, $am, $s, $cs, $ranim, $bfanim, $bddanim, $col)

`$c`: classname (string). Whatever classname you use should be the same as the wrapper of all the
individual dots. If the classname `loading-dots` the HTML should look like this:

    <div class="loading-dots">
        <div class="loading-dots__dot"></div>
        <div class="loading-dots__dot"></div>
        <div class="loading-dots__dot"></div>
        <div class="loading-dots__dot"></div>
        <div class="loading-dots__dot"></div>
    </div>

`$am`: Amount of `<div class="loading-dots__dot"></div>` elements.

`$s`: The size of the dots (Width and height is equal and the border-radius is set to 50%).

`$cs`: The circle size. The height and width of space where all the dots go in circles

`$ranim`: Amount of time it takes a dot to animate 2 full circles (the speed up and slow down parts
are calculated)

`bfanim`: Delay in seconds for every dot between every 2 rounds (the time a dot is invisible after
ending 2 rounds)

`bddanim`: Delay in seconds between every dot (the higher, the more distance there will be between 2
dots)

`$col`: The color of the dots

### dots-horizontal

    create-horizontal-dots-elem($c, $am, $s, $col, $w, $al, $ad)

`$c`: classname (string). Whatever classname you use should be the same as the wrapper of all the
individual dots. If the classname `loader-horizontal-dots` the HTML should look like this:

    <div class="loader-horizontal-dots">
        <div class="loader-horizontal-dots__dot"></div>
        <div class="loader-horizontal-dots__dot"></div>
        <div class="loader-horizontal-dots__dot"></div>
        <div class="loader-horizontal-dots__dot"></div>
        <div class="loader-horizontal-dots__dot"></div>
    </div>

`$am`: Amount of `<div class="loader-horizontal-dots__dot"></div>` elements

`$s`: The size of the dots (Width and height is equal and the border-radius is set to 50%).

`$col`: The color of the dots

`$w`: The width of the **container** element. This is also how far to the right every dot will go

`$al`: Time it takes to go from left to right for each dots

`$ad`: Delay in seconds between every dot (the higher, the more distance there will be between 2
dots)

### google-spinner

    create-google-spinner-elem($c, $s, $bw, $r, $g, $b, $y)

`$c`: classname (string). Whatever classname you use should be the same as the wrapper. If the
classname `loading-google-spinner` the HTML should look like this:

    <div class="loading-google-spinner">
        <svg class="loading-google-spinner__circle-svg" viewBox="25 25 50 50">
            <circle class="loading-google-spinner__circle-stroke" cx="50" cy="50" r="20" fill="none" stroke-width="2" stroke-miterlimit="10"/>
        </svg>
    </div>

`$s`: The size of the circle

`$bw`: The width of the border of the circle (the visible colored part)

`$r, $g, $b, $y`: The colors the circle will change in (red, green, blue, yellow are standard, make
them all the same to have no transition)

### gooey-loader

    create-gooey-loader-elem($c, $w, $h, $bcol1, $bcol2, $bcol3, $al, $fcw)

`$c`: classname (string). Whatever classname you use should be the same as the wrapper . If the
classname `loading-gooey` the HTML should look like this:

    <div class="loading-gooey">
        <div class="loading-gooey__dot loading-gooey__dot--dot3"></div>
        <div class="loading-gooey__dot loading-gooey__dot--dot2"></div>
        <div class="loading-gooey__dot loading-gooey__dot--dot1"></div>
    </div>
    <svg xmlns="http://www.w3.org/2000/svg" version="1.1">
        <defs>
            <filter id="gooey-filter">
                <feGaussianBlur in="SourceGraphic" stdDeviation="10" result="blur" />
                <feColorMatrix in="blur" mode="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 21 -7"/>
            </filter>
        </defs>
    </svg>

`$w`: The width of each dot.

`$h`: The height of each dot.

`$bcol1, $bcol2, $bcol3`: The colors of each dot

`$al`: length in seconds of the full animation

`$fcw`: The width of the circle (and height) that all the dots move in

NOTE: The SVG is not needed, but it looks better with it. (it makes the colors morph) NOTE: This one
is the _most_ buggy out of all of them to customize. You can play around with it

### Spinner (2 halves)

    @mixin create-spinner-elem($c, $s, $bs, $col, $al, $ad: normal, $s-s: $s - 20px, $s-bs: $bs, $s-col: $col, $s-al: $al, $s-ad: reverse)

Variables here are devided in the big circle and small circle

`$c`: classname (string). Whatever classname you use should be the same the loader element. The
loader is just 1 element using pseudo's if the name "loading-spinner" was used the HTML should look
like this:

    <div class="loading-spinner"></div>

`$s`: The size of the big circle

`$bs`: border-size of the big circle

`$col`: Color of the big circle

`$al`: Animation length of the big circles

`$ad`: Animation direction: OPTIONAL. STANDARD: normal (clockwise)

`$s-s`: size of the small circle. OPTIONAL, STANDARD: Big circle size - 20px

`$s-bs`: border size of the small circle. OPTIONAL, STANDARD: Big circle border customize

`$s-col`: Color of the small circle. OPTIONAL, STANDARD: big circle color

`$s-al`: Animation length of the small circle. OPTIONAL, STANDARD: Big circle animation length

`$s-ad`: Animation direction of the small circle. OPTIONAL, STANDARD: Reverse (counter-clockwise)

### border

This one is a bit different. You put this one in a parent container of your choosing, the class does
not matter of the parent, only of the border elements. There's 2 elements both using the `:before`
and `:after`. Together making all 4 sides.

NOTE: Make the parent container `position: relative;`

    @mixin create-border-elem($c, $t, $al, $col, $w: 100%, $h: 100%)

`$c`: Classname, this is the base class. if you choose the class `loader-border` you place 2 `div`
items in a parent div of your choosing. The HTML should then look like this:

    <div class="any-class"> <!-- The container that will have the border, this can be anything, this has to be position: relative.  -->
        <div class="loader-border-lefttop"></div> <!-- these 2 elements are both needed -->
        <div class="loader-border-rightbot"></div>
    </div>

`$t`: The thickness of the border in px

`$al`: Animation length

`$col`: Color of the borders

`$w`: The width of the parent. OPTIONAL, STANDARD: 100%

`$h`: The height of the parent. OPTIONAL, STANDARD: 100%

NOTE: If the parent has different width from height. Not giving the width and height will result in
strange results. still looking to fix this, but for now width and height needs to be given.

## Credits

Credit for the horizontal dots loader: https://codepen.io/jenning/pen/rrkBbq. I used his
`cubic-bezier` css animation property, that's it

Credit for the gooey loader: https://codepen.io/Izumenko/pen/MpWyXK. I used this and tried to make
it more customizable

Credit for the border animation: https://codepen.io/PicturElements/pen/ZOwkwv. Got the idea here,
thought it looked cool
