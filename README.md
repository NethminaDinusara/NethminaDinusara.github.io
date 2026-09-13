# Dinusara Wijewardana — Portfolio

Single-file portfolio website. Free hosting on GitHub Pages.

---

## 📁 Repository එකේ තියෙන්න ඕන Folder Structure එක

```
your-username.github.io/
├── index.html          ← main website file
├── README.md
├── CV.pdf              ← ඔයාගේ CV එක (Résumé button එකට)
└── images/             ← මේ folder එක හදන්න ඕන
    ├── profile.jpg                    ← ඔයාගේ photo එක
    ├── vehicle-1.jpg
    ├── vehicle-2.jpg
    ├── vehicle-video-thumb.jpg
    ├── pet-robot-1.jpg
    ├── pet-robot-2.jpg
    ├── pet-robot-video-thumb.jpg
    ├── line-follower-1.jpg
    ├── line-follower-2.jpg
    └── line-follower-video-thumb.jpg
```

> Image එකක් නැත්නම් website එක break වෙන්නේ නෑ — "test card" placeholder එකක් පේනවා. ඒ නිසා photos ටිකෙන් ටික add කරන්න පුළුවන්.

---

## 📸 Photo එක දාන්නේ කොහෙද?

**ඔයාගේ portrait එක:** `images/profile.jpg`

Hero section එකේ දකුණු පැත්තේ, name එකට ලඟින් පේනවා — corner registration ticks එක්ක frame කරලා, drifting scanline එකක් උඩින් යනවා (live feed එකක් වගේ).

| Image | Size (best) | Notes |
|---|---|---|
| `profile.jpg` | **800 × 1000 px** (4:5 portrait) | මුහුණ මැදට, උරහිස් ටිකක් පේන්න. Plain background එකක් හොඳයි |
| Project photos | **1200 × 800 px** (3:2 landscape) | Robot එක හොඳට පේන්න, හොඳ ආලෝකයක් තියෙන තැනක |
| Video thumbnails | **1200 × 800 px** | Video එකේ හොඳම frame එක |

**වැදගත්:** හැම image එකක්ම **300 KB** ට වඩා අඩුවෙන් තියාගන්න. [squoosh.app](https://squoosh.app) එකෙන් free compress කරන්න පුළුවන් — quality එක නැති නොවී size එක 80% ක් අඩු වෙනවා.

### Images upload කරන විදිහ

1. Repository එකේ **Add file → Create new file** click කරන්න
2. File name එකේ type කරන්න: `images/temp.txt` (මේකෙන් `images` folder එක හැදෙනවා)
3. **Commit** කරන්න
4. දැන් `images` folder එකට ගිහින් **Add file → Upload files** click කරලා photos ඔක්කොම drag & drop කරන්න
5. `temp.txt` එක පස්සේ delete කරන්න පුළුවන්

---

## 🎬 Videos දාන්නේ කොහොමද?

Video files (mp4) කෙලින්ම GitHub එකට upload කරන එක **recommend කරන්නේ නෑ** — file size ලොකුයි, site එක slow වෙනවා.

**හොඳම ක්‍රමය — YouTube:**

1. Video එක YouTube එකට upload කරන්න → **Unlisted** select කරන්න (search වලට එන්නේ නෑ, link එකෙන් විතරයි බලන්න පුළුවන්)
2. Video URL එකෙන් **ID** එක ගන්න:
   ```
   https://www.youtube.com/watch?v=dQw4w9WgXcQ
                                   ^^^^^^^^^^^
                                   මේක තමයි ID එක
   ```
3. `index.html` එකේ `REPLACE_ID_1` හොයලා ඒ ID එක දාන්න:

   **කලින්:**
   ```html
   <div class="tile vid" data-yt="REPLACE_ID_1" tabindex="0">
   ```
   **පස්සේ:**
   ```html
   <div class="tile vid" data-yt="dQw4w9WgXcQ" tabindex="0">
   ```

4. Thumbnail image එකත් `images/` folder එකට දාන්න

Video IDs 3ක් තියෙනවා: `REPLACE_ID_1` (vehicle), `REPLACE_ID_2` (pet robot), `REPLACE_ID_3` (line follower).

> Video එක click කරන කල් YouTube player එක load වෙන්නේ නෑ (facade pattern) — ඒකෙන් page එක ගොඩක් වේගවත් වෙනවා.

---

## ⚠️ වෙනස් කරන්න ඕන Dummy Details

`index.html` එකේ **Ctrl+F** එකෙන් `REPLACE` කියලා search කරොත් ඔක්කොම හොයාගන්න පුළුවන්.

| දැන් තියෙන්නේ | දාන්න ඕන |
|---|---|
| `dinusara.wijewardana@example.com` | ඔයාගේ real email — **2 තැනක** (`mailto:` සහ display text) |
| `linkedin.com/in/your-linkedin-username` | LinkedIn URL — **2 තැනක** |
| `+94 77 000 0000` / `tel:+94770000000` | Phone number |
| `github.com/your-github-username` | GitHub username — **2 තැනක** |
| `REPLACE_ID_1/2/3` | YouTube video IDs |
| `CV.pdf` | CV එක repo එකට upload කරන්න |

---

## 🚀 GitHub Pages Hosting

1. GitHub.com → **New repository**
2. Name: `your-username.github.io` (හරියටම මේ format එකට)
3. **Public** → Create
4. Files ඔක්කොම upload කරන්න
5. `https://your-username.github.io` — live! 🎉

---

## ✏️ Host කරාට පස්සේ Edit කරන විදිහ

Browser එකෙන්ම: `index.html` → **pencil (✏️) icon** → edit → **Commit changes**.
1-2 minutes ඇතුළත live site එකේ update වෙනවා. Software එකක් අවශ්‍ය නෑ.

---

## ➕ අලුත් Project එකක් Add කරන්න

`Build log` section එකේ `<article class="build-row rv">` block එකක් copy කරලා content එක වෙනස් කරන්න. Media tiles වල `data-full` සහ `src` paths අලුත් image names වලට වෙනස් කරන්න මතක තියාගන්න.

- `chip live` = cyan "IN PROGRESS"
- `chip done` = amber "COMPLETE"

---

## 🎨 Colors

`:root` block එකේ:
```css
--amber:#FFB03A;   /* main accent */
--cyan:#5FD0E8;    /* in-progress / video accents */
--void:#080B11;    /* background */
```

---

## Design notes

**Concept:** oscilloscope / instrument panel. Animations ඔක්කොම එකම vocabulary එකේ —
beam sweep on section rules, scanline "signal acquire" on images, drifting feed line on
the portrait, pulsing play buttons, signal-strength scroll progress.

- Type: Archivo (display) + IBM Plex Sans (body) + IBM Plex Mono (data)
- Lightbox on project photos (Esc to close, keyboard accessible)
- Lazy-loaded video facades
- `prefers-reduced-motion` respected — animations ඔක්කොම නවතිනවා
- No frameworks, no build step — single HTML file
