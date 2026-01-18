# 🚀 Deployment Guide

## GitHub Setup

### 1. Initialize Git Repository

```bash
cd /Users/ememakpan/asylum-seekers-research/docs/Impact_of_Asylum

# Initialize git
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: Women Asylum Seekers Analysis Project"
```

### 2. Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon → "New repository"
3. Repository name: `asylum-seekers-research` or your preferred name
4. Description: "Analysis of women asylum seekers vulnerability to sexual harassment and mental health impacts"
5. Choose Public or Private
6. **DO NOT** initialize with README (we already have one)
7. Click "Create repository"

### 3. Push to GitHub

```bash
# Add remote origin
git remote add origin https://github.com/Emesticalytic/asylum-seekers-research.git
. . 
# Create main branch
git branch -M main

# Push to GitHub
git push -u origin main
```

## Streamlit Cloud Deployment

### Prerequisites
- GitHub repository (completed above)
- Streamlit Cloud account (free at [share.streamlit.io](https://share.streamlit.io))

### Deployment Steps

1. **Sign in to Streamlit Cloud**
   - Go to [share.streamlit.io](https://share.streamlit.io)
   - Sign in with GitHub

2. **Create New App**
   - Click "New app" button
   - Connect your GitHub account (if not already connected)

3. **Configure App Settings**
   - **Repository**: Select your repository (`Emesticalytic/asylum-seekers-research`)
   - **Branch**: `main`
   - **Main file path**: `docs/Impact_of_Asylum/app.py`
   - **App URL**: Choose a custom URL (e.g., `asylum-seekers-analysis`)

4. **Advanced Settings (Optional)**
   - Python version: 3.8+
   - Add secrets if needed (not required for this project)

5. **Deploy**
   - Click "Deploy!" button
   - Wait 2-5 minutes for deployment
   - Your app will be live at: `https://your-app-name.streamlit.app`

## Post-Deployment

### Update README with Live URL

```bash
# Edit README.md and add your Streamlit app URL
# Replace the placeholder in the badge link

git add README.md
git commit -m "Update README with live Streamlit app URL"
git push
```

### Verify Deployment

1. Visit your app URL
2. Test all pages and features:
   - Home page loads correctly
   - Data visualizations render
   - All navigation works
   - No errors in console

### Monitoring

- Check Streamlit Cloud dashboard for:
  - App status
  - Logs and errors
  - Resource usage
  - Analytics

## Troubleshooting

### Common Issues

1. **App won't deploy**
   - Check `requirements.txt` for correct package versions
   - Verify file path is correct: `docs/Impact_of_Asylum/app.py`
   - Check logs in Streamlit Cloud dashboard

2. **Import errors**
   - Ensure all packages are in `requirements.txt`
   - Check Python version compatibility

3. **Visualizations not showing**
   - Clear cache: Add `?clear_cache=true` to URL
   - Check matplotlib/seaborn compatibility

4. **App is slow**
   - Use `@st.cache_data` decorator (already implemented)
   - Optimize data loading
   - Reduce image sizes

## Updating Your App

```bash
# Make changes to your code
git add .
git commit -m "Description of changes"
git push

# Streamlit Cloud will automatically redeploy
```

## Custom Domain (Optional)

1. Go to Streamlit Cloud dashboard
2. Click on your app
3. Settings → Custom domain
4. Follow instructions to set up your domain

## Local Development vs Production

### Local Development
```bash
streamlit run app.py
```

### Production Environment
- Streamlit Cloud handles all infrastructure
- Automatic HTTPS
- CDN for static assets
- Auto-scaling

## Security Best Practices

1. **Never commit sensitive data**
   - Use `.gitignore` (already configured)
   - Store secrets in Streamlit Cloud secrets manager

2. **Data Privacy**
   - This project uses simulated data
   - For real data: implement proper authentication
   - Consider data encryption

3. **API Keys** (if needed in future)
   - Store in Streamlit Cloud secrets
   - Access via `st.secrets["key_name"]`

## Backup Strategy

```bash
# Create backup branch
git checkout -b backup-$(date +%Y%m%d)
git push origin backup-$(date +%Y%m%d)

# Return to main
git checkout main
```

## Support

- **Streamlit Docs**: [docs.streamlit.io](https://docs.streamlit.io)
- **Community Forum**: [discuss.streamlit.io](https://discuss.streamlit.io)
- **GitHub Issues**: Create issues in your repository

## License

MIT License - See LICENSE file for details
