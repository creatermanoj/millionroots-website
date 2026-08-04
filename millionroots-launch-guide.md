# millionroots.in — Full Website Launch Guide
### #MissionMillion | Step-by-step for non-technical founders

> **Deadline: July 30, 2026** — Father's retirement day. Every step below moves you closer to that moment.

---

## Overview — What We're Doing

| Step | What | Time Needed |
|------|------|-------------|
| 1 | Prepare your files | 10 minutes |
| 2 | Upload to GitHub | 15 minutes |
| 3 | Deploy on Vercel | 10 minutes |
| 4 | Connect millionroots.in domain | 15 min setup + 24–48 hrs DNS |
| 5 | Connect Formspree (email sign-ups) | 15 minutes |
| 6 | Pre-launch checklist | 30 minutes |

**Total hands-on time: ~90 minutes** (then wait 24–48 hrs for domain to go live)

---

## PHASE 1 — Prepare Your Files (10 minutes)

### What your folder must look like

Your website folder should have this structure:

```
millionroots-website/
├── index.html        ← MUST be named exactly this
├── style.css         (if separate)
├── script.js         (if separate)
├── images/
│   └── (all your photos/logos here)
└── (any other files)
```

### Steps
1. Find the folder on your computer where your website files are saved
2. Make sure your main page is named **`index.html`** (not `home.html` or anything else — Vercel requires this)
3. Make sure all images are inside the folder (not linked from your desktop or another location)
4. That's it — no zipping, no special formatting needed

> ⚠️ **If your CSS or JS is inside the HTML file (all-in-one), that's perfectly fine — no changes needed.**

---

## PHASE 2 — Upload to GitHub (15 minutes)

GitHub is where your code lives online. Vercel reads from GitHub to deploy your site. Think of GitHub as a "cloud folder" for your website files.

### Step 1: Go to GitHub
- Open your browser and go to **github.com**
- Sign in to your account

### Step 2: Create a new repository (folder)
1. Click the **green "New"** button (top-left, or the "+" icon top-right → New repository)
2. Fill in:
   - **Repository name:** `millionroots-website`
   - **Description:** Million Roots Foundation — #MissionMillion
   - **Visibility:** Choose **Public** (required for Vercel free tier) or **Private** (works with Vercel free tier too)
3. ✅ Check **"Add a README file"**
4. Click **"Create repository"**

### Step 3: Upload your files
1. Inside your new repository, click **"uploading an existing file"** (small link in the middle of the page) OR click **"Add file" → "Upload files"**
2. **Drag and drop your entire website folder contents** into the upload area
   - Upload `index.html`, `style.css`, `script.js`, and the `images/` folder all at once
   - Do NOT drag the outer folder itself — drag the files/folders *inside* it
3. Scroll down to "Commit changes"
4. Leave the message as-is or type: `Initial website upload`
5. Click **"Commit changes"** (green button)

✅ Your files are now on GitHub. You'll see them listed in the repository.

---

## PHASE 3 — Deploy on Vercel (10 minutes)

Vercel reads your GitHub files and turns them into a live website — automatically.

### Step 1: Sign up / Sign in to Vercel
1. Go to **vercel.com**
2. Click **"Sign Up"** (or Log In)
3. Choose **"Continue with GitHub"** — this links Vercel to your GitHub account directly
4. Authorize when prompted

### Step 2: Import your project
1. After logging in, click **"Add New…" → "Project"**
2. You'll see a list of your GitHub repositories
3. Find **`millionroots-website`** and click **"Import"**

### Step 3: Configure (almost nothing to do)
Vercel will auto-detect your project. For a plain HTML site:
- **Framework Preset:** Leave as "Other" or "No Framework"
- **Root Directory:** Leave as-is (`.`)
- **Build Command:** Leave empty
- **Output Directory:** Leave empty

4. Click **"Deploy"** (blue button)

### Step 4: Watch it go live
- Vercel will show a build progress screen
- In about 30–60 seconds, you'll see **"Congratulations! 🎉"**
- You'll get a temporary URL like: `millionroots-website.vercel.app`
- Click it — your website is live on the internet!

> 💡 Every time you update files on GitHub (drag-and-drop new files), Vercel automatically re-deploys your site within seconds. No manual steps needed.

---

## PHASE 4 — Connect millionroots.in Domain (15 min + 24–48 hrs DNS)

### Step 1: Add domain in Vercel
1. In Vercel, go to your project dashboard
2. Click **"Settings"** (top menu)
3. Click **"Domains"** (left sidebar)
4. In the text box, type: `millionroots.in`
5. Click **"Add"**
6. Also add: `www.millionroots.in` (do this separately)
7. Vercel will show you **DNS records** — keep this page open, you'll need it in the next step

### Step 2: Find your domain registrar
Your domain was purchased somewhere — common registrars:
- GoDaddy (godaddy.com)
- Namecheap (namecheap.com)
- BigRock (bigrock.in) — common in India
- Google Domains / Squarespace Domains
- GoDaddy India (in.godaddy.com)

> If you're not sure where you bought it, check your email for a confirmation from when you purchased `millionroots.in`.

### Step 3: Update DNS settings at your registrar
1. Log in to your domain registrar
2. Find **"DNS Management"** or **"Manage DNS"** or **"DNS Zone"**
3. You need to add the records Vercel gave you. It will look like one of these options:

