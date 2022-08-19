---
title: "podcast:transcript"
permalink: /tag/transcript
---

# <i class="pi pi-tag-transcript"></i>podcast:transcript
**A link to transcripts and/or captions for a podcast episode**

* [The official specification](https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md#transcript)

- - -

This tag enables:

* **closed captions**, or **subtitles** - timed text appearing on-screen alongside the audio
* **transcripts** - a document containing the full text of a podcast episode

These are vital for accessibility: those who are deaf or hard of hearing, or for those temporarily unable to listen to the audio.

They can also be used for indexing podcasts for search engines, allowing users deep-search into a podcast's content, rather than merely the description or title.

Transcripts or closed captions can also be used to better identify appropriate advertising alongside content, or to ensure brand safety for advertisers who wish to avoid appearing alongside certain subject matter.

## Objections

_"On-device captioning exists on many operating systems"_ or _"Podcast apps can automatically transcribe audio on demand"_ : this is fine as a fall-back where captions don't exist, but automated transcripts are not 100% accurate, and may open up podcasters or app developers to legal challenge. As one example: "Margaret Thatcher beat miners" is historically accurate, but "Margaret Thatcher beat minors" is not; and an allegation of child-beating against a former UK Prime Minister might be sub-optimal.

_"We have the technology to auto-transcribe, so we'll use that"_ : in order to properly respect creators' work, your app or service should use a transcript if one is presented to you through the RSS feed, which may be corrected and better quality than an automatic version.

_"This doesn't work with DAI"_ - this is only true for timed captions, not for transcripts. It's possible to overcome using consistently-timed ad insertion material, or with dynamically-produced caption files. A further revision of this specification may also be able to anchor chapter markers on specific markers within the audio.

## An example of how to use it

This goes in the `<item>` section of your RSS feed. A link to closed-captions:

```
<podcast:transcript
 url="https://mp3s.nashownotes.com/PC20-97-Captions.srt"
 type="application/srt"
/>
```

A link to a transcript:

```
<podcast:transcript
 url="https://podnews.net/transcript/blubrry-programmatic"
 type="text/html"
/>
```

## Support

### Podcast hosting companies
This is simple to implement for podcast hosting companies. The file can exist on a third-party website, so this work can be provided by a subcontractor or service that a podcaster may wish to use. Transcripts may be a product differentiator for you, or you may be able to achieve additional revenue by providing this service in a premium tier.

It's one of the most well-supported tags by [large podcast hosts](https://podcastindex.org/apps?appTypes=hosting&elements=Transcript), including Buzzsprout, Captivate, Fireside and RSS.

### Podcast apps

For podcast apps, linking to transcripts is a simple webview with accompanying UX.

For captions in playback, libraries already exist to decode and play subtitle files, which are easily associated with media playback controls.

Both the [CC] icon and a subtitle icon are [part of Android's Material Icon](https://fonts.google.com/icons?icon.query=caption) set, while a [caption icon](https://podnews.net/uploads/caption-icon.png) is available in iOS and macOS's SF Symbols set.

It's supported by [a number of larger podcast apps](https://podcastindex.org/apps?appTypes=app&elements=Transcript) including _Podcast Addict_, one of the more popular podcast apps for Android, along with PodLP for KaiOS devices, and a wide variety of apps for iOS, Android and the web.

## Examples in the wild

The Podcasting 2.0 show ([RSS](http://mp3s.nashownotes.com/pc20rss.xml)) includes closed captions, using an SRT file.

Listen on the web [using PodFriend](https://web.podfriend.com/podcast/podcasting-20/9485400086) - click "play this episode" to see the closed captions automatically appearing as you listen.

<iframe width="300" height="300" src="https://www.youtube-nocookie.com/embed/o_DftGS5f88" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

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
