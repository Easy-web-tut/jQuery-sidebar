<!---------------------------------------------------------------------------->
<!-- STOP, LOOK & LISTEN!                                                   -->
<!-- ====================                                                   -->
<!-- Do NOT edit this file directly since it's generated from a template    -->
<!-- file, using https://github.com/IonicaBizau/node-blah                   -->
<!--                                                                        -->
<!-- If you found a typo in documentation, fix it in the source files       -->
<!-- (`lib/*.js`) and make a pull request.                                  -->
<!--                                                                        -->
<!-- If you have any other ideas, open an issue.                            -->
<!--                                                                        -->
<!-- Please consider reading the contribution steps (CONTRIBUTING.md).      -->
<!-- * * * Thanks! * * *                                                    -->
<!---------------------------------------------------------------------------->

# jquery-sidebar

A stupid simple sidebar jQuery plugin.

## Available on CDN! :ship:
*jQuery-Sidebar* is available on [CDNJS](https://cdnjs.com/libraries/jquery-sidebar) and you can use it like this:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-sidebar/3.3.1/jquery.sidebar.min.js"></script>
```

## Usage

This library depends on:

 - [jQuery](https://jquery.com/)

Include the script file in your HTML page:

```html
...
<!-- Include jQuery -->
<script src="path/to/jquery.min.js"></script>
<!-- Include jQuery Sidebar -->
<script src="path/to/jquery.sidebar.min.js"></script>
<!-- Or from CDNJS:
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-sidebar/3.3.1/jquery.sidebar.min.js"></script>
-->
...
<div class="sidebar left">Hello World</div>
<div class="sidebar right">I am on right!</div>
<div class="sidebar top">I am on top!</div>
<div class="sidebar bottom">I am on bottom!</div>
...
<script>
    // Sidebar on left (default)
    $(".sidebar.left").sidebar().trigger("sidebar:open");

    // Sidebar on right side
    $(".sidebar.right").sidebar({side: "right"});

    // Sidebar on top side
    $(".sidebar.top").sidebar({side: "top"});

    // Sidebar on bottom side
    $(".sidebar.bottom").sidebar({side: "bottom"});
</script>
...
```

## Documentation

### `sidebar(options)`
Initialize sidebar on selected elements.

```js
$(".my-sidebar").sidebar({...});
```

After the call above, you can programatically open/close/toggle the sidebar using:

```js
$(".my-sidebar").trigger("sidebar:open");
$(".my-sidebar").trigger("sidebar:close");
$(".my-sidebar").trigger("sidebar:toggle");
$(".my-sidebar").trigger("sidebar:close", [{ speed: 0 }]);
```

After the sidebar is opened/closed, `sidebar:opened`/`sidebar:closed` event is emitted.

```js
$(".my-sidebar").on("sidebar:opened", function () {
   // Do something on open
});

$(".my-sidebar").on("sidebar:closed", function () {
   // Do something on close
});
```

#### Params
- **Object** `options`: An object that will be merged with the default options.
 - `speed` (Number): animation speed (default: `200`)
 - `side` (String): left|right|top|bottom (default: `"left"`)
 - `isClosed` (Boolean): A boolean value indicating if the sidebar is closed or not (default: `false`).
 - `close` (Boolean): If `true`, the sidebar will be closed by default.

#### Return
- **jQuery** The jQuery elements that were selected.

## Changelog
To see the versions and the changes between them go to [releases page](https://github.com/jillix/jQuery-sidebar/releases).

## How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].

## License
See the [LICENSE][license] file.

[license]: /LICENSE
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md