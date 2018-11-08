# Animation, data retrieval all-in-one with Greensock and Waypoint

### Updates - had to change the DB setup a bit and how the event handing works

I updated the label row in the DB to match the IDs on the SVGs themselves, not the section tags. This works a little better - you can't add event handling to object tags (forgot about that). There are other ways to do this by exposing the functionality in the main .js file to the script inside the SVGs - if you're having issues making this work, we can discuss over the weekend / next week (send repo links with questions).

When you mouseover the top graphic, the XHR (fetch) request gets fired via the getData function invocation at the end of the runAnimation function. It passes the ID through to the getData function, which in turn runs the php file and passes that ID in as a query parameter.

Data comes back, gets passed into the parseData function, at which point you can do whatever you want with it. Refer to last week's car example to see how to put data into HTML elements (it'll be pretty similar for SVG text).

Good luck!

TVR