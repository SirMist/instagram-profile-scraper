[Instagram Profile Scraper](https://apify.com/zerobreak/instagram-profile-scraper?fpr=data)

# Instagram Profile Scraper: Extract Public Instagram Profile Data in Bulk

Instagram Profile Scraper pulls public data from any Instagram account and returns structured JSON. Give it a list of usernames and get back follower counts, following counts, bio text, post totals, verification status, external links, business email, and profile picture URLs. No Instagram login required, no browser needed.

## Use cases

- **Influencer research**: compare follower counts, post totals, and bio links across dozens of accounts without opening Instagram
- **Lead generation**: collect business emails and external URLs from creator or brand profiles in one run
- **Competitor tracking**: monitor follower and post counts for a set of competitors on a recurring schedule
- **Social media audits**: pull profile data to cross-reference Instagram presence with other marketing metrics
- **Recruitment and partnerships**: find contact info and audience size for potential brand partners or content collaborators
- **Market research**: build Instagram profile datasets for specific industries or content categories

## Input

| Parameter | Type | Default | Description |
| --- | --- | --- | --- |
| `username` | string |  | Single Instagram username to scrape (no @ symbol) |
| `usernames` | array |  | List of usernames for bulk Instagram scraping (one per line) |
| `maxItems` | integer | 100 | Maximum profiles to process per run (up to 1,000) |
| `timeoutSecs` | integer | 300 | Overall run timeout in seconds |
| `requestTimeoutSecs` | integer | 30 | Per-request timeout in seconds |
| `proxyConfiguration` | object | Datacenter (Anywhere) | Proxy type and location for requests. Supports Datacenter, Residential, Special, and custom proxies. Optional. |

### Example input

```
{
    "usernames": ["instagram", "apple", "natgeo"],
    "maxItems": 100,
    "proxyConfiguration": { "useApifyProxy": true }
}
```

## What data does this actor extract?

Each profile entry in the dataset looks like this:

```
{
    "username": "instagram",
    "fullName": "Instagram",
    "biography": "Discover what's new. Find what you love.",
    "followersCount": 697000000,
    "followingCount": 511,
    "postsCount": 7419,
    "profilePicUrl": "https://example.cdn.instagram.com/v/profile.jpg",
    "isVerified": true,
    "isPrivate": false,
    "externalUrl": "",
    "profileUrl": "https://www.instagram.com/instagram/",
    "userId": "25025320",
    "category": "Internet company",
    "businessEmail": "",
    "scrapedAt": "2025-03-12T10:30:00.000000+00:00"
}
```

| Field | Type | Description |
| --- | --- | --- |
| `username` | string | Instagram username |
| `fullName` | string | Full display name shown on the profile |
| `biography` | string | Bio text from the profile |
| `followersCount` | integer | Number of followers |
| `followingCount` | integer | Number of accounts followed |
| `postsCount` | integer | Total posts on the profile |
| `profilePicUrl` | string | Profile picture URL (HD when available) |
| `isVerified` | boolean | Whether the account has a verified badge |
| `isPrivate` | boolean | Whether the account is private |
| `externalUrl` | string | External link in the bio |
| `profileUrl` | string | Full Instagram profile URL |
| `userId` | string | Instagram internal user ID |
| `category` | string | Account category (e.g. Brand, Musician, Public Figure) |
| `businessEmail` | string | Business contact email if publicly available |
| `scrapedAt` | string | ISO timestamp of when the data was collected |

## How it works

1. Reads the list of Instagram usernames from input and removes duplicates
2. For each username, calls Instagram's internal profile API with realistic browser headers
3. Parses the JSON response and extracts all available public profile fields
4. Pushes the result to the Apify dataset
5. Rotates proxies between requests to stay under rate limits

## Integrations

Connect Instagram Profile Scraper with other apps and services using [Apify integrations](https://apify.com/integrations). You can integrate with Make, Zapier, Slack, Airbyte, GitHub, Google Sheets, Google Drive, and many more. You can also use [webhooks](https://docs.apify.com/integrations/webhooks) to trigger actions whenever scraping results are ready.

## FAQ

**Can this actor scrape private Instagram profiles?**
No. Private profiles don't expose public data. The actor returns an error entry for private accounts and moves on to the next username.

**Do I need an Instagram account to run this actor?**
No. It scrapes publicly visible profile data without login credentials.

**How many Instagram profiles can I scrape per run?**
Default is 100 profiles per run. Raise it to 1,000 via `maxItems`. For larger batches, split into multiple runs or schedule recurring runs.

**Why use a proxy?**
Instagram rate-limits repeated requests from the same IP. Rotating through Apify's Residential or Datacenter proxies lets you scrape more profiles without hitting blocks.

**What happens if a username doesn't exist?**
The actor pushes an error entry with the username and a short error message, then continues processing the rest of the list.