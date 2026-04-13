# Deployment Guide

This guide will help you deploy the Ecommerce Retail Dashboard to Vercel and push it to GitHub.

## 📋 Prerequisites

- **Git** installed on your machine
- **GitHub account** (free)
- **Vercel account** (sign up at [vercel.com](https://vercel.com))
- **Node.js** (optional, for local testing)

## 🚀 Step 1: Initialize Git Repository Locally

Open your terminal/PowerShell in the project directory and run:

```bash
# Initialize git repository
git init

# Add all files to git
git add .

# Create initial commit
git commit -m "Initial commit: Ecommerce Retail Dashboard"
```

## 📤 Step 2: Push to GitHub

### 2.1 Create a New Repository on GitHub

1. Go to [GitHub](https://github.com/new)
2. Create a new repository named `ecommerce-retail-dashboard`
3. **Do NOT** initialize with README (we already have one)
4. Click "Create repository"

### 2.2 Push Your Local Repository

After creating the GitHub repository, copy the commands provided by GitHub (usually looks like this):

```bash
# Add the remote repository
git remote add origin https://github.com/YOUR_USERNAME/ecommerce-retail-dashboard.git

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

## 🌐 Step 3: Deploy to Vercel

### 3.1 Connect Vercel to GitHub

1. Sign in to [Vercel](https://vercel.com/dashboard)
2. Click **"Add New..."** → **"Project"**
3. Select **"Import Git Repository"**
4. Authorize Vercel to access your GitHub account
5. Select the `ecommerce-retail-dashboard` repository

### 3.2 Configure Deployment Settings

- **Framework Preset**: Select "Other" (since it's a static site)
- **Build Command**: Leave empty
- **Output Directory**: Leave empty
- **Environment Variables**: No additional variables needed

### 3.3 Deploy

Click **"Deploy"** and wait for the deployment to complete.

Vercel will automatically:
- Build and optimize your static site
- Deploy to a global CDN
- Provide you with a live URL (e.g., `https://ecommerce-retail-dashboard.vercel.app`)

## ✅ Verification

After deployment:

1. Visit your Vercel deployment URL
2. Verify all files load correctly
3. Test the PDF download functionality
4. Check the Excel file download
5. Verify responsive design (test on mobile)

## 📝 Post-Deployment Steps

### Add Custom Domain (Optional)

1. In Vercel dashboard, go to your project
2. Navigate to **"Settings"** → **"Domains"**
3. Add your custom domain
4. Follow DNS configuration steps

### Enable Analytics (Optional)

1. In Vercel dashboard, enable **"Web Analytics"**
2. Start tracking visitor insights

### Set Up Auto-Deployments

Vercel automatically deploys on every push to the `main` branch.

To change this:
1. Go to **"Settings"** → **"Git"**
2. Configure branch and deployment rules

## 🔄 Making Updates

To make changes and redeploy:

```bash
# Make your changes locally
# Then:

git add .
git commit -m "Description of changes"
git push origin main

# Vercel will automatically redeploy!
```

## 🐛 Troubleshooting

### Files Not Found (404 Error)

- Verify all file paths in `index.html` are correct
- Ensure file names match exactly (case-sensitive on Linux/Mac)
- Check that `Ecommerce Product Review Dashboard.xlsx` and `EPRD.png` exist

### PDF Download Not Working

- Ensure `html2pdf` library loads from CDN
- Check browser console for errors (F12)
- Verify file name in download is correct

### Git Push Fails

```bash
# Pull latest changes first
git pull origin main

# Then push
git push origin main
```

### Vercel Deployment Fails

1. Check the Vercel build logs in your dashboard
2. Ensure `.gitignore` doesn't exclude important files
3. Verify all assets are committed to git

## 📚 Additional Resources

- [Vercel Documentation](https://vercel.com/docs)
- [GitHub Quick Start](https://docs.github.com/en/get-started/quickstart)
- [Git Basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)

## 🆘 Need Help?

- Check the repository's GitHub Issues
- Contact: harshad.dhongade@example.com
- LinkedIn: [harshad-dhongade](https://www.linkedin.com/in/harshad-dhongade)

---

**Deployment completed!** Your dashboard is now live on the internet. 🎉
