---
title: "podcast:funding"
permalink: /tag/funding
---

# <i class="pi pi-tag-funding"></i>podcast:funding
**A simple link, or links, to methods to help fund or donate to a podcast.**

* [The official specification](https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md#funding)

- - -

This tag is for you if you have a PayPal or Patreon page that asks your listeners for donations.

You can use it to link anywhere: services like _Buy Me A Coffee_, or even a [Stripe payment link](https://stripe.com/en-au/payments/payment-links), like [this $5 tip jar](https://buy.stripe.com/6oEbLU2OC6cG22c144) that Podnews set up. Or, you can use it to go to a page with details about advertising or support.

## An example of how to use it

This goes in the `<channel>` section of your RSS feed. You can have more than one link according to the specification.

```
<podcast:funding url="https://www.example.com/donations">Give us donations</podcast:funding>
```

## An example in the wild

The Podnews RSS feed contains: `<podcast:funding url="https://podnews.net/article/advertising">Support us</podcast:funding>`

### <i class="pi pi-antennapod"></i> AntennaPod

It is given a prominent place in the podcast information UX:

![Screenshot_20220815-220530](https://user-images.githubusercontent.com/231941/184632448-2b715e7f-bc27-4ad0-be3e-358bd804c1ad.png)

## Support

It's supported by [a number of larger podcast apps](https://podcastindex.org/apps?appTypes=app&elements=Funding) including _Podcast Addict_ and _AntennaPod_, two larger podcast apps for Android.

It's supported by [large podcast hosts](https://podcastindex.org/apps?appTypes=hosting&elements=Funding) including Buzzsprout, RSS.com, Powerpress by Blubrry, and Transistor.

