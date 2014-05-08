---
layout: default
---

## How these work

For all of these samples a new window will pop up separately with a defined height and width. In that window will be the submission form for whichever social network is being used populated with the content specified in the parameter fields.

To use, copy the code listed and update the content in the paramter areas. If you prefer to use an image instead of text, just have the anchor tag wrap an `img` tag.

*You must encode all the URLs you use within the sharer URL.*

## Twitter

Twitter allows you to send a tweet and takes the text of the tweet as its only parameter.

<a class="example" href="http://twitter.com/intent/tweet?text={{ site.name }} {{ site.encodedUrl }} via @{{ site.twitter }}" onclick="window.open(this.href, 'twitterwindow','left=20,top=20,width=600,height=300,toolbar=0,resizable=1'); return false;">Tweet this</a>

Snippet:

``` html
<a href="http://twitter.com/intent/tweet?text=[TWEET_CONTENT_GOES_HERE]" onclick="window.open(this.href, 'twitterwindow','left=20,top=20,width=600,height=300,toolbar=0,resizable=1'); return false;">Tweet this</a>
```

## Facebook

Facebook allows you to share a webpage and takes a title, summary, url, and image(s) as parameters. This usually performs better if you include open graph meta tags.

<a class="example" href="http://www.facebook.com/sharer.php?s=100&amp;p[title]={{ site.name }}&amp;p[summary]={{ site.description }}&amp;p[url]={{ site.encodedUrl }}&amp;p[images[0]={{ site.encodedUrl }}{{ site.image }}" onclick="window.open(this.href, 'facebookwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Share on Facebook</a>

Snippet

```html
<a href="http://www.facebook.com/sharer.php?s=100&amp;p[title]=[TITLE_GOES_HERE]&amp;p[summary]=[SUMMARY_GOES_HERE]&amp;p[url]=[URL_GOES_HERE]&amp;p[images[0]=[IMAGE_GOES_HERE]" onclick="window.open(this.href, 'facebookwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Share on Facebook</a>
```

Meta Tags

```html
<meta property="og:url" content="">
<meta property="og:image" content="">
<meta property="og:title" content="">
<meta property="og:description" content="">
```

## Tumblr

Tumblr takes a URL and title as parameters.

<a class="example" href="http://www.tumblr.com/share?s=&v=3&u={{ site.encodedUrl }}&t={{ site.name }}" onclick="window.open(this.href, 'tumblrwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Share on Tumblr</a>

Snippet:

```html
<a href="http://www.tumblr.com/share?s=&v=3&u=[URL_GOES_HERE]&u=[TITLE_GOES_HERE]" onclick="window.open(this.href, 'tumblrwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Share on Tumblr</a>
```

## Google+

Google+ just takes a URL as the parameter for the sharer link

<a class="example" href="https://plus.google.com/share?url={{ site.encodedUrl }}" onclick="window.open(this.href, 'googlepluswindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Share on Google+</a>

Snippet:

```html
<a href="https://plus.google.com/share?url=[URL_GOES_HERE]" onclick="window.open(this.href, 'googlepluswindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Share on Google+</a>
```

## Pinterest

Pinterest let's you pin images or video and takes the media, a URL, media type, and a description as parameters.For the `is_video` parameter, select `true` or `false`.

<a class="example" href="http://pinterest.com/pin/create/bookmarklet/?media={{ site.encodedUrl }}{{ site.image }}&url={{ site.encodedUrl }}&is_video=false&description={{ site.description }}" onclick="window.open(this.href, 'pinterestwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Pin this!</a>

Snippet:

```html
<a href="http://pinterest.com/pin/create/bookmarklet/?media=[IMAGE_GOES_HERE]&url=[URL_GOES_HERE]&is_video=[true|false]&description=[DESCRIPTION_GOES_HERE]" onclick="window.open(this.href, 'pinterestwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Pin this!</a>
```

## Reddit

Reddit takes a URL and Title for the post.

<a class="example" href="http://www.reddit.com/submit?url={{ site.encodedUrl }}&title={{ site.name }}" onclick="window.open(this.href, 'redditwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Post to Reddit</a>

Snippet:

```html
<a href="http://www.reddit.com/submit?url=[URL_GOES_HERE]&title=[TITLE_GOES_HERE]" onclick="window.open(this.href, 'redditwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Post to Reddit</a>
```

## Hacker News

Hacker News takes a URL and Title for the post.

<a class="example" href="http://news.ycombinator.com/submitlink?u={{ site.encodedUrl }}&t={{ site.name | url_param_escape }}" onclick="window.open(this.href, 'hackernewswindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Submit to Hacker News</a>

Snippet:

```html
<a href="http://news.ycombinator.com/submitlink?u=[URL_GOES_HERE]&t=[TITLE_GOES_HERE]" onclick="window.open(this.href, 'hackernewswindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Submit to Hacker News</a>
```

## Buffer App

Buffer App takes a URL and Title for the post.

<a class="example" href="http://bufferapp.com/add?text={{ site.name }}&url={{ site.encodedUrl }}" onclick="window.open(this.href, 'bufferwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Queue on Buffer</a>

Snippet:

```html
<a href="http://bufferapp.com/add?text=[TITLE_GOES_HERE]&url=[URL_GOES_HERE]" onclick="window.open(this.href, 'bufferwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Queue on Buffer</a>
```

## Digg

Digg takes a URL and Title for the post.

<a class="example" href="http://digg.com/submit?url={{ site.encodedUrl }}&title={{ site.name }}" onclick="window.open(this.href, 'diggwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Submit to Digg</a>

Snippet:

```html
<a href="http://digg.com/submit?url=[URL_GOES_HERE]&title=[TITLE_GOES_HERE]" onclick="window.open(this.href, 'diggwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Submit to Digg</a>
```

## LinkedIn

LinkedIn takes a URL and Title for the post.

<a class="example" href="http://www.linkedin.com/shareArticle?url={{ site.encodedUrl }}&title={{ site.name }}" onclick="window.open(this.href, 'linkedinwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Post on LinkedIn</a>

Snippet:

```html
<a href="http://www.linkedin.com/shareArticle?url=[URL_GOES_HERE]&title=[TITLE_GOES_HERE]" onclick="window.open(this.href, 'linkedinwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Post on LinkedIn</a>
```

## StumbleUpon

StumbleUpon takes a URL and Title for the link.

<a class="example" href="http://www.stumbleupon.com/submit?url={{ site.endcodedUrl }}&title={{ site.name }}" onclick="window.open(this.href, 'stumbleuponwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Post on StumbleUpon</a>

Snippet:

```html
<a href="http://www.stumbleupon.com/submit?url=[URL_GOES_HERE]&title=[TITLE_GOES_HERE]" onclick="window.open(this.href, 'stumbleuponwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Post on StumbleUpon</a>
```

## Delicious

Delicious takes a URL and Title for the link, and also takes a "provider" naming the company that provided the link.

<a class="example" href="https://delicious.com/save?v=5&provider={{ site.author }}&noui&jump=close&url={{ site.encodedUrl }}&title={{ site.name }}" onclick="window.open(this.href, 'deliciouswindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Save this on Delicious</a>

Snippet:

```html
<a href="https://delicious.com/save?v=5&provider=[PROVIDER_GOES_HERE]&noui&jump=close&url=[URL_GOES_HERE]&title=[TITLE_GOES_HERE]" onclick="window.open(this.href, 'deliciouswindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Save this on Delicious</a>
```
