# Instructions for AI Assistants

> 🤖 **READ THIS FIRST** when starting a new development session

## 📖 Essential Reading Order

When resuming development or starting a new session, read these files in this order:

### 1. DEVELOPMENT_CONTEXT.md (CRITICAL - READ FIRST)
**Location**: `/DEVELOPMENT_CONTEXT.md`
**Purpose**: Complete project history, all decisions, current status
**Contains**:
- Project overview and structure
- Complete development timeline
- All architectural decisions with rationale
- Current progress (X/100 cases)
- Next steps and TODO items
- Technical stack and dependencies
- Known issues and limitations

### 2. ROADMAP.md (For Planning Context)
**Location**: `/docs/ROADMAP.md`
**Purpose**: Understand which phase we're in and what's planned
**Contains**:
- 4-week MVP timeline
- Phase breakdowns
- Success criteria

### 3. CASE_TEMPLATE.md (For Creating Cases)
**Location**: `/CASE_TEMPLATE.md`
**Purpose**: Standard format for all use cases
**Contains**:
- Complete case structure
- All required sections
- Quality checklist

## ⚡ Quick Start Checklist

Before doing anything, confirm:

- [ ] I have read DEVELOPMENT_CONTEXT.md completely
- [ ] I understand the current phase (check "Current Status" section)
- [ ] I know what the last session accomplished (check git log)
- [ ] I understand what needs to be done next (check "Next Steps")
- [ ] I know the repository is PRIVATE (not public yet)
- [ ] I understand all content must be BILINGUAL (EN + CN)

## 🎯 Core Rules

### Repository Rules
1. **Repository is PRIVATE** - Do not assume it's public
2. **All content must be bilingual** - English AND Chinese, no exceptions
3. **Case template is mandatory** - Every case must follow CASE_TEMPLATE.md
4. **Test before commit** - Every prompt needs 3-5 test generations
5. **Update context** - Update DEVELOPMENT_CONTEXT.md before ending session

### File Naming Rules
```
Cases:  [A|I|L]-###-descriptive-name.md
Images: [case-id]-[input|output]-description.jpg
READMEs: README.{lang}.md (ISO 639-1 codes)
```

### Git Commit Rules
- Write clear, descriptive commit messages
- Use the format established in previous commits
- Reference case IDs in commits (e.g., "Add A-002: Elevation to Render")
- Push regularly (every 5-10 cases or significant milestone)

### Quality Standards
Every case MUST include:
1. Problem statement (EN + CN)
2. Complete prompt with {PLACEHOLDERS}
3. Tested parameters
4. High-quality example image (1920px+)
5. Practical tips
6. Related case links

## 📊 Progress Tracking

### Always Update These Counters
In DEVELOPMENT_CONTEXT.md:
- Overall progress: X/100 cases
- Per-category progress: Architecture X/30, Interior X/40, Landscape X/30
- Per-subcategory checklists

In README.md and README.zh-CN.md:
- Update progress badge: "X/100 cases completed"
- Update phase status

## 🔄 End of Session Protocol

Before ending EVERY session:

1. **Update DEVELOPMENT_CONTEXT.md**:
   - [ ] Update "Last Updated" date
   - [ ] Update "Current Status" section
   - [ ] Record new cases in progress checklist
   - [ ] Add any new decisions to "Architecture Decisions"
   - [ ] Update "Next Steps" for next session

2. **Commit Changes**:
   - [ ] Stage all files: `git add -A`
   - [ ] Write clear commit message
   - [ ] Push to GitHub: `git push origin main`

3. **Verify**:
   - [ ] Check GitHub to confirm push succeeded
   - [ ] Verify no uncommitted changes: `git status`

## 🚨 Common Mistakes to Avoid

### DON'T:
- ❌ Skip reading DEVELOPMENT_CONTEXT.md
- ❌ Assume you know the project state without checking
- ❌ Create cases without following template
- ❌ Forget to update progress tracking
- ❌ Commit without bilingual content
- ❌ Push untested prompts
- ❌ Forget to update DEVELOPMENT_CONTEXT.md at end of session

### DO:
- ✅ Read DEVELOPMENT_CONTEXT.md FIRST, ALWAYS
- ✅ Check current phase and TODO items
- ✅ Follow established patterns and conventions
- ✅ Test every prompt 3-5 times
- ✅ Update documentation as you go
- ✅ Commit regularly with clear messages
- ✅ Update DEVELOPMENT_CONTEXT.md before ending

## 📞 User Context

### User: qzh3722
- Prefers Chinese communication
- Uses GitHub Desktop
- Values structured, documented approach
- Quality-focused (not rushing)

### Project Philosophy
- **Quality > Speed** - Take time to do it right
- **Bilingual is critical** - Both EN and CN must be complete
- **Real solutions** - Every case solves actual design problems
- **Professional grade** - Content suitable for design professionals

## 🔧 Technical Context

### Technologies
- Git/GitHub for version control
- Markdown for documentation
- Python PIL/Pillow for image optimization
- No other dependencies (static site)

### File Structure
```
Root files: README files, CONTRIBUTING, LICENSE, templates
/.github/: Issue templates, PR template
/assets/: Images and media
/cases/: 100 use cases (organized by category)
/docs/: User documentation (Getting Started, FAQ, Roadmap)
```

## 📝 Workflow for Creating New Cases

1. **Check DEVELOPMENT_CONTEXT.md** for next case to create
2. **Copy CASE_TEMPLATE.md** to appropriate directory
3. **Name file** following convention: `A-###-descriptive-name.md`
4. **Fill all sections** (EN + CN)
5. **Test prompt** 3-5 times, document parameters
6. **Generate example images** (or use placeholders if workflow not ready)
7. **Update category README** with new case
8. **Update DEVELOPMENT_CONTEXT.md** progress
9. **Commit** with clear message
10. **Push** to GitHub

## 🎓 Learning from History

The DEVELOPMENT_CONTEXT.md contains all important decisions made so far, including:
- Why we use `.jpg` instead of `.png` for banners
- Why `README.zh-CN.md` instead of `README_CN.md`
- Why repository is private during development
- What the 100-case structure looks like
- What quality standards were established

**Don't reinvent decisions** - check if something was already decided and follow the established pattern.

## 🔍 Quick Reference

| Need to know... | Check this file... |
|-----------------|-------------------|
| What was done before | DEVELOPMENT_CONTEXT.md |
| What's next | DEVELOPMENT_CONTEXT.md → "Next Steps" |
| How to format a case | CASE_TEMPLATE.md |
| Project timeline | docs/ROADMAP.md |
| How to contribute | CONTRIBUTING.md |
| File naming | DEVELOPMENT_CONTEXT.md → "Architecture Decisions" |

## 🎯 Success Criteria

You're doing it right if:
- ✅ You read DEVELOPMENT_CONTEXT.md first
- ✅ You follow established patterns
- ✅ All content is bilingual
- ✅ Progress tracking is updated
- ✅ Commits are clear and regular
- ✅ DEVELOPMENT_CONTEXT.md is updated before ending

---

**Remember**: DEVELOPMENT_CONTEXT.md is the single source of truth. When in doubt, check there first!
