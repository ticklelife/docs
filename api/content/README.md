# Overview
Tickle.Life Content Partner API let's you get access to all stories published on Tickle.Life, via a simple to use API. To apply for a partner-access-api write to us at social@tickle.life.

## Endpoint for All Content
`POST` `https://www.tickle.life/api/content/`


### Request Body (`Content-Type: application/json`):
```js
{
	"user": "<user>",
	"key": "<API KEY>",
	"count": 10, // default: 10
	"page": 1 // default: 1,
	"sort": "published" // or "updated" (default: "published"
	"ignore_header": true // Option. Ignores headings from excerpt
}
```

### Success Response Object:
```js
{
    "hits": [
        {
            "title": "<Post title>",
            "excerpt": "<Plain text excerpt>",
            "slug": "<datetime>",
            "published_at": "<datetime>",
            "updated_at": "<datetime>",
            "published_at": "<human friendly datetime>",
            "updated_at_human": "<human friendly datetime>",
            "thumbnail_url": "<thumbnail-url>",
            "link": "<original-post-url>",
            "author": {
                "link": "<author-profile-url>",
                "full_name": "<author-full-name>",
                "bio": "<author-bio>",
                "image": "<author-image-url>"
            }
        }
        ... // list
    ],
    "total": <count-of-articles>
}
```


---


## Endpoint for Single Content
`POST` `https://www.tickle.life/api/content/<slug>/`


### Request Body (`Content-Type: application/json`):
```js
{
	"user": "<user>",
	"key": "<API KEY>",
}
// Please note that the post-slug is passed in the URL
```

### Success Response Object:
```js
{
    "hits": [
        {
            "title": "<Post title>",
            "excerpt": "<Plain text excerpt>",
            "slug": "<datetime>",
            "published_at": "<datetime>",
            "updated_at": "<datetime>",
            "published_at": "<human friendly datetime>",
            "updated_at_human": "<human friendly datetime>",
            "thumbnail_url": "<thumbnail-url>",
            "link": "<original-post-url>",
            "author": {
                "link": "<author-profile-url>",
                "full_name": "<author-full-name>",
                "bio": "<author-bio>",
                "image": "<author-image-url>"
            }
        }
    ],
    "total": 1
}
```
