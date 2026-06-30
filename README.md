[Instagram Profile Scraper](https://apify.com/figue/instagram-profile-scraper?fpr=data)

# Instagram Profile Scraper — 50+ Fields · Ultra Fast 500/min 🚀 · $1/1K

## 📌 Overview

The most complete and affordable Instagram profile scraper on Apify. Extract **50+ data points** from any public Instagram profile — bio, followers, business info, contact details, bio links, and enriched recent posts with hashtags, mentions, carousel images, and direct video URLs.

Just paste usernames, @handles, or profile URLs → get structured JSON output in seconds.

**⚡ Ultra Fast — 500/min** 🚀 · **📦 50+ fields per profile** · **💰 $1 per 1,000 profiles**

---

## 🚀 Why This Scraper?

✅ **Full API data** — Returns the complete Instagram response. Every field, nothing stripped out. New fields Instagram adds appear automatically.

✅ **Engagement metrics on every post** — Likes, comments, video views, and reshare status included on each post. Calculate engagement rates at scale without extra API calls. Detects when creators hide their metrics (`hide_like_and_view_counts`, `comments_disabled`).

✅ **Enriched posts** — Recent posts come with parsed hashtags, mentions, carousel images with individual dimensions, direct video URLs, alt text, tagged users, coauthor detection, and pinned post flags. Not just captions and likes.

✅ **Bio links included** — Full `bio_links` array with resolved URLs and Instagram tracking links (`lynx_url`). Most scrapers skip this.

✅ **Related profiles** — Instagram's own `edge_related_profiles` suggestions included. Scrape one competitor → discover all similar accounts → scrape those too. Perfect for prospection loops.

✅ **Cross-platform IDs** — Get `fbid` and `eimu_id` to link Instagram profiles to their Meta/Facebook identity. Perfect for cross-platform enrichment.

✅ **Direct video URLs** — Get actual `.mp4` video URLs for Reels and video posts, not just thumbnails. Multiple quality levels available via DASH manifests.

✅ **Account trust signals** — Spot fake or new accounts with `is_joined_recently`, check Meta Verified status, and detect Threads presence — all in one call.

✅ **Ultra Fast — 500/min** 🚀 — Pure HTTP requests, no browser.

✅ **Cheapest on the Store** — $1.00 per 1,000 profiles. No hidden fees. No browser overhead.

---

## 🔧 How It Works

1. **Add profiles** — Paste usernames, @handles, or Instagram URLs
2. **Click Start** — The scraper fetches all public data via Instagram's API
3. **Download results** — Export in JSON, CSV, or Excel

No login required. No cookies. No Instagram account needed.

---

## 📤 What You Get

### 🧑‍💼 Profile Data

| Field | Description |
| --- | --- |
| `username` | Instagram handle |
| `full_name` | Display name |
| `biography` | Bio text |
| `biography_with_entities` | Bio with detected mentions and hashtags |
| `bio_links` | All bio links with resolved URLs and tracking links |
| `external_url` | Primary link in bio |
| `profile_pic_url_hd` | HD profile picture |
| `followersCount` | Number of followers |
| `followsCount` | Number of accounts followed |
| `postsCount` | Total posts |
| `is_verified` | Verified badge |
| `is_private` | Private account flag |
| `is_business_account` | Business account flag |
| `is_professional_account` | Creator/professional flag |
| `category_name` | Business or creator category |
| `business_email` | Contact email (business accounts) |
| `business_phone_number` | Contact phone (business accounts) |
| `business_address_json` | Street address, city, zip (business accounts) |
| `business_contact_method` | Preferred contact method |
| `pronouns` | Pronouns if set |
| `highlight_reel_count` | Number of story highlights |
| `has_clips` | Has Reels |
| `has_guides` | Has Guides |
| `has_channel` | Has broadcast channel |
| `edge_related_profiles` | Similar accounts suggested by Instagram |
| `fbid` | Facebook/Meta profile ID |
| `eimu_id` | Cross-platform Meta entity ID |
| `has_onboarded_to_text_post_app` | Whether the user is on Threads |
| `is_joined_recently` | New account flag — useful for fraud detection |
| `hide_like_and_view_counts` | Whether the profile hides engagement metrics |
| `scrapedAt` | Exact timestamp of when the data was collected |
| ...and more | Every field from Instagram's API is included |

### 🖼️ Recent Posts (up to 12)

| Field | Description |
| --- | --- |
| `shortcode` | Post shortcode |
| `url` | Direct link to the post |
| `caption` | Full caption text |
| `hashtags` | Parsed hashtags from caption |
| `mentions` | Parsed @mentions from caption |
| `likesCount` | Number of likes |
| `commentsCount` | Number of comments |
| `comments_disabled` | Whether comments are turned off |
| `like_and_view_counts_disabled` | Whether engagement counts are hidden on this post |
| `timestamp` | Post date and time |
| `type` | Image, Video, or Sidecar (carousel) |
| `display_url` | Image/video preview URL |
| `video_url` | Direct `.mp4` video URL (videos/Reels) |
| `video_view_count` | View count (videos only) |
| `has_audio` | Whether the video has audio |
| `dimensions` | Width and height |
| `accessibility_caption` | Alt text / AI-generated image description |
| `images` | All carousel image URLs |
| `childPosts` | Individual slides with dimensions, URLs, and types |
| `coauthor_producers` | Collab post partners |
| `pinned_for_users` | Whether the post is pinned |
| `location` | Tagged location data |
| `tagged_users` | Users tagged in the media |

---

## 📦 Example Output

```
{
    "username": "natgeo",
    "full_name": "National Geographic",
    "biography": "Experience the world through the eyes of National Geographic photographers.",
    "bio_links": [
        {
            "url": "https://www.nationalgeographic.com",
            "title": "nationalgeographic.com",
            "link_type": "external"
        }
    ],
    "followersCount": 284000000,
    "followsCount": 150,
    "postsCount": 32000,
    "is_verified": true,
    "is_business_account": true,
    "category_name": "Media/News Company",
    "business_email": "contact@natgeo.com",
    "business_phone_number": "+1 202-857-7000",
    "fbid": "17841400229977610",
    "eimu_id": "100719121328287",
    "has_onboarded_to_text_post_app": true,
    "hide_like_and_view_counts": false,
    "is_joined_recently": false,
    "edge_related_profiles": ["natgeotravel", "natgeowild", "..."],
    "scrapedAt": "2026-02-13T16:25:31.312Z",
    "latestPosts": [
        {
            "shortcode": "ABC123",
            "type": "Sidecar",
            "caption": "A breathtaking view of the Northern Lights #NorthernLights #Iceland",
            "hashtags": ["NorthernLights", "Iceland"],
            "mentions": [],
            "likesCount": 1500000,
            "commentsCount": 3200,
            "comments_disabled": false,
            "timestamp": "2026-02-12T18:00:00.000Z",
            "images": ["https://scontent.cdninstagram.com/v/...1.jpg", "..."],
            "video_url": "https://scontent.cdninstagram.com/o1/v/...video.mp4",
            "video_view_count": 520000,
            "coauthor_producers": [],
            "pinned_for_users": []
        }
    ]
}
```

> The output includes **all fields** from the Instagram API. The example above shows common fields — additional fields may appear depending on account type and API changes.

---

## ⚡ Performance

|  | This Scraper | Browser-based scrapers |
| --- | --- | --- |
| Speed | **Ultra Fast — 500/min** 🚀 | ~1 profile/sec |
| Memory | **1 GB** | 2+ GB |
| Cost per 1,000 | **$1.00** | $3–10 |

---

## 🧠 Use Cases

- **Lead generation** — Find business emails and phone numbers from Instagram profiles at scale
- **Influencer marketing** — Analyze engagement rates, spot hidden metrics, flag suspicious accounts, and compare content categories
- **Competitor analysis** — Track competitor profiles, posting frequency, and bio changes
- **Account discovery** — Use `edge_related_profiles` to snowball from one target profile into hundreds of similar accounts
- **Social media dashboards** — Feed profile data into your analytics tools
- **Market research** — Map businesses by category, location, and audience size
- **CRM enrichment** — Match Instagram handles to contact details and cross-platform Meta IDs
- **Collab tracking** — Detect partnership posts via `coauthor_producers`
- **Fraud detection** — Flag recently created accounts, hidden engagement metrics, and disabled comments

---

## 📬 Support

Questions? Need help? Contact us at **[hello@figue.io](mailto:hello@figue.io)**

---

🚀 **The most complete Instagram profile data at the best price. Start scraping now!**