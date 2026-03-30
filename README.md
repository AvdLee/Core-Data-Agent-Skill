# Core Data Agent Skill

Expert guidance for any AI coding tool that supports the [Agent Skills open format](https://agentskills.io/home) — safe persistence, performance optimization, and schema migration.

Based on the [Core Data Best Practices](https://github.com/AvdLee/CoreDataBestPractices) repo, WeTransfer production apps, and WWDC sessions, distilled into actionable, concise references for agents.

## Who this is for
- Teams working with Core Data who need safe defaults and quick triage
- Developers debugging persistence issues, threading errors, or performance problems
- Anyone migrating schemas or integrating CloudKit sync

## See also my other skills:
- [Swift Concurrency Expert](https://github.com/AvdLee/Swift-Concurrency-Agent-Skill)
- [SwiftUI Expert](https://github.com/AvdLee/SwiftUI-Agent-Skill)
- [Swift Testing Expert](https://github.com/AvdLee/Swift-Testing-Agent-Skill)

## How to Use This Skill

### Option A: Using skills.sh (recommended)
Install this skill with a single command:
```bash
npx skills add https://github.com/avdlee/core-data-agent-skill --skill core-data-expert
```

For more information, visit the [skills.sh platform page](https://skills.sh/avdlee/core-data-agent-skill/core-data-expert).

Then use the skill in your AI agent, for example:  
> Use the core data skill and analyze the current project for Core Data improvements

### Option B: Claude Code Plugin

#### Personal Usage

To install this Skill for your personal use in Claude Code:

1. Add the marketplace:
   ```bash
   /plugin marketplace add AvdLee/Core-Data-Agent-Skill
   ```

2. Install the Skill:
   ```bash
   /plugin install core-data-expert@core-data-agent-skill
   ```

#### Project Configuration

To automatically provide this Skill to everyone working in a repository, configure the repository's `.claude/settings.json`:

```json
{
  "enabledPlugins": {
    "core-data-expert@core-data-agent-skill": true
  },
  "extraKnownMarketplaces": {
    "core-data-agent-skill": {
      "source": {
        "source": "github",
        "repo": "AvdLee/Core-Data-Agent-Skill"
      }
    }
  }
}
```

When team members open the project, Claude Code will prompt them to install the Skill.

### Option C: Using pi package manager

Install via [pi](https://github.com/badlogic/pi-mono):
```bash
pi install https://github.com/AvdLee/Core-Data-Agent-Skill
```

The skill will be available automatically in pi sessions.

### Option D: Manual install
1) **Clone** this repository.  
2) **Install or symlink** the `core-data-expert/` folder following your tool's official skills installation docs (see links below).  
3) **Use your AI tool** as usual and ask it to use the "core-data-expert" skill for Core Data tasks.

#### Where to Save Skills

Follow your tool's official documentation, here are a few popular ones:
- **Codex:** [Where to save skills](https://developers.openai.com/codex/skills/#where-to-save-skills)
- **Claude:** [Using Skills](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview#using-skills)
- **Cursor:** [Enabling Skills](https://cursor.com/docs/context/skills#enabling-skills)

**How to verify**: 

Your agent should reference the triage/playbook in `core-data-expert/SKILL.md` and jump into the relevant reference file for your error or task.

## What This Skill Offers

This skill gives your AI coding tool comprehensive Core Data guidance. It can:

### Guide Your Persistence Decisions
- Choose the right stack setup (NSPersistentContainer vs NSPersistentCloudKitContainer)
- Understand when to use view context vs background context
- Navigate merge policies and conflict resolution
- Apply proper context configuration for your use case

### Write Thread-Safe Code
- Avoid common threading pitfalls with NSManagedObjectID
- Prevent data races with proper context usage
- Handle cross-context communication correctly
- Use perform vs performAndWait appropriately

### Optimize Performance
- Write efficient fetch requests with proper batching and property limiting
- Reduce memory usage with context resets and faulting control
- Use batch operations for large-scale data changes
- Profile with Instruments to identify bottlenecks

### Migrate Schemas Safely
- Use lightweight migration for common changes
- Decompose complex migrations with staged migration (iOS 17+)
- Defer expensive cleanup with deferred migration (iOS 14+)
- Handle composite attributes and model versioning

### Integrate with CloudKit
- Set up NSPersistentCloudKitContainer correctly
- Design schemas within CloudKit limitations
- Monitor sync with event notifications
- Debug sync issues with system logs

## What Makes This Skill Different

**Expert Knowledge**: Based primarily on the comprehensive [SwiftLee Core Data articles](https://www.avanderlee.com/category/core-data/) and the [Core Data Best Practices repository](https://github.com/AvdLee/CoreDataBestPractices), with additional insights from WWDC sessions. All content reflects real-world experience from production apps like Collect by WeTransfer.

**Non-Opinionated**: Focuses on industry-standard best practices and compile-time safety, not architectural preferences. Works with any Swift project, coding style, or architecture.

**Modern Core Data**: Covers the latest features including:
- Composite attributes (iOS 17+)
- Staged migration (iOS 17+)
- Deferred migration (iOS 14+)
- NSBatchInsertRequest improvements (iOS 14+)
- NSPersistentCloudKitContainer patterns

**Practical & Concise**: Assumes your AI agent is already smart. Focuses on what developers need to know, not what they already understand. Includes code examples for every pattern.

## Skill Structure

```
core-data-expert/
├── SKILL.md                       # Main skill file with decision trees
└── references/
    ├── _index.md                  # Navigation index
    ├── batch-operations.md        # NSBatchInsertRequest, NSBatchDeleteRequest, NSBatchUpdateRequest
    ├── cloudkit-integration.md    # NSPersistentCloudKitContainer, schema design, monitoring
    ├── fetch-requests.md          # Query optimization, NSFetchedResultsController, aggregates
    ├── glossary.md                # Core Data terminology and quick definitions
    ├── migration.md               # Lightweight, staged, and deferred migration strategies
    ├── model-configuration.md     # Constraints, derived attributes, transformables, validation
    ├── performance.md             # Profiling with Instruments, memory management, optimization
    ├── persistent-history.md      # History tracking setup, Observer/Fetcher/Merger/Cleaner
    ├── project-audit.md           # Checklist to discover a project's Core Data setup
    ├── saving.md                  # Conditional saving, hasPersistentChanges, save timing
    ├── stack-setup.md             # NSPersistentContainer setup, merge policies, contexts
    ├── testing.md                 # In-memory stores, shared models, data generators
    └── threading.md               # NSManagedObjectID, perform vs performAndWait, concurrency
```

## Resources

This skill is based primarily on:

- **[SwiftLee Core Data Articles](https://www.avanderlee.com/category/core-data/)** - Comprehensive articles covering Core Data best practices, performance optimization, and real-world implementations
- **[Core Data Best Practices GitHub Repository](https://github.com/AvdLee/CoreDataBestPractices)** - Working code examples demonstrating Core Data best practices

Additional resources:

- **[WWDC 2022-10119: Optimize your use of Core Data and CloudKit](https://developer.apple.com/videos/play/wwdc2022/10119/)** - Performance optimization and CloudKit integration
- **[WWDC 2022-10120: Evolve your Core Data schema](https://developer.apple.com/videos/play/wwdc2022/10120/)** - Schema migration strategies
- **[WWDC 2023-10186: What's new in Core Data](https://developer.apple.com/videos/play/wwdc2023/10186/)** - Composite attributes, staged migration, and deferred migration

## Contributing

Contributions are welcome! This repository follows the [Agent Skills open format](https://agentskills.io/home), which has specific structural requirements.

**We strongly recommend using AI assistance for contributions:**
- Use the [skill-creator skill](https://github.com/anthropics/skills/tree/main/skills/skill-creator) with Claude to ensure proper formatting
- This helps maintain the Agent Skills format and ensures your contribution works correctly with AI agents

**Please read [CONTRIBUTING.md](CONTRIBUTING.md) for:**
- How to use the skill-creator skill for contributions
- Agent Skills format requirements
- Quality standards and best practices
- Pull request process

This skill is maintained to reflect the latest Core Data best practices and will be updated as the framework evolves.

## About the Author

Created by [Antoine van der Lee](https://www.avanderlee.com), a Swift expert with years of experience building production apps with Core Data. He developed the Collect by WeTransfer app for over four years and has [published numerous articles on Core Data](https://www.avanderlee.com/category/core-data/) on his blog called SwiftLee.

## License

This skill is open-source and available under the MIT License. See [LICENSE](LICENSE) for details.
