[Instagram Profile Scraper](https://apify.com/cryptosignals/instagram-profile-scraper?fpr=data)

# Instagram Profile & Posts Scraper 2026 — No API Key

Extract complete Instagram profile data and recent posts from any public account. No Facebook Developer account, no Graph API approval, no login required.

> ⭐ **Free to try** — if this actor saves you time, [leave a quick review](https://apify.com/cryptosignals/instagram-profile-scraper/reviews). It takes 30 seconds and helps other researchers find it.

---

## What It Extracts

Pass one or more Instagram usernames. Get back structured JSON in seconds:

**Profile data**

- Username, full name, biography, website URL
- Follower count, following count, total posts count
- Verified badge status, business account flag, category
- HD profile picture URL
- Profile URL, internal user ID

**Recent posts** (up to 50 per profile)

- Caption text with embedded hashtags and mentions
- Like count, comment count, video view count
- Post type (image, video, carousel)
- Media URL, post URL, timestamp

---

## ⚠️ Session Cookie for Accurate Counts

Without a session cookie, Instagram caps what unauthenticated requests return — follower counts and post counts may come back as 0 or 1. **Add your `sessionid` cookie value in the `sessionCookie` field to get accurate numbers.**

The rest of the data (bio, name, verification, posts) is available without it.

---

## Input Parameters

```
{
  "username": "natgeo, nike, tesla",
  "action": "profile",
  "maxPosts": 24,
  "sessionCookie": ""
}
```

| Field | Type | Default | Description |
| --- | --- | --- | --- |
| `username` | string | required | Instagram handle(s), comma-separated. Accepts `@handle`, full URL, or plain username. |
| `action` | string | `"profile"` | `"profile"` returns profile + recent posts. `"posts"` returns posts only. |
| `maxPosts` | integer | `24` | Max recent posts per profile. Range: 1–50. |
| `sessionCookie` | string | `""` | Your Instagram `sessionid` cookie value. Optional but recommended for full data. |

**Accepted username formats:**

- `natgeo`
- `@nike`
- `https://www.instagram.com/tesla/`
- `natgeo, nike, tesla` (comma-separated list)

---

## Example Output

```
{
  "username": "natgeo",
  "fullName": "National Geographic",
  "biography": "Experience the world through the eyes of National Geographic photographers.",
  "followerCount": 281500000,
  "followingCount": 132,
  "postCount": 29847,
  "isVerified": true,
  "isPrivate": false,
  "category": "Media",
  "externalUrl": "https://natgeo.com",
  "profilePicUrl": "https://instagram.fcdn.net/v/t51.2885-19/...jpg",
  "profileUrl": "https://www.instagram.com/natgeo/",
  "userId": "787132",
  "scrapedAt": "2026-04-23T09:15:42.000Z",
  "recentPosts": [
    {
      "postId": "3398271049123456789",
      "shortcode": "C6xYzAbC1234",
      "type": "GraphImage",
      "caption": "A lion surveys the plains at dawn in Kenya's Masai Mara. #wildlife #kenya #africa",
      "likeCount": 284932,
      "commentCount": 1842,
      "videoViewCount": 0,
      "isVideo": false,
      "imageUrl": "https://instagram.fcdn.net/v/t51.2885-15/...jpg",
      "postUrl": "https://www.instagram.com/p/C6xYzAbC1234/",
      "timestamp": "2026-04-12T08:30:00.000Z"
    },
    {
      "postId": "3398271049123456790",
      "shortcode": "C6xYzAbC5678",
      "type": "GraphVideo",
      "caption": "Deep inside the Amazon — a species no camera has captured before. #nature #discovery",
      "likeCount": 193041,
      "commentCount": 2310,
      "videoViewCount": 4812000,
      "isVideo": true,
      "imageUrl": "https://instagram.fcdn.net/v/t51.2885-15/...jpg",
      "postUrl": "https://www.instagram.com/p/C6xYzAbC5678/",
      "timestamp": "2026-04-09T14:22:10.000Z"
    }
  ]
}
```

---

## Who Uses This

**Influencer marketing teams** — vet creators before signing contracts. Compare follower counts, post frequency, and engagement rates across dozens of accounts in one run instead of opening each profile manually.

**Brand managers** — monitor competitor accounts weekly. Catch changes to bios, track follower milestones, watch which content formats drive the most likes.

**Marketing agencies** — build client reports with real Instagram metrics. Pull profiles for entire client rosters automatically instead of copying numbers by hand.

**Market researchers & academics** — analyze posting patterns, engagement benchmarks, and content trends across accounts in a niche. Export to CSV for analysis in Python or R.

**Lead generation** — build lists of active creators filtered by follower thresholds, post frequency, and category.

---

## Why Not Use the Official Instagram Graph API?

Instagram's Graph API requires a Facebook Developer account, app review, business verification, and only returns data for accounts you manage or that have explicitly granted permissions. For third-party research on public profiles, it is effectively unusable.

This actor works on any **public** profile instantly — no approvals, no waiting, no account dependencies.

---

## Integrations & Export

Results export to **JSON**, **CSV**, or **Excel** directly from the Apify console. Connect to:

- **Google Sheets** — sync actor output automatically
- **Webhooks** — push results to your own backend on run completion
- **Zapier / Make** — trigger downstream workflows
- **Apify API** — call from your own code using the Apify Python or Node.js client

Schedule runs hourly, daily, or weekly to track accounts over time.

---

## Limits

- Public profiles only — private accounts are skipped
- Maximum 50 posts per profile per run
- Add a session cookie for accurate follower/post counts

---

## 💰 Pricing

This actor uses **Pay-Per-Result (PPE)** pricing — **$0.005 per profile scraped**. You only pay for successful results, not for platform compute time.

- 100 profiles = $0.50
- 1,000 profiles = $5.00
- 10,000 profiles = $50.00

Free tier users can run the actor to test before committing to a paid plan.

---

## ⭐ Leave a Review

If this actor saved you time, **please take 30 seconds to leave a review**: 👉 [https://apify.com/cryptosignals/instagram-profile-scraper/reviews](https://apify.com/cryptosignals/instagram-profile-scraper/reviews)

Reviews are the primary way this actor reaches new users and gets maintained and updated.