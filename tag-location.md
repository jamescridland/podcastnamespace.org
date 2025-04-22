---
title: "podcast:location"
permalink: /tag/location
---

# <i class="pi pi-tag-location"></i>podcast:location
**A way to list hosts and other people involved with the podcast**

<!-- * [The official specification](https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md#person) -->

- - -

This tag is for you if you want to help your podcast be discovered because of **the place it's about**, or because of **where it's made**.

There is [simple generator code here](https://jamescridland.github.io/podcast-location-generator/) for how to make one of these tags. It's all in JavaScript, and you can view the source and save it for your own use.

The tag is pragmatically built with a number of items. Here's a typical tag for a podcast that is about the Eiffel Tower in France.

```
<podcast:location
 rel="subject"
 geo="geo:48.8529371,2.3500501"
 osm="W201611261"
 country="FR"
>
Cathedral of Notre Dame
</podcast:location>
```

The `country` element is a simple two-character code for the country, and it's here to allow easy identification of countries in a database without having to geo-locate every single location.

The `geo` element puts a point on Planet Earth (or, if it starts with something like `lunar:`, on the moon, perhaps?). You'll be familiar with lat/lon points. The difficulty with lat/lon points is that - well, they're just points. They don't tell you anything about the point. You don't even know how big it is - or what it is. You only know where it is.

So that's why the `osm` element is there. While the osm element is written in the specification as highly recommended but optional, you *lose a lot of the functionality* of this tag if you omit it, so it's, as it says, highly recommended.

### OpenStreetMap and why the OSM element is here

OpenStreetMap is an open, free map that everyone can use. (You can download it if you want a copy, too). It lists a great deal of detail (and you can quickly add things it doesn't list, too). In the example above, it is set to "W" (for 'way', one of the three OpenStreetMap object types), and then the ID of 201611261. [It links here](https://www.openstreetmap.org/way/201611261#map=19/48.852937/2.349870) - it's Notre Dame Cathedral in Paris.

Now, check this one:

```
<podcast:location
 rel="subject"
 geo="geo:48.8588897,2.3200410"
 osm="R7444"
 country="FR"
>
Paris
</podcast:location>
```

This has a really similar lat/lon - it's within 100 meters or so of the other point. You might be forgiven for thinking that it's the same place. But it isn't. It's a podcast [about the city of Paris](https://www.openstreetmap.org/relation/7444#map=12/48.8341/2.3512) - the OSM "Relation" object, ID 7444.

So, one is about "Paris", while one is about a big church. And, while the lat/lon is almost identical, these two are clearly not covering the same place. It would be wrong to put these two as pins on a map, for example.

### Overpass and new ways of finding podcasts

Let's just go back to [Notre Dame Cathedral](https://www.openstreetmap.org/way/201611261#map=19/48.853274/2.348932). Take a look at the data on the left-hand side of OpenStreetMap's page. It's got lots of information about it - it's a cathedral, and it's built in the gothic style.

So, let's consider how you'd make an app that automatically grabs all podcast episodes about cathedrals in France, as one example.

[This link](https://overpass-turbo.eu/s/22Jd) searches OpenStreetMap for all cathedrals in France. On the right is a map - above it, you can switch it to "data", where you'll see all the data about individual cathedrals in France, including [R1373890](https://www.openstreetmap.org/relation/1373890#map=13/49.42320/1.12893), which is a cathedral in Rouen. Is there a podcast about R1373890? That's a simple database lookup.

Oh, and remember I mentioned that Notre Dame was in the gothic style? Let's find [all cathedrals in France in a gothic style](https://overpass-turbo.eu/s/22Jf).

OpenStreetMap is very powerful - you can get it to return, for example, "[all wineries in Adelaide](https://overpass-turbo.eu/s/22Ji)", and very quickly build a wine website covering the area - with links to podcasts about them, where it makes sense. (And, by the way, most AI tools will accept a prompt like "Write a query for Overpass showing all wineries in Adelaide").

Know that this information is there for every object in OpenStreetMap - but also know that *you can't do this with a lat/lon*. 

You might not build this into a podcast app. It might be on a gothic cathedral fan website. It might be a website about wine, or breweries, or railway stations. But the `podcast:location` tag offers really powerful, exciting ways into podcasts that we've simply never had before.

## Support

This is a revised tag, and currently we're unaware of full support for it.
