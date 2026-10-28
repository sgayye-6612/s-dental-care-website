# S Dental Care — Website

A one-page website for **S Dental Care** and **Dr. Sreeshma Sunder** (Orthodontist · Invisalign Provider), Moosapet X Roads, Hyderabad.

The whole site lives in one file: `index.html` (HTML, CSS and JavaScript together). It has a premium coffee-brown and gold look, a 3D tooth you can open, patient stories, clinic videos and a Google Map.

---

## 1. Folder layout

```
S-Dental/
├── index.html          ← the whole website
├── README.md           ← this file
├── images/             ← all photos (and videos, if you like)
└── videos/             ← optional: vid1–vid4 can go here instead
```

## 2. Files the page needs

Put these in the `images` folder. Names must match **exactly**, including small and capital letters.

| File | Where it shows |
|---|---|
| `Doctor.jpeg` | Main doctor photo at the top |
| `doc2.jpeg` | "Every smile has its own story" (Doctor section) |
| `doc_ria.jpg` | Treatments → Smile consultation card |
| `sreeshma_kids.jpg` | Treatments → Kids & teens card |
| `image1.jpeg` | Inside the clinic → Treatment room |
| `image2.jpeg` | Inside the clinic → Waiting lounge |
| `image3.jpeg` | Inside the clinic → Reception, and the Contact section |
| `picture1.avif` | Shown in place of the 3D tooth when there's no internet |
| `pat1` – `pat6` | Patient stories photos |
| `p1.png` and `Screenshot 2026-10-28 214722.png`, `…214742`, `…214759`, `…214816`, `…214822`, `…214830`, `…214839`, `…214849` | Smile Gallery (9 photos) |
| `vid1` – `vid4` | Clinic videos in the brown "Real smiles" section |

**Endings:** `doc2`, `doc_ria`, `sreeshma_kids`, `pat1`–`pat6` work as `.jpg`, `.jpeg` or `.png`; `pat1`–`pat6` also as `.webp` or `.avif`. Gallery photos use their exact file names. The videos work as `.mp4`, `.webm` or `.mov`, in either `images/` or `videos/`. Use **.mp4** for videos, because Chrome often can't play iPhone `.mov` files.

To see file endings in Windows: File Explorer → **View** → **Show** → **File name extensions**.

## 3. How to run it on your computer

1. Open the `S-Dental` folder in **VS Code**.
2. Install the **Live Server** extension, if you don't have it.
3. Right-click `index.html` → **Open with Live Server**. It opens at `http://127.0.0.1:5500`.
4. After changing the code, save with **Ctrl+S** and reload the page with **Ctrl+Shift+R**.

Don't double-click `index.html` to open it, and don't open a copy from Downloads. Without Live Server some parts don't load, and a copy outside this folder can't find the `images` folder.

**Needs internet for:** the fonts, the 3D tooth, the 4 stock treatment photos and the Google Map. Everything else works offline.

## 4. Page sections (top to bottom)

| Menu link | Section | What's in it |
|---|---|---|
| Home | Hero | Doctor photo with an entrance animation, badges (12+ years, 4.9 rating, Modern tech), coffee-brown waves |
| Services | Our treatments | 6 cards with photos: Invisalign, Braces, Smile consultation, Bite correction, Kids & teens, Retainers |
| Doctor | Doctor profile | doc2 photo, credentials, approach |
| About Us | About S Dental Care | Text, stats (5K+, 6+, 98%) and the **3D tooth**: drag left to open it, drag right to close it |
| Patient Stories | Patient stories | 6 story cards that slide by themselves (pat1–pat6) |
| — | Inside the clinic | 3 clinic photos |
| Gallery | Smile Gallery | 9 photos in a staggered layout; a missing file shows a "Photo missing" card with its name |
| — | Real smiles | Instagram and Facebook buttons, 4 clinic videos (vid1–vid4) |
| Contact | Contact + map | Phone, email, Instagram, Facebook, address, Google Map |

## 5. Quick edits

In VS Code, press **Ctrl+F**, search for the text shown, change it, then save.

| To change… | Search for |
|---|---|
| Phone number (it appears in several places) | `916304126855` and `63041 26855` |
| Email | `sdental332@gmail.com` |
| Address | `Sunder Square` |
| Instagram link | `instagram.com/s_dental_care` |
| Facebook link | `facebook.com/p/S-Dental-care` |
| Stats (5K+, 6+, 98%) | `data-to="5"`, `data-to="6"`, `data-to="98"` |
| Hero badges (12+, 4.9) | `data-to="12"`, `data-to="4.9"` |
| A patient story | the first few words of that story |
| Colours | `--coffee`, `--gold` (at the top of `<style>`) |

**Replacing a photo:** the easiest way is to give the new photo the same file name as the old one, and put it in `images/`.

**More gallery photos:** search for `214849`, copy that whole `<figure>…</figure>` block, paste it below, and change the file name to your new photo's name. In file names, write each space as `%20` (for example `My%20photo.png`). To remove a photo, delete its `<figure>…</figure>` block.

**Photo viewer:** tap any photo (doctor, treatments, clinic, stories, gallery, contact) to see it full-screen. Use ← → or swipe to browse, and Esc or ✕ to close.

**Instagram reels (optional):** search for `PASTE_REEL_1` and paste a real reel link in its place, like `https://www.instagram.com/reel/ABC123/`. Reels stay hidden until you do.

## 6. Before going live — checklist

- [ ] Dr. Sreeshma approves all text: credentials (BDS, MDS, FRCD), 12+ years, 4.9 rating, 5K+ clients, 6+ years, 98% satisfaction, and the treatment list.
- [ ] Replace the **sample patient stories** with each patient's own words, then delete the "Sample stories…" note.
- [ ] Get written permission from every patient whose photo or video is used, including parents for the kids' photo.
- [ ] Check the Google Map pin points to the right building. If not, get the exact embed code from Google Maps (**Share** → **Embed a map**).
- [ ] Download the 4 stock treatment photos (Unsplash and Pexels, free to use) into `images/` and change their links to local files.
- [ ] Shrink large photos and videos, ideally under 500 KB per photo and 10 MB per video, so the page loads fast on phones.
- [ ] Remove the concept note in the footer ("This is an initial website concept…").

## 7. Hosting it online (free options)

Upload the whole `S-Dental` folder (with `index.html` at the top level) to any of these:

- **Netlify** — drag the folder onto app.netlify.com/drop.
- **GitHub Pages** — push the folder to a repository, then turn on Pages in its settings.
- **Cloudflare Pages** or **Vercel** — similar drag-and-drop or GitHub setup.

Then connect a domain, for example `sdentalcare.in`, from the host's settings.

## 8. Built with

- Plain HTML, CSS and JavaScript, with no build step.
- [Three.js r128](https://threejs.org) for the 3D tooth, loaded from cdnjs.
- Google Fonts: *Playfair Display* (headings) and *Jost* (text).
- Stock photos from [Unsplash](https://unsplash.com) and [Pexels](https://www.pexels.com) (free licence).
