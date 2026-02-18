# Security Policy

## Reporting Security Vulnerabilities

The Awesome GitHub Copilot team takes security seriously. We appreciate your efforts to responsibly disclose your findings.

### How to Report a Security Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please report security vulnerabilities by emailing:

**[security@github.com](mailto:security@github.com)**

Include as much of the following information as possible:

- Type of issue (e.g., buffer overflow, SQL injection, cross-site scripting, etc.)
- Full paths of source file(s) related to the manifestation of the issue
- The location of the affected source code (tag/branch/commit or direct URL)
- Any special configuration required to reproduce the issue
- Step-by-step instructions to reproduce the issue
- Proof-of-concept or exploit code (if possible)
- Impact of the issue, including how an attacker might exploit it

### What to Expect

After you submit a report, you should receive:

1. **Acknowledgment**: Within 48 hours, we'll acknowledge receipt of your report
2. **Updates**: We'll keep you informed about our progress
3. **Resolution**: We'll work to validate, reproduce, and address the issue
4. **Credit**: If appropriate, we'll credit you for the discovery when we publish details

## Security Best Practices for Contributors

### When Contributing Content

1. **Never include secrets**: Don't commit API keys, passwords, tokens, or other sensitive credentials
2. **Review generated code**: AI-generated code should be reviewed for security issues before use
3. **Sanitize examples**: Ensure code examples don't contain security vulnerabilities
4. **Follow secure coding practices**: Apply security best practices in instructions and prompts
5. **Validate input**: Instructions should guide users to validate and sanitize input
6. **Avoid dangerous patterns**: Don't promote insecure coding patterns

### Security Considerations for Agents and Prompts

1. **Input Validation**: Agents should encourage proper input validation
2. **Output Encoding**: Guide users to properly encode output to prevent injection attacks
3. **Authentication & Authorization**: Instructions should emphasize proper auth implementation
4. **Cryptography**: Use established libraries and don't create custom crypto
5. **Dependencies**: Keep dependencies up to date and audit for vulnerabilities
6. **Least Privilege**: Encourage principle of least privilege in generated code

### Plugin Security

1. **Review dependencies**: Audit all dependencies for known vulnerabilities
2. **Permissions**: Document all permissions and access requirements
3. **Data handling**: Clearly explain how data is processed and stored
4. **Third-party integrations**: Verify security of external services

## Security Disclaimer

### User Responsibility

The customizations (agents, prompts, instructions, skills, and plugins) in this repository are:

- **Community-contributed**: Created by third-party developers
- **Not verified by GitHub**: Not officially endorsed or guaranteed
- **Use at your own risk**: Users should review and understand code before using it

### Before Using Any Customization

1. **Review the code**: Understand what it does and what permissions it requires
2. **Check dependencies**: Audit for known security vulnerabilities
3. **Test in isolation**: Try it in a safe, non-production environment first
4. **Monitor behavior**: Watch for unexpected actions or requests
5. **Stay updated**: Keep track of updates and security patches

## Vulnerability Disclosure Policy

### Scope

This security policy applies to:

- The Awesome GitHub Copilot repository
- All agents, prompts, instructions, skills, and plugins within
- Supporting scripts and infrastructure
- Documentation and examples

### Out of Scope

- Issues in GitHub Copilot itself (report to GitHub)
- Third-party services referenced in customizations
- General GitHub platform issues

## Security Updates

When security issues are identified and resolved:

1. We'll update the affected files
2. Document the issue in commit messages (after resolution)
3. Notify users if action is required
4. Credit security researchers (with permission)

## Supported Versions

We address security issues in:

- The current main branch
- Recently released content (within 90 days)

Older content may not receive security updates. Users should:

- Use the latest versions when possible
- Review older content carefully before using
- Report security issues regardless of content age

## Security Resources

- [GitHub Security Advisories](https://github.com/advisories)
- [OWASP Top Ten](https://owasp.org/www-project-top-ten/)
- [CWE/SANS Top 25](https://cwe.mitre.org/top25/)
- [GitHub Security Best Practices](https://docs.github.com/en/code-security)

## Additional Security Measures

### For Repository Maintainers

- Enable branch protection on main branch
- Require pull request reviews
- Use automated security scanning
- Regularly audit dependencies
- Keep actions and workflows secure

### For Content Creators

- Follow secure coding guidelines
- Test for common vulnerabilities
- Document security assumptions
- Provide security-focused examples
- Stay informed about security trends

## Contact

For security-related questions or concerns:

- **Security issues**: [security@github.com](mailto:security@github.com)
- **General questions**: Open a discussion on GitHub
- **Non-security bugs**: Create a GitHub issue

## Acknowledgments

We thank the security researchers and community members who help keep Awesome GitHub Copilot secure.

---

**Remember**: Security is everyone's responsibility. Thank you for helping keep this project safe and secure for all users.
