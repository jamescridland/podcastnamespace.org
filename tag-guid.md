---
title: "podcast:guid"
permalink: /tag/guid
---

# <i class="pi pi-tag-guid"></i>podcast:guid
**Used to declare a unique, global identifier for a podcast.**

* [The official specification](https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md#guid)

- - -

## What's the point of this?

Podcasting is decentralized.  There is no single point of registration or tracking.  Also, podcasts move - a lot. This means that keeping track of which feed urls currently go with which podcasts is a real nightmare.

The podcast guid tag does for podcasts what the episode guid tag does for episodes.  It assigns a globally unique ID to every podcast so that the world can know that two different feeds are actually the same thing - or not. Even if the podcast changes RSS address or name, the GUID sticks with it for the rest of its life.

## Support

This is easy to implement for both podcast hosting companies and podcast directories.

It's supported by [large podcast hosts](https://podcastindex.org/apps?appTypes=hosting&elements=guid) including Buzzsprout and Castos.

## An example in the wild

The Podland RSS feed contains: 

```xml
<podcast:guid>396d9ae0-da7e-5557-b894-b606231fa3ea</podcast:guid>
```

Because this GUID will never change, it means that this link:

[https://podnews.net/podcast/396d9ae0-da7e-5557-b894-b606231fa3ea](https://podnews.net/podcast/396d9ae0-da7e-5557-b894-b606231fa3ea)

will also always find the podcast, even though Podnews's podcast pages use a separate, proprietary ID.




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
