# Installation & Setup Guide

## 🖥️ System Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Text editor (VS Code, Sublime, Notepad++)
- Python 3.x (optional, for local server)

---

## 📥 Installation Steps

### Step 1: Clone or Download the Repository

**Option A: Using Git**
```bash
git clone https://github.com/Manohar-NM/Responsive-Landing-Page.git
cd Responsive-Landing-Page
```

**Option B: Download ZIP**
1. Visit: https://github.com/Manohar-NM/Responsive-Landing-Page
2. Click "Code" → "Download ZIP"
3. Extract the ZIP file

### Step 2: Open the Project

Navigate to the project folder:
```
Responsive Landing Page/
├── index.html
├── style.css
├── script.js
├── todo-index.html
├── todo-style.css
├── todo-script.js
└── README.md
```

### Step 3: Run the Application

**Option 1: Direct Browser**
- Double-click `index.html` to open landing page
- Double-click `todo-index.html` to open to-do app

**Option 2: Python HTTP Server** (Recommended)
```bash
# Navigate to project directory
cd "path/to/Responsive Landing Page"

# Start server
python -m http.server 8000

# Open in browser
# http://localhost:8000 (Landing Page)
# http://localhost:8000/todo-index.html (To-Do App)
```

**Option 3: VS Code Live Server**
1. Install extension: "Live Server" by Ritwick Dey
2. Right-click `index.html`
3. Select "Open with Live Server"
4. Browser opens automatically

**Option 4: Node.js HTTP Server**
```bash
# Install http-server globally
npm install -g http-server

# Run server
http-server

# Open browser to localhost:8080
```

---

## ✅ Verification Checklist

After setup, verify:
- [ ] Landing page loads without errors
- [ ] Navigation menu works on desktop
- [ ] Hamburger menu works on mobile
- [ ] All links are clickable
- [ ] To-do app opens properly
- [ ] Can add tasks to to-do list
- [ ] Can mark tasks as completed
- [ ] Tasks persist after refresh
- [ ] Filters work correctly
- [ ] Mobile responsive on small screens

---

## 🐛 Troubleshooting

### Issue: Page not loading
- **Solution:** Ensure you're accessing through HTTP server, not file://
- Check browser console for errors (F12)

### Issue: Images/Styles not loading
- **Solution:** Make sure all files are in the same directory
- Check file paths in HTML are relative

### Issue: Tasks not saving
- **Solution:** Check browser's local storage is not disabled
- Verify localStorage is enabled in browser settings

### Issue: Mobile menu not working
- **Solution:** Clear browser cache
- Try a different browser
- Check JavaScript console for errors

### Issue: Form submission not working
- **Solution:** Check browser console (F12)
- Verify JavaScript is enabled
- Try a different browser

---

## 🔧 Configuration

### Changing Colors

Edit `style.css` and `todo-style.css`:
```css
:root {
    --primary-color: #2563eb;      /* Change blue */
    --secondary-color: #1e40af;    /* Change dark blue */
    --text-dark: #1f2937;          /* Change text color */
    --bg-light: #f9fafb;           /* Change background */
}
```

### Changing Contact Information

Edit `index.html` footer:
```html
<li>📧 Email: <a href="mailto:your-email@example.com">your-email@example.com</a></li>
<li>📱 WhatsApp: <a href="https://wa.me/your-number">Your Number</a></li>
```

### Changing Company Name

Edit `index.html`:
```html
<h1 class="logo">Your Company Name</h1>
<h2 class="hero-title">Welcome to Your Company</h2>
```

---

## 📊 Performance Tips

1. **Minimize HTTP Requests** - All files are optimized
2. **Use CDN for Fonts** - Already using system fonts
3. **Optimize Images** - Currently using emoji (no images)
4. **Enable Caching** - Browser caches are enabled
5. **Minify CSS/JS** - Recommended for production

---

## 🔒 Security Features

- ✅ XSS Protection in to-do app (HTML escaping)
- ✅ No external dependencies vulnerable to attacks
- ✅ Local storage only (no server communication)
- ✅ Semantic HTML5
- ✅ No sensitive data exposed

---

## 📱 Browser Compatibility

| Browser | Desktop | Mobile |
|---------|---------|--------|
| Chrome | ✅ | ✅ |
| Firefox | ✅ | ✅ |
| Safari | ✅ | ✅ |
| Edge | ✅ | ✅ |
| Opera | ✅ | ✅ |
| IE 11 | ⚠️ | N/A |

---

## 🚀 Deployment Options

### Option 1: GitHub Pages (Free)
1. Push to GitHub
2. Go to Settings → Pages
3. Select main branch
4. Your site is live at: `username.github.io/repo-name`

### Option 2: Netlify (Free)
1. Sign up at netlify.com
2. Connect GitHub repository
3. Deploy with one click

### Option 3: Vercel (Free)
1. Sign up at vercel.com
2. Import project
3. Automatic deployments on push

### Option 4: Traditional Hosting
1. Upload files via FTP
2. Access through your domain
3. Works on any web server

---

## 📞 Support

For issues or questions:
- **Email:** info.softgrowtech@gmail.com
- **WhatsApp:** +91 7839686310
- **GitHub Issues:** [Create an issue on GitHub](https://github.com/Manohar-NM/Responsive-Landing-Page/issues)

---

**Version:** 1.0.0  
**Last Updated:** February 20, 2026
