
# Security Policy

## Overview
This project uses Firebase Authentication and Hosting to ensure secure handling of user credentials and encrypted communication (HTTPS). Sensitive configuration files are never committed to version control.

## API Key & Domain Restrictions
Firebase API keys in this project are limited to trusted domains only:

- `*.web.app` (Firebase Hosting)
- `*.firebaseapp.com` (Firebase Hosting)
- `localhost:*` (Development)

## Sensitive Configuration Files
The following files contain confidential Firebase or environment settings and are excluded from the repository:

- `lib/firebase_options.dart` (API keys and project config)
- `android/app/google-services.json` (Android config)
- `ios/Runner/GoogleService-Info.plist` (iOS config)
- `.env` (if used for environment variables)

## Secure Setup
To configure your own Firebase project:
1. Obtain your Firebase configuration from the [Firebase Console](https://console.firebase.google.com/).
2. If a template is provided, copy `lib/firebase_options_template.dart` to `lib/firebase_options.dart`.
3. Fill in your project-specific values.

## Reporting Vulnerabilities
If you find a security issue, please contact the maintainer by email rather than using the public issue tracker. This helps keep users safe while the problem is resolved.
