[Instagram Profile Scraper](https://apify.com/logical_scrapers/instagram-profile-scraper?fpr=data)

# Instagram Profile Scraper

---

![banner](https://images.apifyusercontent.com/ioXP7_K9_t3aTwlcoZRo5D0qT9TcXSCUNDrRgnLY_Kw/w:1800/cb:1/aHR0cHM6Ly9pLmliYi5jby9oMWNzNEZIZy9TY3JlZW5zaG90LTIwMjYtMDMtMzAtYXQtMTEtMjctNTktUE0ucG5n.webp)

---

An [Apify](https://apify.com/logical_scrapers/instagram-profile-scraper) actor that extracts comprehensive user profile information from Instagram accounts. Process multiple usernames and extract detailed profile data including contact information, social media links, business details, and more.

## Features

- **No authentication required** — scrapes public profiles without cookies
- **Contact extraction** — emails and phone numbers from bios + business info
- **Social media link detection** — identifies links to other platforms
- **Built-in retries** — automatic retry with session rotation on failures
- **Proxy support** — residential proxy configuration for reliable scraping
- **Multi-username support** — process multiple profiles in a single run

## Input Configuration

```
{
    "usernames": ["bigfootvlog", "instagram", "cristiano"],
    "proxyConfiguration": {
        "useApifyProxy": true,
        "apifyProxyGroups": ["RESIDENTIAL"]
    }
}
```

| Field | Type | Description |
| --- | --- | --- |
| `usernames` | array | List of Instagram usernames to scrape (with or without @) |
| `proxyConfiguration` | object | Apify proxy configuration (residential recommended) |

## Output Format

```
{
    "name": "Bigfoot Vlog",
    "username": "bigfootvlog",
    "id": "1234567890",
    "category": "Digital Creator",
    "businessCategory": "Creator",
    "overallCategory": "Creator",
    "categoryEnum": "CREATOR",
    "bio": "Digital creator | contact@bigfootvlog.com",
    "bioLinks": [{ "title": "", "url": "https://bigfootvlog.com", "linkType": "external" }],
    "homepage": "https://bigfootvlog.com",
    "followers": 50000,
    "follows": 1000,
    "facebookId": "17841400000000000",
    "isPrivate": false,
    "isVerified": true,
    "isBusinessAccount": true,
    "isProfessionalAccount": true,
    "hasClips": true,
    "hasGuides": false,
    "hasChannel": false,
    "highlightReelCount": 5,
    "pinnedChannelsListCount": 0,
    "pronouns": [],
    "businessContactMethod": "CALL",
    "profileImage": "https://scontent.cdninstagram.com/...",
    "profileImageStandard": "https://scontent.cdninstagram.com/...",
    "videoCount": 150,
    "videos": [],
    "imageCount": 300,
    "images": [],
    "savedCount": 0,
    "collectionsCount": 0,
    "relatedProfiles": ["similar_user1", "similar_user2"],
    "biographyWithEntities": {},
    "businessEmail": "contact@bigfootvlog.com",
    "businessPhone": "+1-555-123-4567",
    "allEmails": ["contact@bigfootvlog.com"],
    "allPhoneNumbers": ["+1-555-123-4567"],
    "socialLinks": ["https://twitter.com/bigfootvlog"],
    "websiteLinks": ["https://bigfootvlog.com"],
    "hasContacts": true,
    "success": true
}
```

| Field | Type | Description |
| --- | --- | --- |
| **Profile** |  |  |
| `name` | string | Full name / display name |
| `username` | string | Instagram username |
| `id` | string | Unique Instagram ID |
| `bio` | string | Biography text |
| `bioLinks` | array | Links from bio (title, url, linkType) |
| `homepage` | string | External website URL |
| `profileImage` | string | High-quality profile picture URL |
| `profileImageStandard` | string | Standard profile picture URL |
| `pronouns` | array | User pronouns |
| **Statistics** |  |  |
| `followers` | number | Follower count |
| `follows` | number | Following count |
| `videoCount` | number | Number of videos/reels |
| `imageCount` | number | Number of posts |
| `savedCount` | number | Number of saved posts |
| `collectionsCount` | number | Number of collections |
| `highlightReelCount` | number | Number of story highlights |
| **Account Status** |  |  |
| `isPrivate` | boolean | Whether account is private |
| `isVerified` | boolean | Whether account is verified |
| `isBusinessAccount` | boolean | Whether it's a business account |
| `isProfessionalAccount` | boolean | Whether it's a professional account |
| `hasClips` | boolean | Whether account has reels |
| `hasGuides` | boolean | Whether account has guides |
| `hasChannel` | boolean | Whether account has a channel |
| **Business Info** |  |  |
| `category` | string | Primary category |
| `businessCategory` | string | Business category |
| `overallCategory` | string | Overall category |
| `categoryEnum` | string | Category enum value |
| `businessContactMethod` | string | Preferred contact method |
| `facebookId` | string | Linked Facebook ID |
| **Contact Info** |  |  |
| `businessEmail` | string | Business email from profile |
| `businessPhone` | string | Business phone from profile |
| `allEmails` | array | All emails (extracted from bio + business) |
| `allPhoneNumbers` | array | All phone numbers (extracted from bio + business) |
| `socialLinks` | array | Social media profile links found in bio |
| `websiteLinks` | array | Non-social website links found in bio |
| `hasContacts` | boolean | Whether profile has any contact info |
| **Media** |  |  |
| `videos` | array | Recent videos with metadata (id, shortcode, views, likes, etc.) |
| `images` | array | Recent posts with metadata (id, shortcode, likes, etc.) |
| `relatedProfiles` | array | Related/suggested usernames |
| `biographyWithEntities` | object | Bio with tagged entities |
| **Meta** |  |  |
| `success` | boolean | Whether scraping was successful |

## Author

Created by [Goldmine](https://apify.com/logical_scrapers)

## Support

For issues and feature requests, please use the Issues tab or reach out to **[coredev.dan@gmail.com](mailto:coredev.dan@gmail.com)**

Don't forget to star this actor if you find it useful!

## Other useful and related actors by Goldmine

- [Instagram Posts with Comments Scraper](https://apify.com/logical_scrapers/instagram-post-comments-scraper)
- [X (Twitter) Profile Scraper](https://apify.com/logical_scrapers/x-twitter-user-profile-tweets-scraper)

---

instagram scraper, lead generation, automation, how to scrape instagram profile, instagram emails extraction, instagram data extraction, instagram data scraping, instagram contact extraction, apify actor