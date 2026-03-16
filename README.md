# Dylan Akosah — Personal Website

Personal website built as a static site, hosted on GitHub Pages.

## Pages

| File | Description |
|------|-------------|
| `index.html` | Homepage with animated starfield and news |
| `about.html` | About page |
| `research.html` | Research & publications |
| `contact.html` | Contact page |

## Publishing to GitHub Pages

### Step 1 — Create a GitHub repository
1. Go to [github.com](https://github.com) and sign in
2. Click **+** → **New repository**
3. Name it `yourusername.github.io` (replace with your actual GitHub username)
4. Set it to **Public**
5. Click **Create repository**

### Step 2 — Upload your files
1. Click **uploading an existing file** on the repo page
2. Drag and drop these files **only**:
   - `index.html`
   - `about.html`
   - `research.html`
   - `contact.html`
   - `.gitignore`
   - `README.md`
3. ⚠️ **DO NOT upload** `admin.html` or `admin-supabase.html`
4. Click **Commit changes**

### Step 3 — Enable GitHub Pages
1. Go to your repo → **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Select branch: **main**, folder: **/ (root)**
4. Click **Save**
5. Your site will be live at `https://yourusername.github.io` within a few minutes

## Admin Console (Local Only)

The admin console (`admin.html`) runs **locally on your computer only** and is excluded from GitHub via `.gitignore`.

**Security:** The admin password is hashed using **PBKDF2 with 310,000 iterations and a random salt** — the same standard used by major password managers. Even if someone obtained the file, cracking the password would take years on modern hardware.

To use the admin:
1. Open `admin.html` directly in your browser (no server needed)
2. Make your changes (news, research, about)
3. Click **Export Homepage HTML** to download the updated `index.html`
4. Upload the new `index.html` to GitHub to publish your changes

## Tech Stack
- Pure HTML, CSS, JavaScript — no frameworks
- NASA public domain imagery
- Eurostile font (embedded)
- localStorage for admin data sync
