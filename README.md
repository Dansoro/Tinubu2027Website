# Tinubu 2027 Website — Renewed Hope 2.0

Supporters' campaign website for President Bola Ahmed Tinubu's 2027 re-election.
Built with HTML & Tailwind CSS (compiled into the page, so no internet is needed for the design).
Not an official APC or government site.

Designed & developed by **Shamsuddeen Danlami Muhammad**.

---

## 1. What's in this folder

All files sit together in ONE folder (no sub-folders):

| File | What it is |
|---|---|
| `index.html` | The whole website (layout, text, slider, album) |
| `tinubu-portrait.jpg` | Main banner photo |
| `tinubu-field.jpg` | "Our Vision" photo |
| `cg-musa.jpg` | Security & Defence photo |
| `rally-01.jpg` … `rally-20.jpg` | Rally photos (slider + album) |
| `slide-1.jpg` … `slide-6.jpg` | Night-event photos (album) |
| `README.md` | This guide |

**Rule:** every photo must sit in the same folder as `index.html`, and names must match exactly (lowercase).

---

## 2. Upload to GitHub (first time)

1. Go to github.com → **New repository** → name it (e.g. `Tinubu2027Website`) → **Create**.
2. Click **uploading an existing file** (or **Add file → Upload files**).
3. Open the extracted folder on your computer, press **Ctrl + A** to select ALL files, and drag them into the GitHub page.
   - Drag the *files*, not the folder.
4. Wait until every file shows in the list, then click **Commit changes**.
5. Check: the repo main page should list `index.html` and all the `.jpg` files together.

## 3. Deploy on Vercel (first time)

1. Go to vercel.com → **Add New → Project**.
2. Find your GitHub repo → **Import**.
3. **Project Name:** lowercase only, e.g. `tinubu-2027-website`.
4. **Framework Preset:** `Other`. Leave Build Command and Output Directory **empty**.
5. Click **Deploy**. Your site: `https://tinubu-2027-website.vercel.app`

---

## 4. How to edit the website

Open `index.html` in VS Code (or Notepad). Use **Ctrl + F** to find the text you want to change.

| To change… | Search for… |
|---|---|
| Main headline | `Renewing` |
| Intro paragraph | `Join millions of Nigerians` |
| Election countdown date | `electionDate` → edit `2027-01-16T08:00:00+01:00` |
| Slider captions | `Renewed Hope, Renewed Mandate` (each slide has a small label + big title) |
| Agenda cards | `Eight Priorities` (each card has an `<h3>` title and a `<p>` text) |
| Security section text | `Experienced leadership` |
| Footer / developer credit | `Designed &amp; developed by` |
| Social media links | `Facebook` → replace `href="#"` with your page link |

**Replace a photo:** upload a new photo with the **exact same file name** (e.g. a new `cg-musa.jpg`). It replaces the old one automatically.

**Add a photo to the album:**
1. Upload the photo, e.g. `rally-21.jpg`.
2. In `index.html`, search for `album-item`, copy one whole `<button ...> ... </button>` block, paste it below, and change both `rally-XX.jpg` names to `rally-21.jpg`.

**Add a slide:** search for `<figure class="relative min-w-full`, copy one whole `<figure> ... </figure>` block, change the photo name and the caption. Dots and counter update by themselves.

> Tip: only change words between `>` and `<`. Don't delete the `class="..."` parts — they control the design.

---

## 5. Upload your edits

**GitHub:**
1. Open your repo → **Add file → Upload files**.
2. Drag in the changed file(s) (e.g. the edited `index.html` or a new photo). Same name = replaces the old one.
3. Click **Commit changes**.

**Vercel:** nothing to do — it redeploys automatically about 1 minute after every commit.
Then open your site and press **Ctrl + F5** to see the new version (clears the old cached page).

To edit directly on GitHub: open `index.html` in the repo → click the ✏️ pencil icon → edit → **Commit changes**.

---

## 7. "Join" sign-ups arrive in your email (no database)

The **Join Now** form is already connected. Every sign-up is emailed to **shamsdanlami2@gmail.com**
as a neat table (name, phone, email, state, LGA), using the free service FormSubmit.

**One-time activation (do this once, right after the site is live):**
1. Open your live site and fill the Join form yourself as a test.
2. Check your Gmail (also check **Spam/Promotions**) for an email from **FormSubmit** asking you to confirm.
3. Click **Activate Form**. Done — every sign-up from now on lands in your inbox.

**Tips**
- Create a Gmail label/filter for subject "New Volunteer" to keep them organised.
- After activation, FormSubmit emails you a private random code. You can replace your email in `index.html`
  (search `formsubmit.co/ajax/`) with that code to hide your email address from the page source.
- To change the receiving email: search `formsubmit.co/ajax/` in `index.html`, replace the email, upload, and activate again.

**Built-in protection:** Nigerian phone number check, required consent box, and a hidden spam trap for bots.

**Privacy:** you are collecting names and phone numbers. Keep these emails private, only share with people
who need them, and delete details when someone asks — in line with the Nigeria Data Protection Act 2023.

---

## 6. Troubleshooting

| Problem | Fix |
|---|---|
| Photos don't show | Make sure the photos are in the same place as `index.html` in the repo, and the names match exactly (lowercase, `.jpg`). |
| Old version still showing | Press **Ctrl + F5**, or check Vercel → Deployments that the latest one is "Ready". |
| Vercel name error | Project name must be lowercase: `tinubu-2027-website`. |
| No sign-up emails arriving | Activate the form first (section 7), and check your Spam folder. |
| Page looks unstyled | Don't remove the big `<style>` block at the top of `index.html` — it contains the Tailwind design. |
