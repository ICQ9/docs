# 📜 Forum Eye Legal Documentation

This directory contains the legal documentation for Forum Eye Discord Bot, including Terms of Service and Privacy Policy.

## 🌐 Published Site

Once GitHub Pages is enabled, the documentation will be available at:
- **Homepage:** `https://your-username.github.io/forum-eyes/`
- **Terms of Service:** `https://your-username.github.io/forum-eyes/terms_of_service.html`
- **Privacy Policy:** `https://your-username.github.io/forum-eyes/privacy_policy.html`

## 📁 Files

- `index.html` - Landing page with links to legal documents
- `terms_of_service.html` - Terms of Service (English)
- `privacy_policy.html` - Privacy Policy (English, GDPR compliant)
- `style.css` - Shared styles for all pages
- `README.md` - This file

## 🚀 Setup GitHub Pages

### Step 1: Push to GitHub

```bash
# Add and commit the docs folder
git add docs/
git commit -m "Add legal documentation for GitHub Pages"
git push origin main
```

### Step 2: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top right)
3. Scroll down to **Pages** (left sidebar)
4. Under **Source**, select:
   - Branch: `main`
   - Folder: `/docs`
5. Click **Save**

### Step 3: Wait for Deployment

GitHub will automatically build and deploy your site. This usually takes 1-2 minutes.

You'll see a message like:
```
Your site is live at https://your-username.github.io/forum-eyes/
```

## ✏️ Customization

### Update GitHub Link

In all HTML files, replace:
```html
<a href="https://github.com/your-repo/forum-eyes" target="_blank">GitHub</a>
```

With your actual GitHub repository URL.

### Update Contact Links

In `index.html`, `terms_of_service.html`, and `privacy_policy.html`, update:
- Discord invite link (currently: `https://discord.gg/yakuza-family`)
- GitHub Issues link (currently: `https://github.com/your-repo/forum-eyes/issues`)

### Change Colors

Edit `style.css` to customize the color scheme:

```css
:root {
    --primary-color: #dc3545;      /* Main red color */
    --primary-dark: #c82333;       /* Darker red for hover */
    --text-color: #212529;         /* Main text color */
    --text-muted: #6c757d;         /* Muted text */
    --bg-light: #f8f9fa;           /* Light background */
    --border-color: #dee2e6;       /* Border color */
    --link-color: #007bff;         /* Link color */
    --link-hover: #0056b3;         /* Link hover color */
}
```

## 🔗 Add Links to Your Bot

### In Bot Commands

Add commands to display legal links:

```python
@app_commands.command(name="terms", description="View Terms of Service")
async def terms(self, interaction: discord.Interaction):
    embed = discord.Embed(
        title="📜 Terms of Service",
        description="Please read our Terms of Service carefully.",
        color=discord.Color.red()
    )
    embed.add_field(
        name="Read Full Terms",
        value="[Click here](https://your-username.github.io/forum-eyes/terms_of_service.html)",
        inline=False
    )
    await interaction.response.send_message(embed=embed, ephemeral=True)

@app_commands.command(name="privacy", description="View Privacy Policy")
async def privacy(self, interaction: discord.Interaction):
    embed = discord.Embed(
        title="🔒 Privacy Policy",
        description="Learn how we protect your data.",
        color=discord.Color.blue()
    )
    embed.add_field(
        name="Read Full Policy",
        value="[Click here](https://your-username.github.io/forum-eyes/privacy_policy.html)",
        inline=False
    )
    await interaction.response.send_message(embed=embed, ephemeral=True)
```

### In Main Menu View

Add legal links to your main menu:

```python
class MainMenuView(discord.ui.View):
    def __init__(self):
        super().__init__(timeout=None)

        # Add Terms button
        self.add_item(discord.ui.Button(
            label="Terms of Service",
            style=discord.ButtonStyle.link,
            url="https://your-username.github.io/forum-eyes/terms_of_service.html"
        ))

        # Add Privacy button
        self.add_item(discord.ui.Button(
            label="Privacy Policy",
            style=discord.ButtonStyle.link,
            url="https://your-username.github.io/forum-eyes/privacy_policy.html"
        ))
```

### In Bot Description

Update your bot's description on Discord Developer Portal:

```
Forum Eye - Monitor complaints from Ukraine GTA5 forum

📜 Terms: https://your-username.github.io/forum-eyes/terms_of_service.html
🔒 Privacy: https://your-username.github.io/forum-eyes/privacy_policy.html
```

## 🌍 Multi-language Support (Optional)

To add Ukrainian language version:

1. Create `terms_of_service_ua.html` and `privacy_policy_ua.html`
2. Add language selector to navigation
3. Update links in both versions

Example language selector:
```html
<div class="language-selector">
    <a href="terms_of_service.html">English</a> |
    <a href="terms_of_service_ua.html">Українська</a>
</div>
```

## 📱 Mobile Responsive

The documentation is fully responsive and works on all devices:
- Desktop (1200px+)
- Tablet (768px - 1199px)
- Mobile (< 768px)

## ♿ Accessibility

Features included for accessibility:
- Semantic HTML structure
- High contrast colors
- Keyboard navigation support
- Screen reader friendly
- Print-friendly styles

## 🔍 SEO

Each page includes:
- Meta descriptions
- Keywords
- Proper heading hierarchy
- Semantic HTML

## 📊 Analytics (Optional)

To add Google Analytics, insert before `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## 🔄 Updates

When updating legal documents:

1. Edit the HTML files
2. Update the "Last Revised" date
3. Commit and push changes

## 📧 Support

For questions about the legal documentation:
- Email: majestic.forum.eye@gmail.com
- Discord: [Yakuza Family Server](https://discord.gg/SbVtdQgGWW)

---

**Ready to deploy! 🚀**

Once you enable GitHub Pages, your legal documentation will be live and accessible to all users.
