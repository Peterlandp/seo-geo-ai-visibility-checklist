English | [简体中文](README.zh-CN.md)

# Website SEO / GEO / AI Visibility Checklist

This checklist tests whether a website can be crawled, understood and cited by search engines and AI assistants. GEO here means Generative Engine Optimization. It has nothing to do with geography or remote sensing.

Passing this checklist means your site is eligible to be cited by AI tools. It does not mean they will recommend you.

Last updated: 2026-11-07

## The short version

- The foundation is still the classic basics: a site that can be accessed, understood, trusted and verified.
- Google's documentation says there are no additional requirements to appear in AI Overviews and AI Mode, and no need for AI-specific text files or special markup. A page needs to be indexed and eligible to show with a snippet.
- Public data does not currently support the claim that llms.txt brings citations. See "Common myths" below.

## Which advice has evidence

| Grade | Meaning | Example |
|---|---|---|
| A | Stated by a protocol, standard, official documentation or law | robots.txt rules, sitemap specification |
| B | Public search-engine guidance or industry consensus; effect on AI answers not quantified | Clear navigation, consistent facts, complete content |
| C | Experience or hypothesis with no public evidence yet | Particular phrasing patterns, Q&A formats |
| X | Data currently shows no effect | llms.txt |

## The full list: 100 checks

The full list is in [CHECKLIST.md](CHECKLIST.md). It has 100 checks, each with a way to verify it and an evidence grade (A, B or C), in 11 parts:

| Part | Checks |
|---|---|
| 1. Crawling and indexing | 10 |
| 2. Technical basics and speed | 8 |
| 3. Page structure | 9 |
| 4. Titles, descriptions and links | 9 |
| 5. Structured data | 9 |
| 6. AI crawlers and access policy | 8 |
| 7. Entity and trust signals | 10 |
| 8. Citable content | 10 |
| 9. Multiple languages and overseas compliance | 10 |
| 10. China site (for mainland China visitors) | 7 |
| 11. Measuring and re-testing | 10 |

Below are the 20 core checks.

## 20 core checks

### Can it be accessed?

- [ ] Important pages open normally, with no large numbers of dead links
- [ ] robots.txt does not block core pages (a missing file is not an error; a server error should be fixed)
- [ ] A sitemap exists and lists only pages that load normally
- [ ] No page carries an unintended noindex
- [ ] Your firewall or CDN does not return 403 to search and AI crawlers across the board
- [ ] The certificate is valid, the site runs on HTTPS, and http redirects once to https

### Can it be understood?

- [ ] Core text is in the raw HTML, not produced only by scripts
- [ ] Each page has a unique title and a clear main heading; descriptions are full sentences, not keyword lists
- [ ] Navigation lets people and crawlers find every core offering, and menu names are self-explanatory
- [ ] Service pages say what it is, who it is for, how it works, what it costs and what the limits are
- [ ] The first screen contains one sentence that can be quoted as a definition

### Can it be trusted?

- [ ] Company name and contact details are clear in the footer and on an About page, and written the same way everywhere
- [ ] Key numbers state source, date and basis; case studies state their scope and do not exaggerate
- [ ] A privacy policy and terms exist and are linked next to every form that collects information
- [ ] Articles show an author and publish and update dates
- [ ] No unsupported absolute claims; promises state their conditions, exceptions and remedies

### Can it be verified?

- [ ] The same facts (name, price, scope of service) match across pages and languages
- [ ] Independent official profiles back you up, such as company registries, official accounts and industry directories
- [ ] You test regularly with a fixed set of questions in the models you care about, and record whether your brand is mentioned and described correctly
- [ ] You re-test after every change instead of trusting a feeling

## Extra checks for overseas sites

- [ ] Each language has its own URL; language versions point to each other with hreflang, and prices and terms match across versions
- [ ] A privacy policy and terms of service exist. For EEA and UK visitors, cookie consent can be declined, no non-essential scripts load before consent, and full page content remains after declining
- [ ] Company information on LinkedIn, Crunchbase, Product Hunt and similar platforms matches the website
- [ ] If your brand name is generic, use a fixed "brand + category" form so it is not drowned out by products with the same name
- [ ] Use IndexNow so Bing-based search learns about updates faster

## If you also sell in China

- [ ] Show your ICP filing number in the footer and link it to the official lookup page; the filing entity should match the site's operator (check whether this applies to you)
- [ ] Avoid the extreme wording that Chinese advertising law restricts, and cite data with source and validity period
- [ ] Check access speed from several mainland networks, and avoid third-party resources that are unreachable there

## Common myths

- "An llms.txt file gets me cited." Ahrefs' analysis of 137,210 domains (published June 2026) found about 38,000 with a valid llms.txt, and 97% of those files received no requests in May 2026. AI retrieval bots made up about 1.1% of requests. Public data does not support the claim.
- "FAQ markup improves recommendations." The value is in having clear questions and answers on the page, not in the markup.
- "More keywords is better." Modern retrieval looks at meaning and facts; stuffing only hurts readability.

## Example: checking our own two sites with this list

The author runs two websites: sharehub.fun for overseas readers and ynwone.com for mainland China. Every page goes through a set of automatic checks before it is published. Here is how that maps to this checklist:

| Area | sharehub.fun (overseas) | ynwone.com (China) |
|---|---|---|
| robots.txt and sitemap | Both present; the pre-release check makes sure the sitemap matches the pages one to one | Both present, same check |
| AI crawler policy | robots.txt allows all crawlers and lists each AI crawler and social preview crawler (all Allow); after publishing, the live file is compared byte for byte with the local one so a platform cannot rewrite it | robots.txt lists the AI crawlers |
| Languages | Chinese, English, Spanish and French, each with its own URL and linked with hreflang | Chinese only |
| IndexNow | Set up | Not applicable |
| Filing and compliance | Privacy policy and terms of service | ICP filing completed |
| llms.txt | Present and lists every page; treated as grade X, so we do not expect citations from it | Same |

This only shows that both sites are eligible to be cited. It does not mean AI tools already recommend them. Both sites are new, and we run this list on ourselves to learn which practices really help.

## How to use it

Go through the list yourself, then hand uncertain items to a tool or a specialist. A machine can tell whether something exists. A person has to confirm that qualifications, case studies and legal compliance are genuine.

The full explanation, in article form:

- English: https://www.sharehub.fun/guides/geo-site-checklist/
- 中文: https://www.sharehub.fun/zh/guides/geo-site-checklist/

## Sources

- Google Search Central, AI features and your website: https://developers.google.com/search/docs/appearance/ai-features
- Ahrefs, We Analyzed 137K Sites: 97% of llms.txt Files Never Get Read (June 2026): https://ahrefs.com/blog/llmstxt-study/

## Author and disclaimer

Author: Peter Landa (兰大鹏), founder of EagleX and ShareHub. 15 years in data and marketing: B2B product sales of over EUR 100 million in total; a consumer campaign that reached 23 million users in one year, 250,000 of them paying; over EUR 15 million of advertising placed for clients in China, the US, Korea and Europe (LinkedIn: https://www.linkedin.com/in/peter-landa ).

Operated by Chengdu Yigekesi Data Co., Ltd. (EagleX). ShareHub (sharehub.fun) is the overseas version of the 野牛王 (ynwone.com) brand.

This list reflects public sources and our own checking practice. It makes no promise about any search engine's or AI model's recommendations. For legal and compliance matters, rely on current regulations and professional advice.

Content in this repository is released under the MIT License; please keep the copyright notice when you reuse it.
