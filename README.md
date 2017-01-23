# gridder

This plugin was inspired by https://github.com/oriongunning/gridder

I tried both the gridder and the gridder-ajax plugin, but what I needed was
a combination of both with some more options, so I created a new one.

=======

Please note: I'm sorry, this documentation is incomplete. Please open an issue
if you'd like to try this plugin, so I can help you.

=======

## Usage

1. Include jQuery:

	```html
	<script src="http://ajax.googleapis.com/ajax/libs/jquery/2.0.0/jquery.min.js"></script>
	```

2. Include plugin's code:

	```html
	<script src="dist/jquery.gridder.js"></script>
	```

3. Call the plugin:

    ```javascript
    <script>
    $(function() {
        // Call Gridder
        $('ul.gridder').Gridder({
            debug: false,
            scroll: true,
            showNav: true,
            scrollOffset: 0,
            rootUrl: "/",
            animationSpeed: 'slow',
            animationEasing: "easeInOutExpo",
            expander: '.gridder-expander',
            gridderContent: '<li class="gridder-show"></li>',
            showNavTemplate: "<div class=\"gridder-navigation\">" +
                             "<a href=\"#\" class=\"gridder-close\">{{closeText}}</a>" +
                             "<a href=\"#\" class=\"gridder-nav prev\">{{prevText}}</a>" +
                             "<a href=\"#\" class=\"gridder-nav next\">{{nextText}}</a>" +
                             "</div>",
            nextText: "Next",
            prevText: "Previous",
            closeText: "Close",
            showTemplate: "<div class=\"gridder-show loading\"></div>",
            outputTemplate: "{{shownav}}<div class=\"gridder-padding\">" +
                            "<div class=\"gridder-expanded-content\">" +
                            "{{thecontent}}" +
                            "</div></div>",
            onStart: function(){},
            onShow: function(){},
            onClose: function(){},
            onFinish: function(){}	
	});
    });
    </script>
    ```
