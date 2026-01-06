# GitHub Profile README Setup Guide

This guide will help you set up an auto-updating GitHub profile README similar to the example.

## Prerequisites

1. A GitHub account
2. A WakaTime account (for coding stats) - [Sign up here](https://wakatime.com/signup)
3. (Optional) Spotify account (for music stats)

## Step 1: Create Your Profile Repository

1. Create a new repository with the same name as your GitHub username
   - For example, if your username is `yourusername`, create a repo named `yourusername`
   - Make it **public**
   - **Do NOT** initialize with a README (we'll add one)

2. Clone the repository locally:
   ```bash
   git clone https://github.com/yourusername/yourusername.git
   cd yourusername
   ```

## Step 2: Set Up GitHub Actions Secrets

1. Go to your repository on GitHub
2. Navigate to **Settings** → **Secrets and variables** → **Actions**
3. Add the following secrets:

### WakaTime API Key

1. Go to [WakaTime Settings](https://wakatime.com/settings/account)
2. Scroll down to "Secret API Key"
3. Copy your API key
4. In GitHub, create a new secret:
   - **Name**: `WAKATIME_API_KEY`
   - **Value**: Your WakaTime API key

### GitHub Token (Auto-generated)

The `GITHUB_TOKEN` is automatically provided by GitHub Actions, so you don't need to create this manually.

## Step 3: Customize Your README

1. Copy the `README.md` from this repository
2. Replace all instances of `guilyx` with your GitHub username
3. Update the personal information in the YAML section:
   - Name, location, job, education, etc.
   - Update social media links
   - Update Spotify user ID (if using)

### Key Sections to Customize:

#### Profile Information (Lines 30-53)
```yaml
name: Your Name
located_in: Your City, Country
from: Your Hometown
job: Your Job Title
# ... update all fields
```

#### Social Links (Lines 15-21)
- Update LinkedIn URL
- Update Spotify user ID (get it from your Spotify profile URL)

#### Spotify Integration
- Replace `11147618695` with your Spotify user ID
- You can find this in your Spotify profile URL: `https://open.spotify.com/user/YOUR_USER_ID`

## Step 4: Enable GitHub Actions

1. Go to your repository on GitHub
2. Navigate to **Settings** → **Actions** → **General**
3. Under "Workflow permissions", select:
   - ✅ **Read and write permissions**
   - ✅ **Allow GitHub Actions to create and approve pull requests**

## Step 5: Test the Workflows

1. Push your changes to GitHub:
   ```bash
   git add .
   git commit -m "Initial setup"
   git push origin main
   ```

2. Go to the **Actions** tab in your repository
3. You should see two workflows:
   - `WakaTime Stats`
   - `Update GitHub Activity`

4. You can manually trigger them by:
   - Going to the Actions tab
   - Selecting a workflow
   - Clicking "Run workflow"

## Step 6: Wait for Updates

- **WakaTime Stats**: Updates every hour
- **GitHub Activity**: Updates every 6 hours

The first run might take a few minutes. After that, your README will auto-update on the schedule.

## Optional: Additional Customizations

### GitHub Profile Trophy
The trophy badge uses your username automatically. You can customize the theme:
- Change `theme=onedark` to other themes like `gruvbox`, `dracula`, `nord`, etc.

### Activity Graph
The activity graph automatically uses your username. You can customize:
- Theme: `github-dark-dimmed`, `github`, `github-light`, etc.
- Hide border: `hide_border=true` or `false`

### Socialify Card
Update the image URL to use your username:
```
https://socialify.git.ci/yourusername/yourusername/image?...
```

## Troubleshooting

### WakaTime stats not showing
- Verify your `WAKATIME_API_KEY` secret is set correctly
- Check that WakaTime is tracking your activity (install the WakaTime plugin in your editor)
- Wait a few hours for data to accumulate

### Activity not updating
- Ensure GitHub Actions has write permissions
- Check the Actions tab for any error messages
- Verify the workflow files are in `.github/workflows/`

### Badges not displaying
- Make sure your repository is public
- Check that the workflow badges reference the correct workflow names

## Resources

- [WakaTime README Stats](https://github.com/anmol098/waka-readme-stats)
- [GitHub Activity README](https://github.com/jamesgeorge007/github-activity-readme)
- [GitHub Profile Trophy](https://github.com/ryo-ma/github-profile-trophy)
- [GitHub Readme Activity Graph](https://github.com/ashutosh00710/github-readme-activity-graph)

## Notes

- The workflows will automatically update your README
- You can manually trigger workflows from the Actions tab
- Make sure to keep your WakaTime API key secret and never commit it to the repository

