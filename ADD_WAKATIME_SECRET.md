# How to Add Your WakaTime API Key to GitHub

## Your WakaTime API Key:
```
waka_39991e25-4b52-406c-a333-67dd2cf22c57
```

## Steps to Add as GitHub Secret:

1. **Go to your GitHub repository** (the one with your username, e.g., `yourusername/yourusername`)

2. **Navigate to Settings**:
   - Click on the **Settings** tab in your repository

3. **Go to Secrets and Variables**:
   - In the left sidebar, click on **Secrets and variables**
   - Then click on **Actions**

4. **Add New Secret**:
   - Click the **New repository secret** button
   - **Name**: `WAKATIME_API_KEY` (must be exactly this)
   - **Secret**: Paste your API key: `waka_39991e25-4b52-406c-a333-67dd2cf22c57`
   - Click **Add secret**

5. **Verify**:
   - You should now see `WAKATIME_API_KEY` listed in your secrets
   - The value will be hidden (showing as `••••••••`)

## After Adding the Secret:

1. The workflow will automatically use this secret on the next run
2. You can manually trigger it by:
   - Going to the **Actions** tab
   - Selecting **WakaTime Stats** workflow
   - Clicking **Run workflow**

## Important Security Notes:

⚠️ **NEVER** commit your API key to the repository
⚠️ **NEVER** share your API key publicly
✅ The secret is encrypted and only accessible to GitHub Actions
✅ Only repository collaborators with admin access can view/edit secrets

## Troubleshooting:

- If stats don't appear, wait a few hours for WakaTime to collect data
- Make sure you have the WakaTime extension installed in your code editor
- Check the Actions tab for any error messages

