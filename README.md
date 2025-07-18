<<<<<<< HEAD
# Occlu-FER Dataset Website

This repository contains the source code for the Occlu-FER dataset website, built with Hugo and the PaperMod theme. The website showcases a deep learning dataset for occluded facial expression recognition research.

## 🚀 Deploying to GitHub Pages

Since you already have a GitHub repository with the same name, you'll need to connect your local repository to the existing GitHub repository. Here's how to do it:

### 1. Connect Local Repository to GitHub

```bash
# Initialize git in your local repository (if not already done)
git init

# Add the remote GitHub repository
git remote add origin https://github.com/your-username/Occlu-FER.git

# Verify the remote was added
git remote -v
```

### 2. Handle Existing Content on GitHub

If your GitHub repository already has content, you'll need to pull it first:

```bash
# Pull the existing content (use --allow-unrelated-histories if needed)
git pull origin main --allow-unrelated-histories

# Resolve any conflicts if they occur
```

### 3. Add and Commit Your Local Changes

```bash
# Add all files
git add .

# Commit the changes
git commit -m "Add Hugo website for Occlu-FER dataset"
```

### 4. Push to GitHub

```bash
# Push to the main branch
git push -u origin main
```

### 5. Configure GitHub Pages

1. Go to your GitHub repository
2. Navigate to Settings → Pages
3. Under "Source", select "GitHub Actions"
4. GitHub will detect the Hugo workflow file and use it for deployment

## 🔧 Local Development

### Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) (v0.128.0 or later)
- [Git](https://git-scm.com/)

### Running Locally

```bash
# Start the Hugo development server
hugo server

# Or with draft content
hugo server -D
```

## 📝 Customization

### Update Site Information

Edit `hugo.toml` to customize:
- Change `baseURL` to your actual GitHub Pages URL
- Update social links and other parameters

### Content Updates

Edit `content/_index.md` to update the main page content.

## 📦 Building for Production

```bash
# Generate the static site
hugo --gc --minify
```

The generated site will be in the `public/` directory.

---

**Note**: The GitHub Actions workflow will automatically build and deploy your site when you push changes to the main branch.
=======
# Occlu-FER
>>>>>>> 957bf6d319fb057d92d4b1c6348fad82835e76ba
