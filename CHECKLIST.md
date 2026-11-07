English | [简体中文](CHECKLIST.zh-CN.md)

# Website SEO / GEO / AI Visibility Checklist (100 checks)

This checklist tests whether a website can be crawled, understood and cited by search engines and AI assistants. GEO here means Generative Engine Optimization. It has nothing to do with geography or remote sensing.

Passing this list means your site is eligible to be cited. It does not mean AI tools will recommend you. A longer list is not a more powerful one: every check carries an evidence grade, so start with the strongest.

Last updated: 2026-11-07

## Evidence grades

| Grade | Meaning |
|---|---|
| A | Stated by a protocol, standard, official documentation or law |
| B | Public search-engine guidance or industry consensus; effect on AI answers not quantified |
| C | Experience or hypothesis with no public evidence yet; treat as optional |

llms.txt is not on the list: public data does not currently support the claim that it brings citations. See "Common myths" in the README.

## Short on time? Do these 20 first

Checks 1, 2, 5, 7, 8, 11, 14, 18, 19, 20, 28, 30, 54, 55, 56, 61, 62, 71, 75 and 91.

## 1. Crawling and indexing

| # | Check | How to verify | Grade |
|---|---|---|---|
| 1 | Home page and core pages return 200 | Open in a browser, or check the status code with curl -I | A |
| 2 | robots.txt is reachable and does not contain Disallow: / | Open /robots.txt | A |
| 3 | robots.txt does not block CSS, JS or image directories by mistake | Read the rules line by line | B |
| 4 | robots.txt contains a Sitemap line | Read the file | A |
| 5 | A sitemap exists and lists only pages that return 200 and can be indexed | Sample the URLs | A |
| 6 | Sitemap lastmod reflects the real update time | Compare with actual page updates | B |
| 7 | Core pages have no noindex (check both the meta tag and the X-Robots-Tag header) | View source and response headers | A |
| 8 | Each page has a canonical pointing to itself or the correct main version | Check link rel=canonical | A |
| 9 | The site is verified in Search Console and the sitemap is submitted | Check in the console | B |
| 10 | Core pages show as indexed in Search Console | URL Inspection tool | A |

## 2. Technical basics and speed

| # | Check | How to verify | Grade |
|---|---|---|---|
| 11 | Whole site on HTTPS with a valid certificate that is not close to expiry | Browser or an SSL checker | A |
| 12 | http redirects to https with one 301, no chains | Follow hops with curl -I | B |
| 13 | Only one of www and non-www is kept; the other 301s to it | curl -I | B |
| 14 | A non-existent URL returns a real 404 status, not 200 | Open a random URL | A |
| 15 | Server 5xx errors are rare and there is monitoring or a log | Logs or monitoring | B |
| 16 | The site works on a phone: text and buttons are usable | Phone or developer tools | B |
| 17 | Core pages load at acceptable speed (LCP, CLS and so on) | PageSpeed Insights | B |
| 18 | The CDN or firewall does not return 403 or 429 to search and AI crawlers | Request with a crawler User-Agent | B |

## 3. Page structure

| # | Check | How to verify | Grade |
|---|---|---|---|
| 19 | Core text is in the raw HTML, not produced only by scripts | View page source | B |
| 20 | One h1 per page, matching the page topic | View source | B |
| 21 | h2 and h3 form a logical outline | Outline viewer | B |
| 22 | Navigation uses plain links (a href) that crawlers can follow | View source | A |
| 23 | Important pages are within 3 clicks of the home page | Count by hand | B |
| 24 | No orphan pages: every page has at least one internal link pointing to it | Crawler tool | B |
| 25 | The footer links to About, Contact, Privacy and Terms | Look at the footer | B |
| 26 | Main text does not require login or closing a pop-up | Open in a private window | B |
| 27 | Images have alt text that describes what they show | View source | A |

## 4. Titles, descriptions and links

| # | Check | How to verify | Grade |
|---|---|---|---|
| 28 | Every page has a unique title | Crawler tool | A |
| 29 | The title sums up the page, puts the main term first and has a sensible length | Manual | B |
| 30 | The meta description is a full sentence, not a keyword list | Look at it | B |
| 31 | The first screen has one sentence that can be quoted as a definition | Manual | C |
| 32 | Internal link text describes the target page, not "click here" | Look at it | B |
| 33 | No large numbers of dead links (internal and external) | Dead-link checker | B |
| 34 | External links point to trustworthy sources | Manual | B |
| 35 | Breadcrumbs where they apply | Look at it | B |
| 36 | URLs are short, readable and stable; redirects are in place after a redesign | Look at it | B |

## 5. Structured data

| # | Check | How to verify | Grade |
|---|---|---|---|
| 37 | Home page has Organization markup (name, URL, logo, contact) | Rich Results Test or Schema Validator | B |
| 38 | The site has WebSite markup | Same | B |
| 39 | Article pages have Article markup with author and dates | Same | B |
| 40 | JSON-LD matches what is visible on the page and adds no information the page lacks | Compare with the page | A |
| 41 | JSON-LD is valid and has no errors | Schema Validator | A |
| 42 | sameAs points to official social accounts and company profiles | Check the markup | B |
| 43 | FAQ markup is used only for questions and answers that really appear on the page | Compare with the page | A |
| 44 | On service or product pages, prices in the markup match the page | Compare with the page | B |
| 45 | You do not expect any markup to earn a recommendation by itself (Google says no special AI markup is needed) | Manual | A |

## 6. AI crawlers and access policy

