---
title: "podcast:person"
permalink: /tag/person
---

# <i class="pi pi-tag-person"></i>podcast:person
**A way to list hosts and other people involved with the podcast**

* [The official specification](https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md#person)

- - -

This tag is for you if you want to highlight the people involved in your podcast: your hosts, guests, composers and other people.

It defaults to a simple way to list your hosts, but you can use the [full podcast taxonomy list](https://podcasttaxonomy.com/) here, to highlight almost everyone in your podcast that you think is deserving of a credit.

Some podcast directories might use this to enhance search (so, by searching for a person it finds all the podcasts they're associated with, for example).

## Support

This is easy to implement for both podcast hosting companies and podcast apps.

It's supported by [a number of larger podcast apps](https://podcastindex.org/apps?appTypes=app&elements=Funding) including _Podcast Addict_ and _AntennaPod_, two larger podcast apps for Android. It has passed the Apple app store review for at least six iOS apps.

It's supported by [large podcast hosts](https://podcastindex.org/apps?appTypes=hosting&elements=Funding) including Buzzsprout, RSS.com, Powerpress by Blubrry, and Transistor.

## Suggestions

The specification allows for images and links for each contributor. Sanitising these fields before display is recommended.

You might want to use Google's suggested `rel="ugc"` attribute to the links, to signal that these are user generated content. You might also consider caching and resizing the images for each person, to ensure fast page loads and lower bandwidth costs for podcasters.

## An example in the wild

The Buzzcast podcast contains, in the `<channel>` element,
```xml
 <podcast:person role="host" href="https://twitter.com/albanbrooke" img="https://storage.buzzsprout.com/variants/byutxwmvq601x1sny2gtnsyc3fmd/101950687c70b7e2f9ca148685b2ebc23e16838eb1d84e62f976687a774717da.jpeg">Alban Brooke</podcast:person>
  <podcast:person role="host" img="https://storage.buzzsprout.com/variants/iwguve03cmi6mwynebgillvq88q2/101950687c70b7e2f9ca148685b2ebc23e16838eb1d84e62f976687a774717da.jpeg">Kevin Finn</podcast:person>
```

### Podcast Guru

Podcast Guru uses the supplied images, as well as the names of the hosts.

![IMG_0088](https://user-images.githubusercontent.com/231941/188256866-9d4c70d2-dd0a-4e32-a7f0-8400f9e167ef.PNG)

### PodcastAddict

PodcastAddict displays supplied images in its information page. You can click the image to open the website link, and search for that person in new podcasts.

![Screenshot_20220903-151107](https://user-images.githubusercontent.com/231941/188256905-ffb1d5c9-4d44-40a8-9dbb-91eac9fcb4d0.png)

### Podnews

[Podnews displays](https://podnews.net/podcast/i6i6) the names of the hosts and the links. It filters for hosts only.

<img width="884" alt="Screen Shot 2022-09-03 at 3 00 19 pm" src="https://user-images.githubusercontent.com/231941/188256535-4dd315c3-ce5c-41e2-973b-299941b8e1be.png">

<script src="https://giscus.app/client.js"
        data-repo="jamescridland/podcastnamespace.org"
        data-repo-id="R_kgDOH0hJuA"
        data-category="General"
        data-category-id="DIC_kwDOH0hJuM4CQ1a_"
        data-mapping="title"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="bottom"
        data-theme="preferred_color_scheme"
        data-lang="en"
        data-loading="lazy"
        crossorigin="anonymous"
        async>
</script>
