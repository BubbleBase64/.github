# 🫧 Contributing to Bubbles

Welcome to the Bubbles open-source community! We're excited that you want to contribute to our AI-powered news platform. This guide will help you understand our development process and ensure consistency across all repositories in the Bubbles organization.

## 🚀 Quick Start

1. **Fork & Clone**: Fork the repository and clone your fork locally
2. **Environment Setup**: Follow the setup instructions in the specific repo's README
3. **Development Config**: Use configs from `bubbles-devops/configs` for consistent code style
4. **Submit PR**: Create a pull request following our guidelines below

---

## 🌿 Branch Naming Convention

Use clear, descriptive branch names that follow this pattern:

```bash
# Feature branches
feature/<scope>/<description>
# Examples:
feature/web/user-authentication
feature/ai/bias-detection-algorithm
feature/backend/news-aggregation-api

# Bug fix branches  
fix/<scope>/<description>
# Examples:
fix/web/login-redirect-issue
fix/ai/timeline-generation-bug

# Chore/maintenance branches
chore/<scope>/<description>
# Examples:
chore/deps/update-dependencies
chore/docs/update-readme
```

**Scopes:**
- `web` - Frontend/UI changes
- `backend` - Server-side, API changes  
- `ai` - ML models, NLP algorithms
- `devops` - Infrastructure, CI/CD
- `docs` - Documentation updates
- `deps` - Dependency updates

---

## 📝 Commit Message Style

We follow [Conventional Commits](https://www.conventionalcommits.org/) for consistent commit history:

```bash
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

### Types:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, no logic change)
- `refactor`: Code refactoring 
- `test`: Adding or updating tests
- `chore`: Build process, dependencies, tooling

### Examples:
```bash
feat(web): add user authentication system
fix(ai): resolve bias detection accuracy issue
docs(readme): update installation instructions
chore(deps): upgrade React to v18.2.0
```

---

## 🔄 Pull Request Process

### 1. PR Title Format
Your PR title should match your commit message style:
```
feat(web): add user feed personalization
fix(backend): resolve news aggregation timeout
```

### 2. Before Submitting
- [ ] Code compiles without errors
- [ ] All tests pass (`npm test` / `pytest` / etc.)
- [ ] Code follows our style guidelines (ESLint + Prettier from `bubbles-devops/configs`)
- [ ] Add tests for new features
- [ ] Update documentation if needed

### 3. PR Description Template
Our template will auto-populate, but include:
- **What changed**: Brief summary of your changes
- **Why**: The problem this solves or feature it adds
- **Testing**: How you tested your changes
- **Screenshots**: For UI changes
- **Breaking changes**: If any

### 4. Review Process
- **Auto-reviewers**: CODEOWNERS will be automatically assigned
- **Required approvals**: At least 1 approval from a code owner
- **CI checks**: All automated checks must pass
- **Merge strategy**: Squash and merge (maintains clean history)

---

## 🛠️ Development Standards

### Code Style
- **ESLint + Prettier**: Use configs from `bubbles-devops/configs`
- **TypeScript**: Preferred for new frontend code
- **Python**: Follow PEP 8, use Black formatter
- **Documentation**: Include JSDoc/docstrings for public APIs

### Testing
- **Unit tests**: Required for new features
- **Integration tests**: For API endpoints and components
- **E2E tests**: For critical user flows
- **Coverage**: Aim for >80% test coverage

### Security
- **Never commit**: API keys, passwords, or sensitive data
- **Environment variables**: Use `.env` files (not committed)
- **Dependencies**: Keep them updated, scan for vulnerabilities
- **Security issues**: Report privately to security@bubblesnews.com

---

## 🏗️ Repository Structure

### Organization Repositories:
- **`bubbles-web`**: React/Next.js frontend
- **`bubbles-backend`**: Node.js/Express API server  
- **`bubbles-ai`**: Python ML models and algorithms
- **`bubbles-devops`**: Infrastructure, CI/CD, configurations
- **`.github`**: Organization-wide templates and policies

### Integration with bubbles-devops:
```bash
# Install shared configs
npm install --save-dev @bubbles/eslint-config @bubbles/prettier-config

# Use in your project
// .eslintrc.js
module.exports = {
  extends: ['@bubbles/eslint-config']
}
```

---

## 🧭 Getting Help

### Community Resources:
- **Discussions**: Use GitHub Discussions for questions
- **Issues**: Bug reports and feature requests
- **Discord**: Real-time chat with the team
- **Documentation**: Check repo-specific docs first

### Team Contacts:
- **Project Lead**: @bahadiryavas
- **Frontend Lead**: @ececebeci  
- **Backend Lead**: @kdemirel849
- **AI/ML Lead**: @tuğbacebeci

---

## 🎯 Special Guidelines

### AI/ML Contributions:
- **Data sources**: Document all training data sources
- **Model versioning**: Use semantic versioning for model releases
- **Bias testing**: Include bias evaluation in ML PRs
- **Performance metrics**: Document accuracy, latency, resource usage

### Frontend Contributions:
- **Accessibility**: Follow WCAG 2.1 AA standards
- **Performance**: Optimize bundle size, use lazy loading
- **Responsive design**: Mobile-first approach
- **User testing**: Include usability considerations

### Backend Contributions:
- **API design**: Follow RESTful principles
- **Database migrations**: Always include rollback scripts
- **Rate limiting**: Implement appropriate limits
- **Logging**: Use structured logging for debugging

---

## ⚖️ Code of Conduct

This project follows our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you agree to uphold this code. Please report unacceptable behavior to conduct@bubblesnews.com.

---

## 📜 License

By contributing to Bubbles, you agree that your contributions will be licensed under the same license as the project (see LICENSE file in each repository).

---

Thank you for contributing to Bubbles! Together, we're building a more informed and critically thinking society. 🫧✨