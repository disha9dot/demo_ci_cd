# untitled

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.


### 🚀 CI/CD Deployment Guide (APK & IPA)

This project uses GitHub Actions to automatically build and release Android APK and iOS IPA files whenever a new version tag is pushed.

# 📌 Prerequisites

All code changes are completed and tested
CI/CD workflow (.github/workflows/main.yml)(folder) is configured
You have push access to the repository

# 📦 Steps to Deploy a New APK / IPA
Step 1: Commit and Push Code Changes
After completing development work, commit and push your changes:

- git add .
- git commit -m "Release v1.0.10"
- git push origin <branch-name>

Step 2: Create a Version Tag
Create a new Git tag with the release version number:
- git tag v1.0.10

⚠️ Always use a new version number for each release.

Step 3: Push the Tag to GitHub

Push the tag to trigger the CI/CD pipeline:
- git push origin v1.0.10

# ⚙️ What Happens Automatically

Once the tag is pushed:
GitHub Actions workflow is triggered
Android APK files are built
iOS IPA file is generated (without code signing)
A new GitHub Release is created
APK and IPA files are uploaded as release assets

# 📥 Download Build Files

Go to GitHub → Releases
Open the latest release (e.g., v1.0.10)
Download the required APK or IPA

# ✅ Important Notes

Reusing an existing tag will not trigger the workflow
Always increment the version number (e.g., v1.0.11, v1.0.12)
The generated IPA is not code-signed and must be signed before uploading to App Store / TestFlight