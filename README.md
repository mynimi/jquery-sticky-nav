# jquery.stickyNav
a lightweight(1KB) jquery plugin to create a true sticky navbar

## What does it do?
This is a very simple plugin to make navbars sticky, without any visible jump as the state of the navbar changes.

## How do you use it?
You want to include jQuery, then this plugin within your page and then call it upon the nav you want to make sticky.

Check out the minimal example below.

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Your Page</title>
        <link href="css/style.css" rel="stylesheet">
    </head>
    <body>
        <!-- header -->
        <header>
            <h1>My awesom header</h1>
        </header>

        <!-- navigation -->
        <nav class="my-navigation">
            <a href="#">Item</a>
            <a href="#">Item</a>
            <a href="#">Item</a>
        </nav>
        <!-- /navigation -->

        <!-- whatever other code you use -->

        <!-- jQuery -->
        <script src="js/jquery.min.js"></script>
        <!-- jQuery Sticky Nav -->
        <script src="js/jquery.stickyNav.min.js"></script>
        <!-- initiate sticky nav -->
        <script>
            $('.my-navigation').stickyNav();
        </script>
    </body>
</html>
```

## How does it work?
the plugin will measure the height of your navigation and then create a placeholder element of the exact same height behind the navigation.

Then as soon as the top of the element has reached the top of the window, the position of the navbar will be changed to fixed, while the placeholder element remains in place.

This will ensure that you won't see a visible little "jump", which sometimes happens with other solutions.

## Are there any options?
Yes, the options you can pass are

**wrapperClass**: the navbar will be wrapped, this is the class added to the element. Default is _'sticky-nav-wrapper'_.

**placeholderClass**: the class of the placeholder element. Default is _'sticky-nav-placeholder'_.

**elementClass** the sticky element itself will get a new class. Default is _'sticky-nav-element'_.

**zIndexValue** the element will get a z-index value. The default is _10_ you might want to amp it up a little maybe.

Options are passed like this:

```js
$('.my-navigation').stickyNav({
    wrapperClass: 'sticky-wrapper',
    placeholderClass: 'sticky-placeholder',
    elementClass: 'sticky-element',
    zIndexValue: 99
});
```

## questions, problems, enhancements
Just open an issue and let me know.