# Workflow Templates

This directory contains reusable GitHub Actions workflow templates for the Morningwood Gaming organization. These templates can be used as starting points when setting up Actions in any repository within the organization.

## Available Templates

### 1. Pull Request Labeler (`labeler.yml`)
Automatically labels pull requests based on file paths and patterns. Helps categorize PRs by type (docs, dependencies, frontend, backend, etc.).

**Setup:**
- Copy `.github/labeler.yml` configuration file to your repository
- Customize the labeling rules for your project's structure
- The workflow will run on every PR

**Labels include:**
- `documentation` - for documentation changes
- `dependencies` - for package/dependency updates
- `javascript`, `typescript`, `dotnet` - for language-specific changes
- `frontend`, `backend` - for architectural changes
- `testing`, `ci-cd`, `database` - for specific areas

### 2. PR Size Labeler (`pr-size-labeler.yml`)
Automatically labels pull requests based on their size (XS, S, M, L, XL). Helps reviewers understand the scope of changes at a glance.

**Size thresholds:**
- XS: up to 10 changes
- S: up to 50 changes
- M: up to 200 changes
- L: up to 500 changes
- XL: more than 500 changes

### 3. Stale Issue and PR Management (`stale.yml`)
Automatically marks and closes stale issues and pull requests to keep the repository clean and organized.

**Default settings:**
- Issues become stale after 60 days of inactivity
- PRs become stale after 45 days of inactivity
- Stale items are closed after 14 additional days
- Exempt labels: `pinned`, `security`, `blocked`, `work-in-progress`

### 4. Dependency Review (`dependency-review.yml`)
Reviews dependencies in pull requests for security vulnerabilities and license compliance. Helps prevent introducing vulnerable or incompatible dependencies.

**Features:**
- Fails PRs with moderate or higher severity vulnerabilities
- Checks license compatibility
- Comments on PRs with a summary

### 5. CodeQL Security Scanning (`codeql-analysis.yml`)
Performs security analysis on your code using GitHub's CodeQL engine. Supports JavaScript/TypeScript and C#/.NET.

**Languages supported:**
- JavaScript/TypeScript
- C#/.NET

**Scanning schedule:**
- On push to default branch
- On pull requests
- Weekly automated scans (Mondays)

### 6. Auto Assign Reviewers (`auto-assign.yml`)
Automatically assigns reviewers to pull requests based on configuration.

**Setup:**
- Copy `.github/auto-assign.yml` configuration file to your repository
- Add your team members to the reviewers list
- Configure review groups if needed

### 7. First Time Contributor Greeting (`first-interaction.yml`)
Welcomes first-time contributors with a friendly message on their first issue or pull request.

**Features:**
- Custom welcome messages for issues and PRs
- Helps build a welcoming community atmosphere
- Encourages best practices

## How to Use These Templates

### In the GitHub UI:
1. Go to your repository
2. Click on "Actions"
3. Click "New workflow"
4. Scroll down to "Workflows created by Morningwood Gaming"
5. Choose a template and click "Configure"
6. Customize as needed and commit

### Manual Setup:
1. Copy the workflow file to `.github/workflows/` in your repository
2. Copy any associated configuration files (like `labeler.yml` or `auto-assign.yml`)
3. Customize the configuration to match your project's needs
4. Commit and push

## Configuration Files

Some workflows require additional configuration files in the `.github/` directory:

- **labeler.yml** - Rules for the Pull Request Labeler
- **auto-assign.yml** - Configuration for Auto Assign Reviewers

Example configuration files are provided in the `.github/` directory of this repository.

## Customization Tips

### For JavaScript/TypeScript Projects:
- Update CodeQL matrix to focus on `javascript-typescript`
- Customize labeler to match your source structure
- Add Node.js version-specific workflows if needed

### For .NET Projects:
- Update CodeQL matrix to focus on `csharp`
- Customize labeler for .NET project structure (Controllers, Services, etc.)
- Consider adding .NET-specific linting/formatting workflows

### For Mixed Projects:
- Keep both language configurations in CodeQL
- Create comprehensive labeling rules for both ecosystems
- Consider separate workflows for different parts of the codebase

## Best Practices

1. **Start Small**: Don't enable all workflows at once. Start with labeler and PR size, then add more as needed.

2. **Customize Labels**: The labeler configuration is generic. Customize it to match your project's structure.

3. **Review Permissions**: Each workflow requests only the permissions it needs. Review these before enabling.

4. **Monitor Usage**: GitHub Actions has usage limits. Monitor your usage in the organization settings.

5. **Keep Updated**: Regularly update action versions to get the latest features and security fixes.

## Support

For questions or issues with these templates, please:
- Check the GitHub Actions documentation
- Review the action's repository for specific configuration options
- Open an issue in this repository

## Contributing

To propose changes to these templates:
1. Open an issue describing the change
2. Submit a pull request with your improvements
3. Update this README if adding new templates

---

Maintained by Morningwood Gaming