**Option A — Vercel gives you an A record:**
| Type | Name | Value |
|------|------|-------|
| A | @ | 76.76.21.21 |
| CNAME | www | cname.vercel-dns.com |

**Option B — Vercel gives you a CNAME:**
| Type | Name | Value |
|------|------|-------|
| CNAME | @ | cname.vercel-dns.com |
| CNAME | www | cname.vercel-dns.com |

> ⚠️ **Use whatever Vercel shows you exactly — copy the values from Vercel, don't type from memory.**

4. Delete any existing **A records** or **CNAME records** for `@` and `www` that might already be there (old ones pointing to a parking page)
5. Save/confirm the changes

### Step 4: Wait for DNS propagation
- DNS changes take **24–48 hours** to spread worldwide (sometimes faster — 1–2 hours)
- You can check progress at: **dnschecker.org** → type `millionroots.in` → click "Search"
- Once it shows green checkmarks, your site is live at millionroots.in ✅

> 💡 While waiting, your site is already live at the `vercel.app` URL — share that link with close family/friends in the meantime.

---

## PHASE 5 — Connect Formspree (Email Sign-ups) (15 minutes)

Formspree captures the names and emails from your "Early Supporter" sign-up form and sends them to your inbox.

### Step 1: Create a Formspree account
1. Go to **formspree.io**
2. Click **"Get Started Free"**
3. Sign up with your email: drmanoj2k8@gmail.com
4. Verify your email

### Step 2: Create a form
1. Click **"+ New Form"**
2. Name it: `Million Roots Early Supporters`
3. Formspree gives you a **unique endpoint URL** that looks like:
   `https://formspree.io/f/xyzabcde`
4. Copy this URL

### Step 3: Update your HTML
Open your `index.html` file. Find your sign-up form — it will look something like:

```html
<form action="YOUR_FORM_URL" method="POST">
```

Replace `YOUR_FORM_URL` with your Formspree endpoint:

```html
<form action="https://formspree.io/f/xyzabcde" method="POST">
```

Make sure your form has these fields (add if missing):
```html
<input type="text" name="name" placeholder="Your Name" required>
<input type="email" name="email" placeholder="Your Email" required>
<button type="submit">Join the Movement</button>
```

### Step 4: Re-upload to GitHub
1. Go back to your GitHub repository
2. Click on `index.html`
3. Click the **pencil (edit) icon** ✏️
4. Make the change directly in GitHub's editor
5. Scroll down → click **"Commit changes"**
6. Vercel will automatically redeploy in ~30 seconds

### Step 5: Test it
1. Go to your live site
2. Fill in the form with your own name and email
3. Click submit — you should get a **"Thank you"** message
4. Check your inbox at drmanoj2k8@gmail.com for the submission

---

## PHASE 6 — Pre-Launch Checklist ✅

Before you announce to the world on July 30, go through this list:

### Content
- [ ] Father's photo added to the story section
- [ ] All placeholder text replaced with real content
- [ ] Tree counter numbers are correct (start at 0 or actual planted count)
- [ ] millionroots.in contact email is working
- [ ] Social media links in footer point to real accounts (or hidden if not ready)

### Technical
- [ ] Site loads correctly on **mobile phone** (open on your phone and test)
- [ ] Site loads correctly on **tablet**
- [ ] Sign-up form submits successfully and you receive the email
- [ ] All images are loading (no broken image icons)
- [ ] Site loads fast — under 3 seconds (test at **pagespeed.web.dev**)

### Domain
- [ ] millionroots.in opens your website (not a parking page)
- [ ] www.millionroots.in also works
- [ ] SSL certificate is active (you should see a 🔒 padlock in browser — Vercel does this automatically)

### Legal (important for NGO)
- [ ] "Section 8 Company Registration in Progress" disclaimer visible (until incorporation is complete)
- [ ] No donation button live until Razorpay is set up AND company is registered
- [ ] Privacy policy added (basic one is fine — Formspree collects email addresses)

---

## WHAT COMES NEXT (After Launch)

| Feature | When to Build | Dependency |
|---------|--------------|------------|
| Razorpay donation page | After Section 8 incorporation | Need company registration docs |
| Father's full story / About page | Anytime | None |
| Blog | After launch | None |
| Sapling/product sales page | Year 2 | After farm is operational |
| Social media launch kit | 2 weeks before July 30 | None |

---

## QUICK REFERENCE — Key Links

| Service | URL | Purpose |
|---------|-----|---------|
| GitHub | github.com | Store your website files |
| Vercel | vercel.com | Host and deploy your website |
| Formspree | formspree.io | Email capture from sign-up form |
| DNS Checker | dnschecker.org | Check if domain is live |
| PageSpeed | pagespeed.web.dev | Test site loading speed |
| Razorpay | razorpay.com | Donations (post-incorporation) |

---

## STUCK? HERE'S WHAT TO DO

| Problem | Solution |
|---------|----------|
| Files not uploading to GitHub | Try uploading 10 files at a time — GitHub has a file limit per upload batch |
| Vercel says "Build Failed" | Share the error message with me — I'll fix it |
| Domain not connecting | Double-check the DNS records match exactly what Vercel shows |
| Form not receiving emails | Check spam folder; verify the Formspree endpoint URL is correct |
| Site looks broken on mobile | Share a screenshot with me — I'll fix the CSS |

---

*Prepared by Claude for Dr. Manoj — Million Roots Foundation*
*Every tree planted is a promise kept. 🌱*
