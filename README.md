[Instagram Profile Scraper](https://apify.com/joyouscam35875/instagram-profile-scraper?fpr=data)

# Instagram Profile Scraper — 50% Cheaper, No Login Required 📸

Extract Instagram profile data **without browser automation and without logging in**. Pure API-based scraping — fast, reliable, and half the price of alternatives.

> ⚡ ~2 seconds per profile vs 8-15 seconds with browser-based scrapers

---

## ✨ Key Features

- 💰 **50% cheaper** — $1.50 per 1,000 profiles vs $3.50+ for alternatives
- 🔓 **No login needed** — no Instagram credentials required
- ⚡ **2s per profile** — pure HTTP, no browser overhead
- 📊 **Full metrics** — followers, following, posts, engagement data
- 📸 **Recent posts** — up to 12 posts with likes, comments, captions
- 🏢 **Business data** — category, website, verified status

---

## 💰 How Much Does It Cost?

| Profiles | This Actor | Apify Instagram Scraper | You Save |
| --- | --- | --- | --- |
| 100 | **$0.15** | $0.35 | 57% |
| 1,000 | **$1.50** | $3.50 | 57% |
| 10,000 | **$15.00** | $35.00 | 57% |

**No browser compute = lower cost.** You only pay for API processing, not Chromium rendering.

---

## 🚀 Getting Started (3 Steps)

1. **Enter usernames** — @handles, profile URLs, or plain usernames all work
2. **Enable residential proxy** — recommended for best success rate
3. **Run** — structured profile data in seconds

---

## 📥 Input Example

```
{
    "usernames": [
        "nike",
        "https://www.instagram.com/natgeo/",
        "@cristiano"
    ],
    "resultsLimit": 12,
    "proxy": {
        "useApifyProxy": true,
        "apifyProxyGroups": ["RESIDENTIAL"]
    }
}
```

| Field | Type | Default | Description |
| --- | --- | --- | --- |
| `usernames` | string[] | *required* | Instagram usernames, @handles, or profile URLs |
| `resultsLimit` | integer | 12 | Max recent posts per profile (0-12) |
| `proxy` | object | — | Proxy config (residential recommended) |

---

## 📤 Example Output

```
{
    "username": "cristiano",
    "fullName": "Cristiano Ronaldo",
    "biography": "Futebol é a minha vida 🇵🇹⚽",
    "profilePicUrl": "https://instagram.com/...",
    "followersCount": 648000000,
    "followingCount": 584,
    "postsCount": 3847,
    "isVerified": true,
    "isPrivate": false,
    "isBusinessAccount": true,
    "businessCategory": "Athlete",
    "externalUrl": "https://www.cristianoronaldo.com",
    "recentPosts": [
        {
            "shortcode": "C5xK2a8...",
            "caption": "Always ready to give my best 💪⚽",
            "likesCount": 12500000,
            "commentsCount": 87000,
            "timestamp": 1711234567,
            "imageUrl": "https://instagram.com/...",
            "isVideo": false
        }
    ]
}
```

---

## 🎯 Use Cases

| Who | Use Case |
| --- | --- |
| 📣 **Marketers** | Influencer marketing — evaluate profiles by follower count, engagement, and business category |
| 🔍 **Brand managers** | Brand monitoring — track competitor profiles, follower growth, content strategy |
| 📈 **Agencies** | Lead generation — build lists of business accounts with contact info and websites |
| 📊 **Researchers** | Social media analysis — study engagement patterns across profiles at scale |
| 🛒 **E-commerce** | Find brand ambassadors — identify verified accounts in target niches |

---

## ❓ FAQ

**Q: Do I need an Instagram account?**
No. The scraper works without any login or Instagram credentials.

**Q: Should I use proxies?**
Yes — **residential proxies are strongly recommended**. Instagram blocks datacenter IPs aggressively. Use Apify's residential proxy group (`RESIDENTIAL`) for best results.

**Q: What about private profiles?**
Private profiles return limited public data: username, profile picture, follower/following counts (from meta tags). Posts are not accessible for private accounts.

**Q: What export formats?**
JSON, CSV, Excel (XLSX) — all from the Apify console. Posts are flattened in CSV format.

---

## 📋 Output Fields

| Field | Type | Description |
| --- | --- | --- |
| `username` | string | Instagram username |
| `fullName` | string | Display name |
| `biography` | string | Profile bio text |
| `profilePicUrl` | string | Profile picture URL |
| `followersCount` | integer | Number of followers |
| `followingCount` | integer | Number following |
| `postsCount` | integer | Total posts count |
| `isVerified` | boolean | Blue checkmark status |
| `isPrivate` | boolean | Private account flag |
| `isBusinessAccount` | boolean | Business/creator account |
| `businessCategory` | string | Business category label |
| `externalUrl` | string | Website link from profile |
| `recentPosts` | array | Up to 12 recent posts |
| `recentPosts[].shortcode` | string | Post shortcode/ID |
| `recentPosts[].caption` | string | Post caption text |
| `recentPosts[].likesCount` | integer | Post likes |
| `recentPosts[].commentsCount` | integer | Post comments |
| `recentPosts[].timestamp` | integer | Unix timestamp |
| `recentPosts[].imageUrl` | string | Post image URL |
| `recentPosts[].isVideo` | boolean | Video flag |

---

## ⚙️ How It Works

1. **Multi-strategy extraction** — tries web API, GraphQL, and HTML parsing in sequence
2. **Automatic retries** — exponential backoff on rate limits (429)
3. **Concurrent processing** — up to 5 profiles simultaneously
4. **Graceful degradation** — returns partial data if a profile is restricted

**Runtime:** Python 3.12 · ~128 MB memory · No browser/Playwright

## 🔗 Integration Examples

### Python

```
from apify_client import ApifyClient
client = ApifyClient("YOUR_API_TOKEN")
run = client.actor("joyouscam35875/instagram-profile-scraper").call(run_input={"usernames": ["instagram"]})
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)
```

### Node.js

```
import { ApifyClient } from 'apify-client';
const client = new ApifyClient({ token: 'YOUR_API_TOKEN' });
const run = await client.actor('joyouscam35875/instagram-profile-scraper').call({"usernames": ["instagram"]});
const { items } = await client.dataset(run.defaultDatasetId).listItems();
console.log(items);
```

### Make / Zapier / n8n

Use the Apify integration — search for this actor by name in the Apify app connector. No code needed.

---

## 🔗 More Scrapers by Ken Digital

| Scraper | What it does | Price |
| --- | --- | --- |
| [YouTube Channel Scraper](https://apify.com/joyouscam35875/youtube-channel-scraper) | Videos, stats, metadata via official API | $0.001/video |
| [France Job Scraper](https://apify.com/joyouscam35875/france-job-scraper) | WTTJ + France Travail + Hellowork | $0.005/job |
| [France Real Estate Scraper](https://apify.com/joyouscam35875/france-real-estate-scraper) | 5 sources + DVF price analysis | $0.008/listing |
| [Website Content Crawler](https://apify.com/joyouscam35875/website-content-crawler) | HTML to Markdown for AI/RAG | $0.001/page |
| [Google Trends Scraper](https://apify.com/joyouscam35875/google-trends-scraper) | Keywords, regions, related queries | $0.002/keyword |
| [GitHub Repo Scraper](https://apify.com/joyouscam35875/github-repo-scraper) | Stars, forks, languages, topics | $0.002/repo |
| [RSS News Aggregator](https://apify.com/joyouscam35875/rss-news-aggregator) | Multi-source feed parsing | $0.0005/article |
| [Instagram Profile Scraper](https://apify.com/joyouscam35875/instagram-profile-scraper) | Followers, bio, posts | $0.0015/profile |
| [Google Maps Scraper](https://apify.com/joyouscam35875/google-maps-scraper) | Businesses, reviews, contacts | $0.002/result |
| [TikTok Scraper](https://apify.com/joyouscam35875/tiktok-scraper) | Videos, likes, shares | $0.001/video |
| [Google SERP Scraper](https://apify.com/joyouscam35875/google-serp-scraper) | Search results, PAA, snippets | $0.003/search |
| [Trustpilot Scraper](https://apify.com/joyouscam35875/trustpilot-scraper) | Reviews, ratings, sentiment | $0.001/review |

👉 [View all scrapers](https://apify.com/joyouscam35875)

## ⚠️ Important: Residential Proxies Required

This actor targets platforms with strict anti-bot protection (Cloudflare, fingerprinting).
To successfully scrape data, you must enable **Apify Residential Proxies** in the actor settings.
Go to the Apify Console → Actor → Settings → Proxy configuration → select **Residential proxy pool**.
Without residential proxies, the actor will return 0 results or errors.
✅ Pro tip: The actor is configured for pay-per-event pricing, so you only pay for successful results.