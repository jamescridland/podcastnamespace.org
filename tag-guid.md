---
title: "podcast:guid"
permalink: /tag/guid
---

# <i class="pi pi-tag-guid"></i>podcast:guid
**Used to declare a unique, global identifier for a podcast.**

* [The official specification](https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md#guid)

- - -

## What's the point of this?

Podcasting is decentralized.  There is no single point of registration or tracking.  Also, podcasts move - a lot.  
This means that keeping track of which feed urls currently go with which podcasts is a real nightmare.  The podcast
guid tag does for podcasts what the episode guid tag does for episodes.  It assigns a globally unique ID to every
podcast so that the world can know that two different feeds are actually the same thing - or not.


## An example of how to use it

This goes in the `<channel>` section of your RSS feed. You should only ever put one of these in your feed.

```xml
<podcast:guid>917393e3-1b1e-5cef-ace4-edaa54e1f810</podcast:guid>
```

## Support

This is easy to implement for both podcast hosting companies and podcast directories.

It's supported by [large podcast hosts](https://podcastindex.org/apps?appTypes=hosting&elements=guid) including Buzzsprout and Castos.

## An example in the wild

The Podnews RSS feed contains: 

```xml
<podcast:guid>9b024349-ccf0-5f69-a609-6b82873eab3c</podcast:guid>
```



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
