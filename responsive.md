https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries  -- the first sentence uses horrible language and too much jargon "A media query consists of a media type and at least one expression that limits the style sheets' scope by using media features" -- this basically saying a media query, such as:

    @media screen and (max-width: 600px) {
         body {
             background-color: blue;
         }
    }

The first line @media screen is saying 

    ONLY IF THE SCREEN WIDTH (_this condition_) {
          __apply these rules__ 
    }

I'm just going to break down that first sentence because it's pretty dense -- "at least one expression " refers to "max-width: 600px" above: which is saying "apply the rules within my Brackets( {} ) IF the width is AT MOST (width of screen is 0-600)  600px. So, if you add this media query to an HTML page you're working on, you will have a blue background on SMALL screens. the easy way to flip it is change max-width to min-width

And within __appy these rules__ is any CSS rule you would normally write, such as p { font-size: 24 } ... and they have to be surrounded by the brackets of the Media query, think of media queries as IF statements. I looked a little bit and this question and the answers seem to be pretty informative http://stackoverflow.com/q/3619217/3100494

___

Anyway, the relevance here is that for the data-visualization (see README) we don't necessarily want to use bootstrap for making the application responsive. We should use pure media queries rather than the help of bootstrap - we can be more specific this way. Maybe it is as simple as setting the map on the right for large screens, and at the bottom for small screens - or have multipl tabs for small screens, to switch between the map, and the options for narrowing down the markers on the map (the preferences area).
