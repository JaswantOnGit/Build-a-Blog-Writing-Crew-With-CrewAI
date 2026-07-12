# Security Policy

## Supported Versions

This is a small learning/portfolio project and does not currently maintain multiple supported versions. Security fixes, if needed, will be applied to the `main` branch.

## Reporting a Vulnerability

This project does not handle sensitive user data, but if you discover a security issue (for example, a leaked credential pattern or an unsafe dependency), please open a private report using GitHub's "Report a vulnerability" feature under the Security tab, or open a regular issue if the concern is not sensitive.

Please avoid publicly disclosing details of a serious vulnerability until it has been reviewed.

## Notes on API Keys and Secrets

This project uses a `.env` file to store API keys (such as a Gemini API key). Never commit real API keys or secrets to this repository. The `.gitignore` file is configured to exclude `.env` from version control.
