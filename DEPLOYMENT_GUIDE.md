# Deployment Guide

## Step 1: Connect to GitHub

1. Go to https://github.com and create a new repository
2. Name it something like `virtruvius-ai-streamlit` or `participatory-design-generator`
3. Don't initialize with README (we already have one)
4. Copy the repository URL
5. Run these commands in your terminal:

```bash
git remote add origin <your-github-repo-url>
git branch -M main
git push -u origin main
```

## Step 2: Deploy to Streamlit Cloud

1. Visit https://share.streamlit.io
2. Sign in with your GitHub account
3. Click "New app"
4. Select your repository
5. Set main file to `app.py`
6. In Advanced settings > Secrets, add:
   ```
   GOOGLE_API_KEY = "your_google_gemini_api_key_here"
   ```
7. Click "Deploy!"

## Step 3: Get Google Gemini API Key

1. Go to https://makersuite.google.com/app/apikey
2. Create a new API key
3. Copy the key and use it in your Streamlit Cloud secrets

## Alternative Deployment Options

### Heroku
1. Install Heroku CLI
2. Create a `Procfile` with: `web: streamlit run app.py --server.port=$PORT --server.address=0.0.0.0`
3. Deploy with `git push heroku main`

### Railway
1. Connect your GitHub repository to Railway
2. Set environment variables in Railway dashboard
3. Deploy automatically on push

## Environment Variables Required

- `GOOGLE_API_KEY`: Your Google Gemini API key (required for AI features)

## Troubleshooting

- If deployment fails, check the logs for missing dependencies
- Ensure all files are committed to Git
- Verify your API key is correctly set in secrets
- Check that `requirements.txt` includes all dependencies