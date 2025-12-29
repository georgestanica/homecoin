# GitHub Copilot Chat - Troubleshooting Guide

## Problem
You see this error message in VS Code:
> Chat took too long to get ready. Please ensure you are signed in to GitHub and that the extension GitHub.copilot-chat is installed and enabled.

## Solutions

### 1. Verify GitHub Authentication

First, ensure you're properly signed in to GitHub in VS Code:

1. Open VS Code
2. Click on the **Accounts** icon in the bottom left corner (or press `Ctrl+Shift+P` / `Cmd+Shift+P`)
3. Look for your GitHub account
4. If not signed in:
   - Click **Sign in with GitHub**
   - Follow the authentication flow in your browser
   - Authorize the application

### 2. Check Copilot Extensions

Verify that both Copilot extensions are installed and enabled:

1. Open Extensions view (`Ctrl+Shift+X` / `Cmd+Shift+X`)
2. Search for and verify these extensions:
   - **GitHub Copilot** (`GitHub.copilot`)
   - **GitHub Copilot Chat** (`GitHub.copilot-chat`)
3. Make sure both show "Enabled" (not "Disabled")
4. If disabled, click the **Enable** button
5. If not installed, click **Install** for both extensions

### 3. Reload VS Code Window

After verifying authentication and extensions:

1. Press `Ctrl+Shift+P` / `Cmd+Shift+P`
2. Type "Reload Window"
3. Select **Developer: Reload Window**
4. Wait for VS Code to restart

### 4. Check Copilot Subscription

Ensure your GitHub account has an active Copilot subscription:

1. Go to [https://github.com/settings/copilot](https://github.com/settings/copilot)
2. Verify your subscription is active
3. If expired or not subscribed:
   - Follow the prompts to start a trial or subscribe
   - Return to VS Code and reload after activating

### 5. Clear Extension Cache

If the problem persists, clear the extension cache:

1. Close VS Code completely
2. Navigate to the extensions folder:
   - **Windows**: `%USERPROFILE%\.vscode\extensions`
   - **macOS/Linux**: `~/.vscode/extensions`
3. Delete or rename the folders:
   - `github.copilot-*`
   - `github.copilot-chat-*`
4. Restart VS Code
5. Reinstall both extensions

### 6. Check Network and Proxy Settings

Connection issues can be caused by network restrictions:

1. Verify you have a stable internet connection
2. If behind a corporate proxy, configure VS Code proxy settings:
   - Open Settings (`Ctrl+,` / `Cmd+,`)
   - Search for "proxy"
   - Set `http.proxy` to your proxy URL if needed
3. Check if your firewall is blocking VS Code connections
4. Ensure these domains are accessible:
   - `github.com`
   - `api.github.com`
   - `copilot-proxy.githubusercontent.com`

### 7. Update VS Code and Extensions

Use the latest versions to avoid known bugs:

1. Check for VS Code updates:
   - **Help** → **Check for Updates**
   - Install any available updates
2. Update Copilot extensions:
   - Open Extensions view
   - Look for update indicators on Copilot extensions
   - Click **Update** if available

### 8. Check Extension Logs

Review logs for specific error details:

1. Press `Ctrl+Shift+P` / `Cmd+Shift+P`
2. Type "Developer: Show Logs"
3. Select **Extension Host**
4. Look for errors related to `copilot` or `copilot-chat`
5. Address any specific errors mentioned

### 9. Restart Extension Host

Try restarting the extension host without reloading the full window:

1. Press `Ctrl+Shift+P` / `Cmd+Shift+P`
2. Type "Developer: Restart Extension Host"
3. Select the command
4. Wait a few seconds
5. Try using Copilot Chat again

### 10. Sign Out and Sign In Again

Force a fresh authentication:

1. Click the **Accounts** icon in the bottom left
2. Find your GitHub account
3. Click the account and select **Sign Out**
4. Wait a few seconds
5. Sign in again with the same steps as Solution #1
6. Reload VS Code window

## Still Having Issues?

If none of these solutions work:

1. **Check GitHub Status**: Visit [https://githubstatus.com](https://githubstatus.com) to see if Copilot services are experiencing issues
2. **Report the Issue**: Open an issue on the [Copilot feedback repository](https://github.com/community/community/discussions/categories/copilot)
3. **Include Details**: When reporting, include:
   - VS Code version (`Help` → `About`)
   - Extension versions
   - Operating system
   - Relevant error logs from Extension Host

## Quick Checklist

- [ ] Signed in to GitHub in VS Code
- [ ] GitHub Copilot extension installed and enabled
- [ ] GitHub Copilot Chat extension installed and enabled
- [ ] Active Copilot subscription
- [ ] VS Code and extensions up to date
- [ ] Window reloaded after changes
- [ ] Network connection stable

## Prevention Tips

- Keep VS Code and extensions updated regularly
- Ensure your Copilot subscription doesn't expire
- Stay signed in to GitHub in VS Code
- Restart VS Code periodically if you use it for extended periods
