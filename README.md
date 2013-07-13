# MapMalaysia

MapMalaysia is a highly customizable choropleth map of Malaysia. As it stands, the map displays population density, mean income and the results from the 2013 general elections in each of Malaysia's states, but the code is easily reusable to display other data.

Code was originally borrowed from the [leaflet choropeth tutorial](http://leafletjs.com/examples/choropleth.html), but has been heavily modified.

The state boundaries were hand drawn using [an online geoJSON editor](http://blog.sallarp.com/google-maps-geojson-editor/).

## Try it out!

There's a github page [here](http://jonnynewbs.github.io/MapMalaysia).

## To do

The states were drawn rather haphazardly to begin with. The way that it should be done is to have two files:

- *frontiers.geosjson* - contains all the definitions for the frontiers between states
- *states.json* - contains the definitions of the states (ie which frontier segments make up the whole state boundary)

Those two files are then compiled into *states.geojson*.

This process has been started, but there's still a lot to do to tidy it up.

## Customizing MapMalaysia

- config.js contains all the config for the choropleth map as well as the geoJSON defining the state shapes. This is where you should look if you want to modify the map for a different country or location.
- stats.json contains the stats for the different Malaysian states. If you want to display different statistics or change the colours on the map, you should modify this file. If you want to use stats from an external server or database, you should modify the ajax_url field in the config.js file and then serve up a stats.json file from your external server.
