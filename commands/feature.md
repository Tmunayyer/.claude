---
description: "Feature development command that enforces git branching best practices and proactive subagent usage. Creates a feature branch from the default branch and analyzes which agents would be helpful for the task."
allowed-tools: ["Read", "Glob", "Bash", "Task"]
---

FEATURE DEVELOPMENT WORKFLOW

Task: "$ARGUMENTS"

**CRITICAL WORKFLOW ENFORCEMENT:**
This command MUST be executed in the following order without deviation:

## STEP 1: GIT BRANCH MANAGEMENT
**MANDATORY**: Before making ANY code changes, execute the following git workflow:

First, let me check the current git status and identify the default branch:
!git status
!git branch -a
!git symbolic-ref refs/remotes/origin/HEAD | cut -d'/' -f4 || echo "main"

Based on the output above, I will now:

1. **Switch to Default Branch**:
!git checkout main || git checkout master

2. **Pull Latest Changes**:
!git pull origin main || git pull origin master

3. **Create Feature Branch**:
Generate a descriptive branch name based on the task.
!git checkout -b "feature/$(date +%m%d-%H%M)-$(echo "$ARGUMENTS" | tr ' ' '-' | tr '[:upper:]' '[:lower:]' | sed 's/[^a-z0-9-]//g' | cut -c1-30)"

**CRITICAL**: Feature branch has been created. Proceeding to agent analysis.

## STEP 2: SUBAGENT ANALYSIS & SELECTION
**MANDATORY**: Before implementing the feature, I will analyze and select appropriate subagents:

### Scanning for Available Agents

**Global Claude Agents**:
!ls -la ~/.claude/agents/ 2>/dev/null || echo "No global agents directory found"

**Project-Specific Agents**:
!pwd
!ls -la ./.claude/agents/ 2>/dev/null || echo "No project-specific agents found"
!ls -la ./agents/ 2>/dev/null || echo "No agents directory in current project"

### Dynamic Agent Discovery

Based on the agents found above, I will now:
1. List all available global agents from ~/.claude/agents/
2. List all project-specific agents from current directory
3. Analyze which agents are most suitable for the task "$ARGUMENTS"

**Task Analysis**:
Based on the task description, I will identify:
- Task Type (Frontend/Backend/Mobile/Full-stack/Infrastructure)
- Complexity Level (Simple/Medium/Complex)
- Special Requirements (Performance/Security/UX/Testing)
- Project-Specific Needs (based on project agents found)

**Common Global Agents** (if available):
- `frontend-developer`: UI components, React/Vue/Angular, state management, responsive design
- `mobile-app-builder`: Native iOS/Android, React Native, mobile-specific features
- `rapid-prototyper`: Quick MVPs, proof-of-concepts, trending features
- `claude-code-command-expert`: Command creation and workflow automation
- `meta-agent`: Creating new sub-agents for specialized tasks

**Project-Specific Agents** (dynamically discovered):
[Will be populated based on what's found in the project directory]

**Agent Selection Strategy**:
I will proactively use the most appropriate agent(s) based on:
1. **Priority 1**: Project-specific agents that match the task (highest priority as they know the codebase)
2. **Priority 2**: Global specialized agents that match the task type
3. **Priority 3**: Meta-agent to create a new specialized agent if no good match exists
4. **Priority 4**: Standard tools with careful planning if no agents apply

The selection will be based on:
- Task requirements and complexity
- Agent descriptions and capabilities
- Project context and existing patterns

## STEP 3: IMPLEMENTATION PLANNING

Before proceeding, I'll create a comprehensive implementation plan using the TodoWrite tool to track all tasks:

1. Understand existing codebase patterns
2. Identify files to create/modify
3. Plan test strategy
4. Implement core functionality
5. Write/update tests
6. Verify everything works

## STEP 4: FEATURE IMPLEMENTATION

Now executing the feature development using the selected agent(s) or standard tools:

If a specialized agent matches the task, I will use:
!/agents [selected-agent] Implement: $ARGUMENTS

Otherwise, I will proceed with standard implementation following these principles:
- Study existing code patterns first
- Write tests before implementation when possible
- Make incremental, working commits
- Follow project conventions
- Ensure all tests pass

## STEP 5: QUALITY ASSURANCE & COMPLETION

**Pre-Completion Checklist**:
- [ ] Feature branch created from default branch
- [ ] Appropriate agents used when applicable
- [ ] Implementation follows project conventions
- [ ] Tests written and passing
- [ ] Code formatted and linted
- [ ] No TODO comments without issue numbers
- [ ] Commits have clear messages

**Final Status Check**:
!git status
!git log --oneline -n 5

**Next Steps**:
Ready to create pull request from current feature branch to the default branch.

**ERROR RECOVERY**:
If any step fails:
1. Document what failed with specific error messages
2. Analyze root cause
3. Fix properly without forcing
4. Maximum 3 attempts per issue, then reassess approach

This workflow ensures proper branching, proactive agent usage, and high-quality feature development.