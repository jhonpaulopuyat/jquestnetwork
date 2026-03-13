# JQuest Network Website

Ultra High Speed Internet provider website — built as a static multi-page site for GitHub Pages with GoDaddy domain.

---

## 📁 File Structure

```
jquest/
├── index.html        ← Home page
├── plans.html        ← Plans & Pricing
├── about.html        ← About Us
├── contact.html      ← Contact
├── css/
│   └── style.css     ← All styles
├── js/
│   └── main.js       ← Navigation, animations
└── images/           ← Put your images here
    └── (your images go here)
```

---

## 🖼️ Adding Your Logo & Images

1. Put your logo image in the `images/` folder (e.g. `images/logo.png`)
2. In each HTML file, find this placeholder div:
   ```html
   <div style="width:42px;height:42px;background:linear-gradient...">JQ</div>
   ```
   Replace it with:
   ```html
   <img src="images/logo.png" alt="JQuest Network" style="height:42px;width:auto;" />
   ```
3. On `about.html`, find the placeholder:
   ```html
   <div class="about-img-placeholder">...</div>
   ```
   Replace with:
   ```html
   <img src="images/your-team-photo.jpg" alt="JQuest Team" />
   ```

---

## 🚀 How to Deploy on GitHub Pages

### Step 1 — Create GitHub Repo
1. Go to [github.com](https://github.com) → New repository
2. Name it exactly: `yourusername.github.io` (for root domain)  
   OR any name like `jquest-website` (for subdomain)
3. Set it to **Public**
4. Upload all these files to the repo

### Step 2 — Enable GitHub Pages
1. Go to your repo → **Settings** → **Pages**
2. Under "Source", select **Deploy from a branch**
3. Branch: `main`, Folder: `/ (root)`
4. Click **Save**
5. Your site will be live at `https://yourusername.github.io` (or the repo subdomain)

### Step 3 — Add Your GoDaddy Domain

#### In GitHub:
1. Repo → Settings → Pages → **Custom domain**
2. Enter your domain (e.g. `www.jquestnetwork.com`)
3. Check **Enforce HTTPS**
4. GitHub will create a `CNAME` file automatically

#### In GoDaddy DNS:
1. Log into GoDaddy → DNS Management for your domain
2. Add these **A records** (for apex/root domain):
   ```
   Type: A   Host: @   Value: 185.199.108.153
   Type: A   Host: @   Value: 185.199.109.153
   Type: A   Host: @   Value: 185.199.110.153
   Type: A   Host: @   Value: 185.199.111.153
   ```
3. Add a **CNAME** record (for www):
   ```
   Type: CNAME   Host: www   Value: yourusername.github.io
   ```
4. DNS changes take 10 minutes to 48 hours to propagate

---

## ✏️ Customization Tips

- **Coverage areas** — Edit the `<span class="area-tag">` list in `plans.html`, `about.html`, and `contact.html`
- **Business hours** — Edit in `contact.html`
- **Facebook URL** — Search for `facebook.com/JQuestNetwork` and update if your page URL is different
- **Map** — The Google Maps embed in `contact.html` shows Arayat, Pampanga. To get a more precise embed for your exact address, go to Google Maps → search your address → Share → Embed a map → copy the iframe src

---

## 🎨 Colors (for reference)

| Variable      | Value     | Use               |
|---------------|-----------|-------------------|
| `--navy`      | `#05102a` | Main background   |
| `--red`       | `#e8192c` | Accent / CTA      |
| `--cyan`      | `#00d4ff` | Highlight / links |
| `--white`     | `#ffffff` | Text              |

---

Built for JQuest Network and Data Solution · Arayat, Pampanga 🇵🇭
