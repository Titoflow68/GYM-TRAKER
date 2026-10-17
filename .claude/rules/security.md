# Security

- Never commit API keys, tokens, passwords, or secrets.
- Never install packages from untrusted sources.
- Never run shell commands that delete files outside the project directory.
- Never expose internal file paths or infrastructure details in client-facing code.
- If .env exists, never read or display its contents -- reference variable names only.
- The GitHub repo is PUBLIC: never commit personal health data (weight, measurements, medical info) or real workout/nutrition logs. Keep them in data/ (gitignored).
