# Contributing to Core Data Agent Skill

Thank you for your interest in contributing! This repository contains an **Agent Skill** following the [Agent Skills open format](https://agentskills.io/home), which means it has specific structural requirements beyond typical documentation.

## 🤖 What Are Agent Skills?

Agent Skills are modular capabilities that extend AI agents' functionality. They package instructions, metadata, and resources in a specific format that agents can discover and use automatically. This isn't just documentation—it's a structured skill that AI coding assistants load on-demand.

**Learn more:**
- [Agent Skills Overview](https://agentskills.io/home) - Understanding the format
- [Anthropic's Agent Skills Documentation](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) - Official specification and best practices

## 🎯 Why This Matters

Contributors who aren't familiar with the Agent Skills format may inadvertently:
- Break the YAML frontmatter structure
- Use incorrect markdown formatting that agents can't parse
- Add content that doesn't follow agent-friendly patterns
- Miss important metadata requirements

**That's why we strongly recommend using AI assistance for contributions.**

## ✨ Recommended Contribution Workflow

### Option 1: Use the skill-creator skill (Highly Recommended)

The best way to contribute is to use Claude with the [skill-creator skill](https://github.com/anthropics/skills/tree/main/skills/skill-creator). This ensures your contribution follows the Agent Skills format correctly.

**How to use it:**

1. **Install the skill-creator skill** in your Claude-compatible tool (Claude.ai, Cursor, etc.)
   ```bash
   # If using skills.sh
   npx skills add https://github.com/anthropics/skills --skill skill-creator
   ```

2. **Ask Claude to help with your contribution:**
   ```
   Use the skill-creator skill to help me update the Core Data Agent Skill.
   I want to [describe your contribution].
   ```

3. **Review the generated changes** to ensure technical accuracy for Core Data

4. **Submit your PR** with the AI-generated improvements

**Benefits:**
- ✅ Proper YAML frontmatter structure
- ✅ Agent-friendly markdown formatting
- ✅ Correct file organization
- ✅ Follows best practices from Anthropic's guidelines

### Option 2: Use Claude Without the skill-creator skill

If you don't have access to the skill-creator skill, you can still use Claude (or other AI assistants) to help:

1. **Share the Agent Skills documentation** with Claude:
   - [Agent Skills Overview](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
   - [Best Practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices)

2. **Ask Claude to review your changes** for Agent Skills format compliance

3. **Request that Claude verify:**
   - YAML frontmatter is valid
   - Markdown structure is agent-friendly
   - Content follows progressive disclosure patterns

### Option 3: Manual Contribution

If you prefer to contribute manually, please carefully review:

1. **The Agent Skills specification**: https://agentskills.io/home
2. **Anthropic's best practices**: https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices
3. **Existing file structure** in this repository

**Key requirements:**
- YAML frontmatter must be valid and complete
- Use clear, actionable headings
- Keep instructions concise and agent-friendly
- Follow the existing reference file patterns
- Test your changes with an AI agent if possible

## 📝 Types of Contributions

We welcome contributions in these areas:

### 1. Bug Fixes
- Incorrect Core Data advice
- Outdated code examples
- Broken links or references
- Typos or clarity improvements

### 2. New Reference Content
- Additional Core Data patterns
- New error scenarios and solutions
- iOS 14-17+ feature coverage
- Real-world examples

### 3. SKILL.md Improvements
- Better decision trees
- Clearer triage guidance
- Updated agent behavior rules

### 4. Documentation Updates
- README improvements
- Installation instructions
- Usage examples

## 🎯 Quality Standards

All contributions should meet these standards:

### Core Data Accuracy
- ✅ Follows iOS 14+ best practices
- ✅ Includes working code examples
- ✅ Cites official Apple documentation when relevant
- ✅ Avoids deprecated patterns
- ✅ Considers performance implications
- ✅ Addresses thread safety

### Agent Skills Format Compliance
- ✅ Valid YAML frontmatter (if modifying SKILL.md)
- ✅ Agent-friendly markdown structure
- ✅ Clear, actionable instructions
- ✅ Proper file organization
- ✅ Progressive disclosure (don't overload main SKILL.md)

### Testing
- ✅ Test code examples compile (Swift 6 mode preferred)
- ✅ Verify advice with an AI agent if possible
- ✅ Check that links work

## 🚀 Pull Request Process

1. **Fork the repository** and create a new branch
   ```bash
   git checkout -b feature/your-contribution
   ```

2. **Make your changes** (preferably using the skill-creator skill or Claude)

3. **Test your changes:**
   - Verify code examples compile
   - Check markdown formatting
   - Test with an AI agent if possible

4. **Commit with a clear message:**
   ```bash
   git commit -m "Add guidance for iOS 17 composite attributes"
   ```

5. **Submit a pull request** with:
   - **Clear description** of what you changed and why
   - **Rationale** for the change (link to Apple documentation, real-world scenario, etc.)
   - **Mention if you used skill-creator or Claude** to ensure format compliance
   - **Test results** if applicable

6. **Respond to feedback** - We may request changes to ensure accuracy or format compliance

## 🛠️ Development Setup

To test your changes locally:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/avdlee/core-data-agent-skill.git
   cd core-data-agent-skill
   ```

2. **Install the skill** in your AI tool (see README.md)

3. **Test with your AI agent:**
   ```
   Use the core-data-expert skill and [test your specific change]
   ```

## 📚 Resources

### Agent Skills Documentation
- [Agent Skills Home](https://agentskills.io/home) - Format overview
- [Anthropic's Agent Skills Guide](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) - Official documentation
- [Agent Skills Best Practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices) - Writing effective skills
- [skill-creator skill](https://github.com/anthropics/skills/tree/main/skills/skill-creator) - AI-assisted skill authoring

### Core Data Resources
- [Core Data Best Practices Repository](https://github.com/AvdLee/CoreDataBestPractices) - Comprehensive examples
- [SwiftLee Blog](https://www.avanderlee.com/category/core-data/) - Core Data articles
- [Apple's Core Data Documentation](https://developer.apple.com/documentation/coredata)
- [WWDC Sessions](https://developer.apple.com/videos/frameworks/data-and-storage) - Official Apple guidance

## 🤝 Code of Conduct

- Be respectful and constructive
- Focus on technical accuracy
- Welcome newcomers and help them learn
- Assume good intentions

## ❓ Questions?

- **About Agent Skills format**: See [agentskills.io](https://agentskills.io/home) or [Anthropic's docs](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
- **About Core Data**: Check the [references folder](skills/core-data-expert/references/) or [SwiftLee blog](https://www.avanderlee.com/category/core-data/)
- **About this skill**: Open an issue for discussion

## 📄 License

By contributing, you agree that your contributions will be licensed under the same MIT License that covers this project.

---

**Thank you for helping make Core Data more accessible to AI agents and developers!** 🎉
