# Publishing to GitHub Marketplace

## ✅ Prerequisites Completed

- [x] Repository created: `kubigo/release`
- [x] Action files created (`action.yml`, `src/index.js`)
- [x] Built and compiled (`dist/index.js`)
- [x] README with comprehensive documentation
- [x] Examples provided
- [x] Tagged with `v1.0.0` and `v1`
- [x] Sub-actions created (deploy, approve, rollback)
- [x] Multi-container support added

## 📋 Steps to Publish to Marketplace

### 1. Create a Release on GitHub

1. Go to https://github.com/kubigo/release/releases
2. Click **"Draft a new release"**
3. Fill in the details:
   - **Tag**: `v1.0.0` (already created)
   - **Release title**: `v1.0.0 - Initial Release`
   - **Description**:

```markdown
## 🎉 Initial Release

Kubigo Release Action allows you to automatically create releases in Kubigo after successful builds.

### ✨ Features

- ✅ Auto-detects repository, branch, and commit from GitHub context
- 🚀 Auto-deploys to environments without approval requirements
- 📊 Rich outputs for downstream workflow steps
- 🔒 Secure API key authentication
- 📝 Detailed logging with release status

### 📦 What's Included

- **Main Action**: Create releases from CI/CD
- **Deploy Action**: Deploy specific releases (`/deploy`)
- **Approve Action**: Approve pending releases (`/approve`)
- **Rollback Action**: Rollback to previous releases (`/rollback`)

### 🚀 Quick Start

```yaml
- uses: kubigo/release@v1
  with:
    kubigo-url: ${{ secrets.KUBIGO_URL }}
    api-key: ${{ secrets.KUBIGO_API_KEY }}
    images: myrepo/myapp:${{ github.sha }}
```

### 📚 Documentation

See [README.md](https://github.com/kubigo/release#readme) for full documentation.
```

4. Check **"Set as the latest release"**
5. Click **"Publish release"**

### 2. Publish to Marketplace

After creating the release:

1. GitHub will automatically detect the `action.yml` file
2. You'll see a banner: **"Publish this Action to the GitHub Marketplace"**
3. Click **"Publish this Action to the GitHub Marketplace"**
4. Fill in the marketplace details:

#### Primary Category
- **Continuous Integration**

#### Additional Categories (optional)
- **Deployment**
- **Utilities**

#### Marketplace Listing Details

**Short Description** (max 125 chars):
```
Automatically create and deploy Kubernetes releases with approval workflows
```

**Icon**: `package` (already set in action.yml)
**Color**: `blue` (already set in action.yml)

**Terms and Conditions**:
- [x] I agree to the GitHub Marketplace Developer Agreement
- [x] I agree to the GitHub Marketplace Terms of Service

5. Click **"Publish release"**

### 3. Verify Marketplace Listing

1. Visit: https://github.com/marketplace/actions/kubigo-release
2. Verify all information is correct
3. Check that examples render properly

## 🎨 Marketplace Optimization

### README Best Practices

- [x] Clear title and description
- [x] Badges (Marketplace, License)
- [x] Quick start example
- [x] Comprehensive input/output documentation
- [x] Multiple usage examples
- [x] Troubleshooting section
- [x] Support information

### SEO Keywords

Make sure README includes these keywords:
- [x] kubernetes
- [x] deployment
- [x] release management
- [x] ci/cd
- [x] github actions
- [x] docker
- [x] continuous deployment

### Screenshots (Optional but Recommended)

Consider adding screenshots to README:
1. Kubigo dashboard showing releases
2. GitHub Actions workflow run
3. Release approval flow

## 📊 Post-Publishing

### Monitor Usage

1. Check marketplace analytics:
   - https://github.com/kubigo/release/insights/traffic
2. Monitor issues and discussions
3. Respond to user feedback

### Promote the Action

1. **Blog Post**: Announce the release
2. **Social Media**: Share on Twitter, LinkedIn
3. **Documentation**: Update Kubigo docs to reference the action
4. **Community**: Share in relevant Discord/Slack channels

### Version Management

For future updates:

```bash
# Create new version
git tag -a v1.1.0 -m "Release v1.1.0 - New features"
git push origin v1.1.0

# Update major version tag
git tag -f v1
git push origin v1 --force

# Create GitHub release
# Marketplace will auto-update
```

## 🔍 Marketplace Checklist

Before publishing, ensure:

- [x] `action.yml` has correct metadata
- [x] `branding` section is set (icon, color)
- [x] README is comprehensive
- [x] Examples are tested and working
- [x] License file exists (MIT)
- [x] Repository is public
- [x] No sensitive information in code
- [x] Dependencies are properly declared
- [x] Action is tested in a real workflow

## 📝 Marketplace Metadata

### Current Settings

```yaml
name: 'Kubigo Release Action'
description: 'Automatically create releases in Kubigo after successful builds'
author: 'Kubigo'
branding:
  icon: 'package'
  color: 'blue'
```

### Available Icons

If you want to change the icon later:
- `package` (current)
- `upload-cloud`
- `server`
- `box`
- `layers`

### Available Colors

If you want to change the color later:
- `blue` (current)
- `green`
- `purple`
- `red`
- `orange`

## 🎯 Success Metrics

Track these metrics after publishing:

1. **Installations**: Number of workflows using the action
2. **Stars**: GitHub stars on the repository
3. **Issues**: User-reported issues (aim for quick responses)
4. **Pull Requests**: Community contributions
5. **Marketplace Ranking**: Position in search results

## 🆘 Troubleshooting

### "Action not found in Marketplace"

- Ensure release is published
- Check that action.yml is in repository root
- Verify repository is public

### "Invalid action.yml"

- Validate YAML syntax
- Ensure all required fields are present
- Check branding section

### "Action fails to run"

- Test locally with `act` tool
- Check dist/index.js is committed
- Verify dependencies are bundled

## 📚 Resources

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Publishing Actions to Marketplace](https://docs.github.com/en/actions/creating-actions/publishing-actions-in-github-marketplace)
- [Action Metadata Syntax](https://docs.github.com/en/actions/creating-actions/metadata-syntax-for-github-actions)
- [Marketplace Developer Agreement](https://docs.github.com/en/github/site-policy/github-marketplace-developer-agreement)

---

**Ready to publish!** 🚀

Follow the steps above to make Kubigo Release Action available to the GitHub community.
