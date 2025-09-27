# 📄 Our Contribution Templates

To keep our workflow consistent and clear, we use two main templates: one for overall contributions and one for Pull Requests.

---

### ## The `CONTRIBUTING.md` File

This file is the high-level guide for anyone working in our repositories. It sets the ground rules for our workflow, communication, and coding standards. A link to it is automatically shown when someone creates a new issue or pull request.

**Here is our `CONTRIBUTING.md` template:**
```markdown
# Contributing to Our Project

Thank you for contributing! To ensure a smooth process, please follow these guidelines.

## Workflow
- All work must be done on a feature branch.
- Never push directly to the `main` branch.
- All changes must be submitted via a Pull Request.
- Ensure your PR is reviewed and approved before merging.

## Commit Messages
- Use the Conventional Commits specification (e.t., `feat:`, `fix:`, `docs:`).


## The PULL_REQUEST_TEMPLATE.md File

## 📝 Description

Please provide a summary of the changes and the problem it solves.
- What is the motivation for this change?
- What is the new behavior?

**Fixes:** # (issue number)


## 🚀 Type of Change

Please check the boxes that apply.

- [ ] 🐛 Bug fix (a non-breaking change which fixes an issue)
- [ ] ✨ New feature (a non-breaking change which adds functionality)
- [ ] 💥 Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] 💅 Refactor (a code change that neither fixes a bug nor adds a feature)
- [ ] 📚 Documentation update
- [ ] ⚙️ Build/CI/CD change
- [ ] ✅ Test update


## 🧪 How to Test This?

Please provide clear, step-by-step instructions for the reviewer to test your changes.
1. `git checkout <branch-name>`
2. `npm install` (or appropriate command)
3. `npm start` (or appropriate command)
4. Go to `http://localhost:3000/...` and verify...
    - [ ] Test case A
    - [ ] Test case B


## 📸 Screenshots / Recordings

If your change affects the UI, please add a screenshot or a short recording to show the new state.

| Before | After |
| ------ | ----- |
|        |       |


## ✅ Self-Review Checklist

Please go through this checklist before you request a review.

- [ ] My code follows the project's style guidelines.
- [ ] I have performed a self-review of my own code.
- [ ] I have commented on any hard-to-understand areas.
- [ ] I have made corresponding changes to the documentation.
- [ ] My changes generate no new warnings or errors.
- [ ] I have added tests that prove my fix is effective or that my feature works.
- [ ] All new and existing unit tests pass locally with my changes.
- [ ] I have checked that there are no hardcoded secrets (API keys, etc.).

