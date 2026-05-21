---
layout: default
permalink: /privacy
title: PageLens Privacy
---

# PageLens, Privacy Policy

**Effective date:** 2026-05-20
**Last updated:** 2026-05-20

This Privacy Policy describes how PageLens ("PageLens," "we," "us," "our") collects, uses, and discloses information when you install and use the PageLens Shopify app (the "App").

**Plain-English summary.** We are a performance-audit tool. We look at what's loading on your storefront and at the files in your theme. We do not look at your customers, their orders, or anything about who is shopping at your store. We never sell your data. The only people who see your data are you (in the App's dashboard) and Shopify (because the App runs on top of their platform).

---

## 1. Who we are

PageLens is operated by **Keenan V.**, a sole proprietor based in **Ohio, USA**.

For privacy questions or data-access requests, contact **keebob02@gmail.com**.

## 2. What we collect

When you install PageLens, we collect and store the following on Shopify's infrastructure and our own servers (Fly.io / Railway, US-based):

### From Shopify (with your authorization)
- **Shop identifier**, your `*.myshopify.com` domain
- **OAuth access token**, used to make Shopify API calls on your behalf, encrypted at rest
- **Theme file names and contents**, read via the `read_themes` scope, used to detect leftover files from uninstalled apps and to audit image-loading patterns. We never write to your theme.
- **Subscription plan handle**, the PageLens pricing tier you selected

### From scanning your storefront
- **Network resource list**, URLs, sizes, content types, and load timings of every script/stylesheet your public storefront homepage loads. Captured by a headless browser (Playwright) acting as a regular shopper visiting your homepage URL.
- **Attribution metadata**, for each resource, which third-party app (if any) it appears to belong to, based on our curated app-domain database.

### From third parties
- **Google PageSpeed Insights scores**, we ask Google to grade your storefront's performance using the public PageSpeed Insights API. This returns scores, metrics, and audit details. We store the raw response for display in our dashboard.

### What we explicitly do NOT collect
- Any data about **your customers** (names, emails, addresses, orders, IPs, browsing history, payment information, cart contents)
- The contents of **product, order, or customer database tables**
- Any **personally identifiable information** belonging to shoppers
- Anything **outside the public storefront homepage** for v1 scans

We deliberately request the minimum Shopify scope needed to do our job (`read_themes` only; nothing customer-facing, no write access).

## 3. How we use the information

- To run scans you requested and display results in the App
- To detect leftover theme files from uninstalled apps ("ghost code")
- To compute PageSpeed scores and identify performance regressions
- To process billing (via Shopify's billing platform, we never see your payment info)
- To send service-related communications via your Shopify admin (in-app notifications only; no marketing email in v1)
- To investigate and troubleshoot bugs you report

## 4. How we share information

We do **not** sell your data, ever.

We share data only with:
- **Shopify**, the platform our App runs on, which is necessary for authentication, billing, and API access
- **Google** (PageSpeed Insights API), we send your storefront URL so Google can grade it; we don't send any other data
- **Our infrastructure provider** (Fly.io or Railway, US-based), our servers run on their infrastructure
- **Law enforcement, if legally compelled**, and only after exhausting legal options to limit disclosure

## 5. Data retention

- **Active install:** we keep scan history while you have the App installed. This is what powers the dashboard's "last scan" view.
- **App uninstalled:** Shopify sends us an `app/uninstalled` webhook. We immediately delete your session and active subscription record.
- **48 hours after uninstall:** Shopify sends us a `shop/redact` webhook. We permanently delete all of your scan data, ghost findings, image findings, and any other stored records associated with your shop.
- This 48-hour window is mandated by Shopify's data-handling contract for App Store apps.

## 6. Customer data requests (GDPR / CCPA)

Because PageLens doesn't collect customer-level data, customer data-access requests will always return **no records**. We respond to Shopify's mandatory `customers/data_request` and `customers/redact` webhooks by acknowledging the request, there is nothing to export or delete.

## 7. Security

- Access tokens are stored encrypted at rest in our database
- All traffic between your shop, our servers, Shopify, and Google is encrypted in transit (HTTPS / TLS 1.2+)
- We never log access tokens or other secrets to plaintext log files
- Our infrastructure is hosted on SOC 2-certified providers (Fly.io / Railway)

## 8. Your rights

You have the right to:
- Know what data we hold about your shop (just ask: **keebob02@gmail.com**)
- Delete all data we hold (uninstall the App; we will fully wipe within 48 hours)
- Export your data (we'll provide a JSON dump on request)
- Lodge a complaint with your local data-protection authority

## 9. Children

PageLens is a business tool for merchants. It is not directed at children and we do not knowingly collect data from children.

## 10. Changes to this policy

We may update this policy. Material changes will be announced in-app and via a notification to the email Shopify has on file for your shop. The "Last updated" date at the top of this document will always reflect the current version.

## 11. Contact

Privacy questions, requests, complaints: **keebob02@gmail.com**.
General support: **keebob02@gmail.com**.