| # | Check | How to verify | Grade |
|---|---|---|---|
| 46 | You know which crawlers to allow, for example OAI-SearchBot, PerplexityBot, Bingbot and Googlebot | Read robots.txt | B |
| 47 | Search crawlers and training crawlers (such as GPTBot, Google-Extended, ClaudeBot) are told apart, and the policy is written in robots.txt | Read robots.txt | A |
| 48 | AI-crawler switches on platforms such as Cloudflare agree with the robots.txt policy | Compare the dashboard with the live robots.txt | B |
| 49 | A platform feature that manages or rewrites robots.txt has not changed your rules | Compare the live file with the local one | B |
| 50 | Server logs show visits and status codes from each kind of AI crawler | Logs | B |
| 51 | The pages crawlers fetch do not return large numbers of 404 or 5xx | Logs | B |
| 52 | No rule blocks every request whose User-Agent looks like a bot | Test with crawler User-Agents | B |
| 53 | IndexNow is set up (Bing-based search) | Check the key file and submission records | B |

## 7. Entity and trust signals

| # | Check | How to verify | Grade |
|---|---|---|---|
| 54 | Company legal name, location and contact details are the same in the footer and on the About page | Manual | B |
| 55 | A separate About page says who you are, what you do and since when | Look at it | B |
| 56 | A Contact page exists and the mailbox really receives mail | Send a test email | B |
| 57 | Authors or founders have a byline page linking to a real personal profile | Look at it | B |
| 58 | The company has consistent profiles in business registries and industry directories | Search the company name | B |
| 59 | Official social accounts use the same name and description as the website | Check each one | B |
| 60 | Brand and product names are written the same way across the site | Search the site for variants | B |
| 61 | A privacy policy and terms of service exist and are reachable | Look at them | A |
| 62 | Key numbers state their source, date and basis | Manual | B |
| 63 | Case studies and reviews are real and verifiable, not exaggerated | Manual | B |

## 8. Citable content

| # | Check | How to verify | Grade |
|---|---|---|---|
| 64 | Each article answers one clear question | Manual | B |
| 65 | The first two sentences give the direct answer | Manual | C |
| 66 | Facts are stated in short sentences; numbers carry units and dates | Manual | B |
| 67 | Comparisons use tables or lists, not long paragraphs | Look at it | C |
| 68 | There is a last-updated date, and it is really updated | Look at it | B |
| 69 | Outside conclusions come with a link to the source | Look at it | B |
| 70 | Facts, opinions and your own data are kept apart | Manual | B |
| 71 | No unsupported absolute claims (best, number one, only) | Search the whole site | A |
| 72 | No large blocks of duplicated, stitched-together or mass-produced low-value pages | Manual sampling | A |
| 73 | The same fact is worded consistently on different pages | Compare pages | B |

## 9. Multiple languages and overseas compliance

| # | Check | How to verify | Grade |
|---|---|---|---|
| 74 | Each language has its own URL | Check the URL structure | A |
| 75 | Language versions point to each other with hreflang, including a self-reference | View source | A |
| 76 | x-default points to a suitable default version | View source | A |
| 77 | The html lang attribute matches the page language | View source | A |
| 78 | Prices and terms are the same across language versions | Compare | B |
| 79 | No forced redirect to a language by visitor IP (crawlers would never see the other versions) | Test from different regions | A |
| 80 | For EEA and UK visitors: cookie consent can be declined and no non-essential scripts load before consent | Private window and developer tools | A |
| 81 | The privacy policy says what data is collected, how long it is kept and how to contact you | Read it | A |
| 82 | Company details on LinkedIn, Crunchbase, Product Hunt and similar sites match the website | Check each one | B |
| 83 | If the brand name is generic, use a fixed "brand + category" form | Manual | C |

## 10. China site (for mainland China visitors)

| # | Check | How to verify | Grade |
|---|---|---|---|
| 84 | The footer shows the ICP filing number and links to the official lookup page | Look at the footer | A |
| 85 | The filing entity matches the site operator | Check the filing record | A |
| 86 | No extreme wording that advertising law restricts | Search the whole site | A |
| 87 | Cited data states its source and validity period | Manual | B |
| 88 | Speed is tested from several mainland carriers | Speed test tool | B |
| 89 | No dependence on third-party resources (fonts, scripts, maps) that cannot be reached in China | Open from a mainland network | B |
| 90 | If you offer AI-generated services, check whether filing and labelling duties apply | Check current rules or ask a professional | A |

## 11. Measuring and re-testing

| # | Check | How to verify | Grade |
|---|---|---|---|
| 91 | Prepare a fixed set of questions (brand, category and scenario queries) | Manual | B |
| 92 | Test regularly in the models you care about | Manual | B |
| 93 | Record whether you are mentioned, whether you are cited and whether the description is correct | Spreadsheet | B |
| 94 | Record the test date, model name and whether browsing was on | Spreadsheet | B |
| 95 | Keep the question set stable; mark new questions separately | Spreadsheet | C |
| 96 | Test once before and once after each change | Spreadsheet | B |
| 97 | Check impressions, clicks and indexing problems in Search Console every week | Dashboard | B |
| 98 | Use logs or Cloudflare to watch visits from each kind of AI crawler | Logs or dashboard | B |
| 99 | Watch referral visits from chatgpt.com, perplexity.ai and similar sources | Analytics tool | B |
| 100 | Treat "cited but described wrongly" as a content problem and fix it | Manual | B |

## Sources and disclaimer

- Google Search Central: AI features and your website; Search Essentials (including spam policies)
- Ahrefs: llms.txt study of 137K sites (June 15, 2026)

Author: Peter Landa. This list reflects public sources and our own checking practice. It makes no promise about any search engine's or AI model's recommendations. For legal and compliance matters, rely on current regulations and professional advice.

Content in this repository is released under the MIT License; please keep the copyright notice when you reuse it.
