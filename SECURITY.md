# Security Policy

## Supported Versions

Given the early stage of the project, we currently only support the latest version with security updates:

| Version | Supported          |
| ------- | ------------------ |
| 0.0.x   | :white_check_mark: |
| < 0.0.1 | :x:                |

### For Contributors

1. **API Keys and Secrets**

    - Never commit API keys, passwords, or other secrets to the repository
    - Use environment variables as described in our secrets management guide
    - Rotate any accidentally exposed credentials immediately

2. **Dependencies**

    - Keep all dependencies up to date
    - Review security advisories for dependencies regularly
    - Use `pnpm audit` to check for known vulnerabilities

3. **Code Review**
    - All code changes must go through pull request review
    - Security-sensitive changes require additional review
    - Enable branch protection on main branches

### For Users

1. **Environment Setup**

    - Follow our [secrets management guide](docs/guides/secrets-management.md) for secure configuration
    - Use separate API keys for development and production
    - Regularly rotate credentials

2. **Model Provider Security**

    - Use appropriate rate limiting for API calls
    - Monitor usage patterns for unusual activity
    - Implement proper authentication for exposed endpoints

3. **Platform Integration**
    - Use separate bot tokens for different environments
    - Implement proper permission scoping for platform APIs
    - Regular audit of platform access and permissions

## Security Features

### Current Implementation

-   Environment variable based secrets management
-   Type-safe API implementations
-   Automated dependency updates via Renovate
-   Continuous Integration security checks


