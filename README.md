# Naveen Kapoor — Portfolio

Personal portfolio site built from your resume. Static HTML/CSS/JS — no build step required.

## Deploy on GitHub Pages

### 1. Create a GitHub repository

1. Go to [github.com/new](https://github.com/new)
2. Name it e.g. `naveen-kapoor-portfolio` (or `yourusername.github.io` for a custom root URL)
3. Leave it **empty** (no README, no .gitignore)
4. Click **Create repository**

### 2. Push this project

From your terminal:

```bash
cd ~/Projects/naveen-kapoor-portfolio

git remote add origin https://github.com/YOUR_USERNAME/naveen-kapoor-portfolio.git
git branch -M main
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username.

### 3. Enable GitHub Pages

1. Open your repo on GitHub → **Settings** → **Pages**
2. Under **Build and deployment** → **Source**, choose **Deploy from a branch**
3. Branch: **main**, folder: **/ (root)**
4. Click **Save**

Your site will be live in 1–2 minutes at:

- `https://YOUR_USERNAME.github.io/naveen-kapoor-portfolio/`  
  (or `https://YOUR_USERNAME.github.io/` if the repo is named `YOUR_USERNAME.github.io`)

---

## Edit content

| What to change | File |
|----------------|------|
| Name, bio, jobs, contact links | `index.html` |
| Colors, fonts, layout | `styles.css` |
| Scroll animations, mobile menu | `script.js` |

Open the folder in Cursor or any editor, edit, save, then push:

```bash
git add .
git commit -m "Update portfolio content"
git push
```

GitHub Pages redeploys automatically after each push.

---

## Add photos

### Step 1 — Add image files

Put your images in the `images/` folder:

```
images/
  profile.jpg      ← headshot for About section
  hertz.jpg        ← optional project/company image
  cognizant.jpg
```

Use `.jpg`, `.png`, or `.webp`. Keep files under ~500 KB for fast loading.

### Step 2 — Reference them in HTML

**Profile photo (About section)** — add inside the `#about` section in `index.html`:

```html
<div class="about-photo reveal">
  <img src="images/profile.jpg" alt="Naveen Kapoor" />
</div>
```

**Company or project image** — inside a role card:

```html
<img src="images/hertz.jpg" alt="Hertz Counter Experience" class="role-image" />
```

The CSS for these classes is already included in `styles.css` (search for `.about-photo` and `.role-image`).

### Step 3 — Preview locally

Open `index.html` in your browser (double-click the file), or run:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`

---

## Project structure

```
naveen-kapoor-portfolio/
├── index.html      # All page content
├── styles.css      # Styling
├── script.js       # Interactions
├── images/         # Your photos go here
├── vercel.json     # Optional — for Vercel deploy instead
└── README.md       # This file
```

## Optional: deploy on Vercel instead

1. Push to GitHub (steps above)
2. Go to [vercel.com](https://vercel.com) → **Add New Project**
3. Import your GitHub repo → Deploy (no settings needed)

---

## Contact info on the site

- Email: tlk2naveen@gmail.com
- Phone: 510-598-5943
- LinkedIn: linkedin.com/in/naveen-kapoor-59908317

Update these directly in the **Contact** section and **hero** of `index.html`.
