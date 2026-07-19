# Glasscott Integrative Therapy website

A static, mobile-friendly website for Glasscott Integrative Therapy. It is designed for free hosting on GitHub Pages and uses only HTML, CSS, and a small amount of JavaScript.

## Included pages

- `index.html` — home page
- `about.html` — professional bio, credentials, specialties, and approach
- `contact.html` — Headway booking link, secure phone, email, privacy warning, and crisis information
- `privacy.html` — basic website privacy information
- `404.html` — custom not-found page
- `styles.css` — all visual styling
- `script.js` — mobile menu and current-year footer
- `CNAME` — custom domain setting
- `sitemap.xml` and `robots.txt` — search engine support

## Important privacy decision

This website intentionally does **not** contain a contact form. GitHub Pages is static hosting and does not securely process or store patient messages. The contact page directs visitors to Headway, phone, or email and warns them not to send protected health information through ordinary email.

## Optional: add Erin's headshot

The site currently uses an `EG` monogram so it works immediately without a missing image. To add a photograph:

1. Create a folder named `images`.
2. Add a web-optimized photo named `erin-headshot.jpg`.
3. In `index.html` and `about.html`, replace this block:

```html
<div class="portrait-placeholder" aria-label="Decorative portrait placeholder">
  <div class="portrait-monogram" aria-hidden="true">EG</div>
</div>
```

with:

```html
<img class="portrait-placeholder" src="images/erin-headshot.jpg" alt="Erin Marie Glasscott, LCSW">
```

Use a photo Erin owns or has permission to publish. Do not hotlink the Psychology Today image.

## Publish with GitHub Pages

1. Sign in to GitHub.
2. Create a **public** repository named `YOUR-USERNAME.github.io`.
3. Upload every file in this folder to the root of the repository.
4. Open the repository's **Settings** tab.
5. Select **Pages** under **Code and automation**.
6. Under **Build and deployment**, choose **Deploy from a branch**.
7. Select branch **main** and folder **/(root)**, then select **Save**.
8. After deployment finishes, test `https://YOUR-USERNAME.github.io`.

## Connect glasscottintegrativetherapy.com

The `CNAME` file is already set to:

```text
glasscottintegrativetherapy.com
```

In GitHub:

1. Open **Settings → Pages**.
2. Enter `glasscottintegrativetherapy.com` under **Custom domain** and save.

At the domain's DNS provider, add these four `A` records for the root/apex domain:

| Host | Type | Value |
|---|---|---|
| `@` | A | `185.199.108.153` |
| `@` | A | `185.199.109.153` |
| `@` | A | `185.199.110.153` |
| `@` | A | `185.199.111.153` |

Add this record for `www`:

| Host | Type | Value |
|---|---|---|
| `www` | CNAME | `YOUR-USERNAME.github.io` |

Remove conflicting website `A`, `AAAA`, or `CNAME` records, but do not remove email-related `MX` records or Google Workspace verification records.

DNS changes may take up to 24 hours. After GitHub recognizes the domain, return to **Settings → Pages** and enable **Enforce HTTPS**.

## Future edits

Open a file in GitHub, select the pencil icon, make changes, then choose **Commit changes**. GitHub Pages republishes automatically after the commit reaches the selected publishing branch.
