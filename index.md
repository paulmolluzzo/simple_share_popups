## How these work

For all of these samples a new window will pop up separately with a defined height and width. In that window will be the submission form for whichever social network is being used populated with the content specified in the parameter fields.

To use, copy the code listed and update the content in the paramter areas. If you prefer to use an image instead of text, just have the anchor tag wrap an `img` tag.

## Twitter

Twitter allows you to send a tweet and takes the text of the tweet as its only parameter.

``` html
<a href="http://twitter.com/intent/tweet?text=[TWEET_CONTENT_GOES_HERE]" onclick="window.open(this.href, 'twitterwindow','left=20,top=20,width=600,height=300,toolbar=0,resizable=1'); return false;">Tweet</a>
```

## Facebook

Twitter allows you to share a webpage and takes a title, summary, url, and image(s) as parameters. This usually performs better if you include open graph meta tags.

Sharing Link

```html
<a href="http://www.facebook.com/sharer.php?s=100&amp;p[title]=[TITLE_GOES_HERE]&amp;p[summary]=[SUMMARY_GOES_HERE]&amp;p[url]=[URL_GOES_HERE]&amp;p[images[0]=[IMAGE_GOES_HERE]" onclick="window.open(this.href, 'facebookwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Share on FB</a>
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

```html
<a href="http://www.tumblr.com/share?v=3&u=[URL_GOES_HERE]&t=[TITLE_GOES_HERE]" onclick="window.open(this.href, 'tumblrwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Share on Tumblr</a>
```

## Google+

Google+ just takes a URL as the parameter for the sharer link

```html
<a href="https://plus.google.com/share?url=[URL_GOES_HERE]" onclick="window.open(this.href, 'googlepluswindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Share on Google+</a>
```

## Pinterest

Pinterest let's you pin images or video and takes the media, a URL, media type, and a description as parameters.For the `is_video` parameter, select `true` or `false`.

```html
<a href="http://pinterest.com/pin/create/bookmarklet/?media=[IMAGE_GOES_HERE]&url=[_GOES_HERE]&is_video=[TRUE|FALSE]&description=[DESCRIPTION_GOES_HERE]" onclick="window.open(this.href, 'pinterestwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Pin it</a>
```

## Reddit

Reddit takes a URL and Title for the post.

```html
<a href="http://www.reddit.com/submit?url=[URL_GOES_HERE]&title=[TITLE_GOES_HERE]" onclick="window.open(this.href, 'redditwindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Post to Reddit</a>
```

## Hacker News

Hacker News takes a URL and Title for the post.

```html
<a href="http://news.ycombinator.com/submitlink?u=[URL_GOES_HERE]&t=[TITlE_GOES_HERE]" onclick="window.open(this.href, 'hackernewswindow','left=20,top=20,width=600,height=700,toolbar=0,resizable=1'); return false;">Post to Reddit</a>
```


