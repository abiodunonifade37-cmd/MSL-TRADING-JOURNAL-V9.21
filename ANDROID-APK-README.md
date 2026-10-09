# MSL Trading Journal V9.2 — Android APK Builder

This package contains the V9.2 web app plus a Capacitor Android wrapper and a GitHub Actions workflow that builds an installable debug APK.

## Build from GitHub on a phone

1. Create a new **public** GitHub repository, for example `MSL-Trading-Journal-V9-Android`.
2. Extract this ZIP on your phone.
3. Upload the **contents** of this folder to the repository root. Make sure `.github/workflows/android-apk.yml` is included. If GitHub's mobile upload screen hides dot-folders, create `.github/workflows/android-apk.yml` directly using GitHub's website and paste in the workflow from this package.
4. Commit the files to the `main` branch.
5. Open the repository's **Actions** tab.
6. Select **Build MSL Trading Journal Android APK** and tap **Run workflow** if it hasn't started automatically after the commit.
7. Wait for the workflow to finish successfully.
8. Open the completed workflow run, find **Artifacts**, and download `MSL-Trading-Journal-V9.2-Android-APK`.
9. Extract the downloaded artifact ZIP. It contains `app-debug.apk`.
10. Tap `app-debug.apk` on your phone and approve Android's prompt to install apps from that source, if asked.

## Supabase

This app uses the same Supabase URL and publishable/anon key configured in the app's Settings. The database schema must already be installed in Supabase. Never put a Supabase service-role/secret key in this app or repository.

## Notes

- This workflow builds a **debug APK** for direct installation/testing. It is not a Play Store release build.
- Internet is required for Supabase cloud authentication and synchronization.
- Keep the web app files at the repository root paths exactly as packaged.
