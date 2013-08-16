bigSlide is a teeny tiny (~1kb compressed) jQuery plugin for creating off-screen slide panel navigation.

It will slide the navigation panel as well as any containers given the `.push` class (or a class of your choosing in the settings).

## Getting Started

In your document, include a link to toggle the navigation:

	<a href="#menu" class="menu-link">&#9776;</a>
	
And your nav menu:

	<nav id="menu" class="panel" role="navigation">
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">The Ballad of El Goodo</a></li>
            <li><a href="#">Thirteen</a></li>
            <li><a href="#">September Gurls</a></li>
            <li><a href="#">What's Going Ahn</a></li>
        </ul>
	</nav>


Reference jQuery and the big-slide.js file:


	<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
	<script src="jquery.big-slide.js"></script>


To initialize the plugin,:

	<script>
    $(document).ready(function() {
        $('.menu-link').bigSlide();
    });
    </script>
    
## Options

| Variable   | Default Value | Description       |
| ---------- |:-------------:| -----------------:|
| menu       | ('#menu')     | The attribute ID of the navigation menu |
| push       | ('.push')     | The class given to additional elements to 'push' when the nav is toggled  |
| menuWidth  | 15.6em        | The width of the navigation menu |
| speed      | 300           | The speed (in milliseconds) of the navigation menu    |

## Other notes

Although bigSlide will automatically position your menu off screen, I recommend adding the following to your CSS to prevent a flash of the menu on load:

	.panel {
		position: fixed;
		left: -15.625em; /*or width of your navigation panel*/
		width: 15.625em; /*should match the above value*/
	}
	
## License

The MIT License (MIT)

Copyright (c) 2013 Adam Scott

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

