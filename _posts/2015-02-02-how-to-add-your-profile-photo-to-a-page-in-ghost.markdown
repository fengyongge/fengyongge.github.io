---
title: How to add your profile photo to a page in Ghost
date: '2015-02-02 04:00:00'
tags: [ghost, test]
---

I thought with the new year I should spruce up my online presence. So I decided a new site was in order. I've really enjoyed what I've seen with [Ghost](https://ghost.org" target="_blank) so I decided to have a go with it. It's been smooth sailing so far and I've come across a few tricks that I thought I should share one.  

If you're interested in adding you profile photo to a page and/or template just do the following:

Add this html to the location where you want your profile image shown:

``` html
<img src="{{#if posts.[0]}}{{posts.[0].author.image}}{{else}}{{post.author.image}}{{/if}}" class="profile-image" alt="My Profile Photo"/>
```

Add this to your css file:

``` css
.profile-image {
      position: relative;
      width: 100px;
      height: 100px;
      border: 3px solid #fff;
      border-radius:100%;
}
```

And if all went well you'll see the profile image similar to what you see on this site. Enjoy.