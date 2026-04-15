# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in this project, please report it responsibly:

1. **Do not** open a public GitHub issue for security vulnerabilities.
2. Email the maintainer at **sydul.cit.bd@gmail.com** with details of the vulnerability.
3. Include steps to reproduce, impact assessment, and any suggested fixes.

We will acknowledge receipt within 48 hours and aim to release a fix within 7 days for critical issues.

## Security Best Practices for Contributors

### Secrets and Credentials

- **Never** commit API keys, tokens, passwords, or other secrets to the repository.
- Use environment variables or a `.env` file (already in `.gitignore`) for sensitive configuration.
- See `.env.example` for the expected environment variable format.
- If you accidentally commit a secret, rotate it immediately and notify the maintainers.

### Dependencies

- Pin all dependency versions in `requirements.txt` to avoid supply-chain attacks.
- Regularly audit dependencies with `pip-audit` or `safety check`.
- Only use well-maintained, reputable packages.

### Data Handling

- Do not commit training data that contains personally identifiable information (PII).
- Sanitize and validate all external data inputs before use in model training pipelines.
- Store model artifacts and large datasets outside the repository (use cloud storage with proper access controls).

### Notebook Security

- Clear all cell outputs before committing notebooks to avoid leaking secrets, tokens, or sensitive data that may appear in output cells.
- Do not hardcode file paths, credentials, or API endpoints in notebooks.
- Use parameterized configuration instead.

### Code Review

- All changes should go through pull request review.
- Reviewers should check for hardcoded secrets, insecure patterns, and dependency issues.

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| main    | Yes                |
