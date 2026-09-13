# CareerOrbit 🚀

**Every Exam. Every Job. Every Opportunity.**

CareerOrbit is a curated platform for discovering government exams, private sector jobs, and entrance tests across India. Built with vanilla HTML, CSS, and JavaScript for speed and accessibility.

---

## Features

✅ **Dynamic Data Loading** – Exams data loads from `exams.json` for easy updates  
✅ **Full-Text Search** – Search across exams, organizations, and categories  
✅ **Category Filtering** – Filter by UPSC, MPSC, SSC, Banking, Engineering, and more  
✅ **Responsive Design** – Mobile-first layout that works on all devices  
✅ **Accessible** – ARIA labels, semantic HTML, keyboard navigation  
✅ **Contact Form Integration** – Powered by Formspree (no backend needed)  
✅ **Fast Performance** – Single-page app with instant navigation  

---

## Getting Started

### Option 1: Host Locally (No Setup)

1. Clone the repository:
   ```bash
   git clone https://github.com/kidsy388-del/careerorbit.git
   cd careerorbit
   ```

2. Open `index.html` in your browser (works offline with sample data)

### Option 2: Host on GitHub Pages

1. Push the repo to GitHub (already done ✓)
2. Go to **Settings → Pages**
3. Set **Source** to `main` branch, folder `/root`
4. Your site will be live at: `https://kidsy388-del.github.io/careerorbit/`

### Option 3: Host on Netlify / Vercel

1. Connect your GitHub repo to [Netlify](https://netlify.com) or [Vercel](https://vercel.com)
2. Set build command: (leave empty)
3. Set publish directory: `.` (root)
4. Deploy ✓

---

## Setting Up the Contact Form

The contact form uses **Formspree** for email delivery (no backend required).

### Step 1: Create a Formspree Account

1. Visit [https://formspree.io/](https://formspree.io/)
2. Sign up with your email
3. Create a new form
4. Copy your form ID (looks like: `mnqynodv`)

### Step 2: Update index.html

Find this line in the `sendMessage()` function:

```javascript
fetch("https://formspree.io/f/mnqynodv", {
```

Replace `mnqynodv` with your Formspree form ID.

### Step 3: Test

1. Go to the **Contact** page
2. Fill out the form and submit
3. You'll receive an email confirmation from Formspree
4. All future submissions will arrive at your registered email

---

## Adding More Exams

Edit `exams.json` and add objects with this structure:

```json
{
  "name": "Exam Name",
  "org": "Organizing Body",
  "type": "government|jobs|entrance",
  "cat": "Category (e.g., UPSC, Banking, Engineering)",
  "desc": "Full description of the exam"
}
```

Your changes will appear immediately on the site.

---

## File Structure

```
careerorbit/
├── index.html          # Main application
├── exams.json          # Exam data (easily updatable)
├── README.md           # This file
└── .gitignore          # Git ignore file
```

---

## Customization

### Change Colors

Edit the CSS variables in `index.html` (near the top):

```css
:root {
  --navy: #0f1f3d;
  --marigold: #e08a1e;
  --paper: #f7f5f0;
  /* ... more colors */
}
```

### Change Branding

Replace "CareerOrbit" with your brand name:
- Header: `<span class="brand-name">Your<em>Brand</em></span>`
- Footer: Update company description

### Add More Filter Categories

In the `listing()` function, add new filter buttons:

```html
<button onclick="renderFiltered('YOUR_CAT',this)">Your Category</button>
```

---

## Accessibility

✓ WCAG 2.1 AA compliant  
✓ ARIA labels on all interactive elements  
✓ Keyboard navigation support  
✓ Focus indicators on all buttons  
✓ Semantic HTML structure  
✓ Color contrast ratios meet standards  

---

## Performance

- **No dependencies** – Pure vanilla JavaScript
- **Lightweight** – ~20KB total (uncompressed)
- **Load time** – <1s on 4G
- **Mobile optimized** – Touch-friendly buttons and forms

---

## Roadmap

- [ ] Backend API for dynamic listings
- [ ] User authentication & saved favorites
- [ ] Email notifications for new exams
- [ ] Admin panel for content management
- [ ] Dark mode toggle
- [ ] Multi-language support
- [ ] Analytics dashboard

---

## Troubleshooting

### "Failed to load exams" error
- Ensure `exams.json` is in the same directory as `index.html`
- Check your browser's console for CORS errors
- If hosting on a server, ensure JSON file is readable

### Contact form not sending
- Verify Formspree form ID is correct in `index.html`
- Check your email for Formspree verification
- Look at browser console for network errors

### Styling looks broken
- Clear browser cache (Ctrl+Shift+Delete)
- Try a different browser
- Check that fonts are loading from Google Fonts CDN

---

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

---

## License

MIT License – Feel free to use and modify for personal or commercial projects.

---

## Contributing

Have ideas or found a bug? Open an issue or pull request on [GitHub](https://github.com/kidsy388-del/careerorbit).

---

## Support

For help setting up or customizing CareerOrbit, email: kidsy388@gmail.com

---

**Built with ❤️ for career seekers across India**
