# Which IP for a TikTok Shop seller account in the US or UK? One static ISP IP per shop (2026)

**Run each TikTok Shop's Seller Center through one static ISP IP in the country the shop is registered in and you live in (a US IP for a US shop, a UK IP for a UK shop), keep that IP for the life of the shop, and use it in one browser profile that serves only that shop.** Team members get their own Seller Center roles instead of the owner's password. Work that needs no sign-in, like viewing a product page the way a shopper would, belongs on rotating residential traffic. Proxy302 maintains this repository and sells these proxies. A static residential (ISP) IP is $7.99 per 30 days or $0.50 per day, with one price for the US, the UK and all other countries. Static IPs of 30 days or longer are dedicated to the buyer. Who may open a shop and in which country is decided by TikTok from your documents; TikTok's registration help says you must live in the country you choose for your shop, and an IP changes none of that.

> Proxy302 maintains this repository and sells the IPs described here; we are a vendor, not a neutral reviewer. 中文：[README.zh-CN.md](README.zh-CN.md)

## Contents

1. [TikTok's rules come first](#1-tiktoks-rules-come-first)
2. [What a fixed IP does for a shop](#2-what-a-fixed-ip-does-for-a-shop)
3. [Which proxy for which job](#3-which-proxy-for-which-job)
4. [Setup for one shop](#4-setup-for-one-shop)
5. [Team access without sharing the password](#5-team-access-without-sharing-the-password)
6. [Mistakes and fixes](#6-mistakes-and-fixes)
7. [FAQ](#7-faq)
8. [Related](#8-related)

## 1. TikTok's rules come first

Read TikTok's own pages before buying anything:

- [Requirements to register as a seller on TikTok Shop](https://ads.tiktok.com/help/article/requirements-to-register-as-a-seller-on-tiktok-shop): among other points, you must live in the country you choose for your shop, and the phone number or email used to register cannot already belong to another TikTok Shop.
- The seller registration pages for the US and the UK list the business documents, identity checks and bank details each market asks for. They change; check them on the day you apply.

The order matters: first be eligible for a US or UK shop, then pick an IP in that same country. An IP is not a way to qualify for a market, and it does not replace any verification. If TikTok asks you to verify, complete it honestly with your own documents.

## 2. What a fixed IP does for a shop

Plenty of shops run fine on the owner's normal internet. Paying for a fixed IP makes sense when:

- **Your home broadband changes address** every few days, so Seller Center sees a new network again and again.
- **You work from a shared space** (co-working, a shared office) whose exit address many unrelated people use.
- **Several people in the same country handle the shop** from different places: an office, home, a laptop on the road. Through one profile and one IP the shop has one address.
- **You run more than one business, each with its own shop.** Each shop gets its own IP and profile, so their connections never mix.

It keeps a legitimate shop's connection consistent. It does not lift restrictions, fix policy problems or make extra shops acceptable.

## 3. Which proxy for which job

| Job | Proxy | Proxy302 price |
|---|---|---|
| Daily Seller Center work, signed in | One static ISP IP in the shop's country | $7.99 per 30 days |
| Trying the setup first | Static ISP IP for 1 day | $0.50 |
| A shop you plan to keep for months | Static ISP IP, 60 or 90 days | $15.98 for 60 days, $23.97 for 90 days |
| Looking at product pages and search results as a signed-out US or UK visitor | Rotating residential | $1.50/GB pay as you go; prepaid traffic never expires |
| Signing in through a rotating IP | Do not | |

Black Friday, 24 Nov to 4 Dec 2026 (UTC+8): static ISP IPs cost $14.00 for 60 days and $18.00 for 90 days (1 to 30 days unchanged), and rotating residential 100, 300 and 500 GB packs come with 25% extra traffic.<!-- bf2026 -->

Static ISP IPs are sold as HTTP or SOCKS5, chosen at purchase; one IP has one protocol. For Chrome and other Chromium browsers choose HTTP, because they cannot log in to a SOCKS5 proxy with a username and password. All prices: [proxy302.com/pricing](https://proxy302.com/pricing/).

## 4. Setup for one shop

1. **Buy one static ISP IP** in the shop's country (US or UK).
2. **Check the exit from a terminal**, replacing the USER, PASS, HOST and PORT placeholders:

   ```bash
   curl -sS -x "http://USER:PASS@HOST:PORT" https://ipinfo.io/json
   ```

   Expect `country` `US` or `GB` as ordered, and an internet operator in `org`, not a hosting company.
3. **Make a browser profile for the shop**: a separate Chrome profile with a proxy extension, or one profile in an antidetect browser. Enter host, port, username and password, then open `https://ipinfo.io/json` inside the profile and compare.
4. **Open Seller Center only from that profile.** Bookmark it there and nowhere else.
5. **Keep the IP.** Turn on auto-renew for it, or note the end date. Renewing keeps the same IP. Once a term runs out, that address is gone for good and the next purchase arrives with another one.

The TikTok app on the owner's own phone, in the shop's country, is ordinary use and does not need the proxy. The thing to avoid is several shops on one phone, one profile or one IP.

## 5. Team access without sharing the password

TikTok's help page [Roles and permissions in Seller Center](https://ads.tiktok.com/help/article/roles-and-permissions-in-seller-center) describes eight roles, including Customer Service Agent, Order Fulfillment Specialist, Product Management Specialist, Finance Specialist and Advertising Manager, and says user management is visible only to the shop owner's account. So:

- The owner adds each person with the role that matches their work.
- Everyone works in the shop's profile, signed in as themselves.
- The owner keeps the main login, its phone number and its email.
- When someone leaves, the owner removes their user. The IP stays.

## 6. Mistakes and fixes

| Symptom | Cause | Fix |
|---|---|---|
| Repeated new-login prompts | Someone opens Seller Center outside the shop's profile | One profile, one entry point |
| The profile cannot connect after a month | The IP's term ended | Renew earlier, or turn on auto-renew |
| 407 Proxy Authentication Required | Username or password typed wrong | Copy them again from the console |
| Chrome extension fails with a SOCKS5 IP | Chromium cannot log in to SOCKS5 | Buy the IP as HTTP |
| `ipinfo` shows a hosting company | A datacenter IP was used | Use a static ISP IP |
| Two shops share an address | A profile was copied with its proxy | One IP per shop; check each profile |

## 7. FAQ

**I have a US shop and a UK shop. One IP or two?**
Two, each in its own country and profile, and only if TikTok accepted you for both markets under its rules.

**Should the IP be in the same city as me?**
The country is what matters. If the order page lets you pick a city, one near you is a sensible choice; after that, stay with it.

**Can I use the same IP for my TikTok Shop and my Amazon account?**
If both belong to the same business and the same people run them, yes. Many sellers still keep one profile per platform, which makes mistakes easier to spot.

**My shop was asked for verification. Will a better IP help?**
No. Submit genuine documents. No IP stands in for verification.

**Is there a free trial?**
No. To try the whole setup on a real shop day, rent one static ISP IP for 24 hours for $0.50.

## 8. Related

- [How do I set up a static residential IP for TikTok?](https://github.com/proxy302/proxy-guides/blob/main/static-residential-ip-for-tiktok/README.md)
- [What is a TikTok native IP?](https://github.com/proxy302/proxy-guides/blob/main/tiktok-native-ip/README.md) (Chinese)
- [Rotating vs sticky residential sessions](https://github.com/proxy302/proxy-guides/blob/main/rotating-vs-sticky-sessions/README.md)
- [proxy-ip-check](https://github.com/proxy302/proxy-ip-check): exit IP, country, network owner and timezone in one command

*Facts checked 23 November 2026.*
