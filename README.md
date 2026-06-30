[Instagram Profile Scraper](https://apify.com/instaprism/instagram-profile-scraper?fpr=data)

Get instant profile information from any public Instagram account. Retrieve follower counts, following counts, bio, posts count, verification status, business category, and more. Perfect for bulk profile lookups and competitor tracking.

## No Login Required

**Your Instagram account stays safe.** This Actor:

- Does NOT require your Instagram login or cookies
- Uses our own infrastructure to fetch data
- Zero risk of account suspension for you
- Works with any public Instagram profile

Unlike browser extensions or tools that use your account, we handle all scraping server-side. Your credentials are never needed.

## Important: Processing Time

**This Actor returns results almost instantly.** Unlike our other scrapers that extract lists of users or posts, the Profile Scraper uses a fast lookup endpoint.

| Profiles | Expected Time |
| --- | --- |
| 1-10 profiles | 5-15 seconds |
| 50 profiles | 30-60 seconds |
| 100+ profiles | 1-3 minutes |

**Why is this so fast?**
Profile information (follower count, bio, etc.) is retrieved via a lightweight API call. No need to paginate through lists of data.

## What You Get

- **User ID** - Unique Instagram identifier
- **Username** - Instagram handle
- **Full Name** - Display name
- **Biography** - Profile bio text
- **Followers Count** - Number of followers
- **Following Count** - Number of accounts they follow
- **Posts Count** - Total number of posts
- **Verification Status** - Blue checkmark (yes/no)
- **Private Status** - Whether account is private
- **Business Status** - Whether it's a business account
- **Category** - Business category (if applicable)
- **External URL** - Website link in bio
- **Profile Picture URL** - HD profile image

## Input

| Parameter | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `usernames` | Array | Yes | - | List of Instagram usernames (without the @ symbol) |

### Example Input

```
{
    "usernames": [
        "nike",
        "adidas",
        "puma",
        "reebok"
    ]
}
```

## Output

| Field | Type | Example | Description |
| --- | --- | --- | --- |
| `username` | String | "nike" | Instagram username |
| `userId` | String | "13460080" | Unique Instagram user ID |
| `fullName` | String | "Nike" | User's display name |
| `biography` | String | "Just Do It." | Profile bio text |
| `followers` | Integer | 306000000 | Number of followers |
| `following` | Integer | 150 | Number of accounts followed |
| `postsCount` | Integer | 1250 | Total number of posts |
| `isPrivate` | Boolean | false | True if account is private |
| `isVerified` | Boolean | true | True if has blue checkmark |
| `isBusiness` | Boolean | true | True if business account |
| `category` | String | "Sportswear Brand" | Business category |
| `externalUrl` | String | "[https://nike.com](https://nike.com)" | Website link in bio |
| `profilePicUrl` | String | "[https://scontent](https://scontent)..." | HD profile picture URL |
| `scrapedAt` | String | "2026-01-15T10:30:00.000Z" | Timestamp of extraction |

### Example Output

```
[
    {
        "username": "nike",
        "userId": "13460080",
        "fullName": "Nike",
        "biography": "Just Do It. #Nike",
        "followers": 306000000,
        "following": 150,
        "postsCount": 1250,
        "isPrivate": false,
        "isVerified": true,
        "isBusiness": true,
        "category": "Sportswear Brand",
        "externalUrl": "https://nike.com",
        "profilePicUrl": "https://scontent-cdg4-1.cdninstagram.com/v/t51.2885-19/...",
        "scrapedAt": "2026-01-15T10:30:00.000Z"
    },
    {
        "username": "adidas",
        "userId": "12345678",
        "fullName": "adidas",
        "biography": "Through sport, we have the power to change lives.",
        "followers": 275000000,
        "following": 200,
        "postsCount": 980,
        "isPrivate": false,
        "isVerified": true,
        "isBusiness": true,
        "category": "Sportswear Brand",
        "externalUrl": "https://adidas.com",
        "profilePicUrl": "https://scontent-cdg4-1.cdninstagram.com/v/t51.2885-19/...",
        "scrapedAt": "2026-01-15T10:30:01.000Z"
    }
]
```

## Use Cases

- **Influencer Vetting** - Quickly verify follower counts and engagement potential before partnerships.
- **Competitor Tracking** - Monitor competitor growth over time with scheduled runs.
- **Lead Enrichment** - Add Instagram data to your existing lead database.
- **Research & Analysis** - Gather profile data for market research projects.
- **Account Monitoring** - Track changes in your own or client accounts.
- **Bulk Lookups** - Process hundreds of profiles efficiently.

## Integrations

Export your data to:

- **Google Sheets** - Direct integration, auto-sync results
- **Zapier / Make (Integromat)** - Trigger workflows when scrape completes
- **Webhooks** - Get real-time notifications
- **API** - Programmatic access via Apify API
- **Download** - JSON / CSV / Excel files

## FAQ

### Why is this Actor so much faster than others?

Profile data (follower count, bio, etc.) comes from a single API endpoint per profile. Other scrapers need to paginate through lists of followers/posts, which takes time.

### Can I scrape private accounts?

Partially. You'll get basic info (username, full name, profile pic, private status = true) but not follower/following counts or bio for private accounts.

### How accurate are the follower counts?

Follower counts are retrieved in real-time from Instagram. They reflect the current count at the moment of scraping.

### Can I track changes over time?

Yes! Set up scheduled runs via Apify to scrape the same profiles daily/weekly. Compare results to track growth.

### What happens if a username doesn't exist?

Invalid usernames will be skipped and noted in the logs. Other valid usernames will still be processed.

### Is there a limit on how many profiles I can scrape?

No hard limit, but very large batches (1000+) should be split across multiple runs for reliability.

### Do I need an Instagram account?

No. This Actor scrapes public data without requiring any Instagram credentials.

### How often can I run this?

As often as you need. Perfect for real-time lookups or scheduled monitoring.

## Keywords

Instagram profile scraper, Instagram profile data, bulk Instagram lookup, Instagram follower count, Instagram bio scraper, Instagram account info, Instagram competitor tracking, Instagram influencer verification, Instagram profile API, Instagram data extraction

## Need Custom Solutions?

Looking for **custom scraping**, **higher limits**, or **dedicated infrastructure**?

📩 **Contact us:**

- **Telegram:** [@taskforceorange](https://t.me/taskforceorange)
- **Website:** [social-swarm.com](https://social-swarm.com)

We offer:

- Custom actor development
- Enterprise-grade scraping solutions
- Dedicated proxy infrastructure
- White-label integrations
- Priority support

---

*Built with ❤️ by the InstaPrism team*