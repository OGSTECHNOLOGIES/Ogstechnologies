# Deployment Guide for OGS Technologies Website

This guide will help you deploy your OGS Technologies website to GitHub Pages.

## Prerequisites

- A GitHub account
- Git installed on your computer
- Your website code in a local folder

## Step-by-Step Deployment Instructions

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository (e.g., `ogs-technologies-website`)
5. Choose "Public" visibility
6. Do NOT initialize with README (since you already have one)
7. Click "Create repository"

### Step 2: Push Your Code to GitHub

Open your terminal in the project folder and run these commands:

```bash
git init
git add .
git commit -m "Initial commit: OGS Technologies website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

Replace `YOUR-USERNAME` and `YOUR-REPO-NAME` with your actual GitHub username and repository name.

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings" tab
3. Scroll down to "Pages" in the left sidebar
4. Under "Source", select "GitHub Actions"
5. The deployment workflow is already configured in `.github/workflows/deploy.yml`

### Step 4: Wait for Deployment

1. Go to the "Actions" tab in your repository
2. You should see a workflow running
3. Wait for it to complete (usually takes 1-2 minutes)
4. Once complete, your site will be live

### Step 5: Access Your Website

Your website will be available at:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

## Automatic Updates

Every time you push changes to the `main` branch, your website will automatically rebuild and deploy.

To make updates:

```bash
git add .
git commit -m "Description of your changes"
git push
```

## Using a Custom Domain (Optional)

If you want to use your own domain name:

1. Go to repository Settings > Pages
2. Under "Custom domain", enter your domain name
3. Add the following DNS records with your domain provider:

```
Type: A
Host: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153

Type: CNAME
Host: www
Value: YOUR-USERNAME.github.io
```

4. Wait for DNS propagation (can take up to 48 hours)
5. Enable "Enforce HTTPS" in GitHub Pages settings

## Troubleshooting

### Build Fails
- Check the Actions tab for error messages
- Ensure all dependencies are listed in `package.json`
- Try running `npm run build` locally to test

### Site Not Loading
- Wait a few minutes after deployment completes
- Clear your browser cache
- Check the Actions tab to ensure deployment was successful

### Images Not Showing
- Ensure all image paths are correct
- Images should be in the `public` folder or `src/assets`
- Check browser console for 404 errors

## Support

For technical support with GitHub Pages, visit:
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Astro Deployment Guide](https://docs.astro.build/en/guides/deploy/github/)

For OGS Technologies website support:
- Phone: 09064424710, 09133970588
- Address: No: 25 Powa Shop, Opp. St. Finbarrs Catholic Church, Bende Rd, Umuahia, Abia State
