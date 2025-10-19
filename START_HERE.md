# 🎯 START HERE - Tutorial 4 Guide

## Welcome! 👋

This project has been prepared for your **Tutorial 4 - Continuous Integration** assignment.

### 🚦 Quick Decision Guide

**Choose your path:**

#### 📖 If you want detailed instructions:
→ Start with **`TUTORIAL_STEPS.md`**

#### 📋 If you want a step-by-step checklist:
→ Use **`CHECKLIST.md`**

#### 🎨 If you want to see what changed:
→ Read **`VISUAL_CHANGES.md`**

#### ⚡ If you just want quick commands:
→ Check **`QUICK_COMMANDS.md`**

#### 📊 If you want a complete overview:
→ Read **`PROJECT_SUMMARY.md`**

---

## 🎬 TL;DR - What You Need to Do

1. **Push this code to GitHub** (it has a bug, that's intentional!)
2. **Watch it fail** on GitHub Actions (take screenshot 📸)
3. **Fix the bug** in `Calc.java` line 12
4. **Push the fix** to GitHub
5. **Watch it pass** on GitHub Actions (take screenshot 📸)
6. **Take one more screenshot** of your commits
7. **Submit** screenshots + GitHub URL on Stream

**Time needed:** ~30 minutes

---

## 📚 Documentation Files Overview

| File | Purpose | When to Use |
|------|---------|-------------|
| **START_HERE.md** | This file - navigation guide | First time opening project |
| **README.md** | Quick overview and status | Quick reference |
| **TUTORIAL_STEPS.md** | Complete step-by-step guide | Following tutorial for first time |
| **CHECKLIST.md** | Interactive checklist | Making sure you don't miss anything |
| **VISUAL_CHANGES.md** | Visual diff of all changes | Understanding what was modified |
| **PROJECT_SUMMARY.md** | Comprehensive summary | Getting complete picture |
| **QUICK_COMMANDS.md** | Git & Maven commands | Quick command reference |
| **Calc.java.FIXED** | Fixed version of Calc.java | Reference when fixing bug |

---

## ⚡ Super Quick Start (for experienced users)

```bash
# 1. Push to GitHub (with bug)
git init
git add .
git commit -m "Initial commit with failing test"
git remote add origin https://github.com/YOUR-USERNAME/tutorial4.git
git branch -M main
git push -u origin main

# 2. Go to GitHub → Actions → Watch build FAIL → Take screenshot

# 3. Fix Calc.java line 12: change "x*y" to "x-y"

# 4. Push fix
git add src/main/java/org/example/Calc.java
git commit -m "Fix subtract method to return correct result"
git push

# 5. Go to GitHub → Actions → Watch build PASS → Take screenshots

# 6. Submit on Stream
```

---

## 🎯 Current Project Status

### ✅ What's Already Done:
- Test file updated with `testSubtraction` test
- GitHub Actions workflow configured (`.github/workflows/build.yml`)
- All documentation created
- `.gitignore` configured

### ❌ What Has a Bug (Intentional!):
- `src/main/java/org/example/Calc.java` line 12
- Currently: `return x*y;`
- Should be: `return x-y;`
- **Don't fix this until AFTER your first GitHub push!**

---

## 📸 Screenshots You Need

### Screenshot 1: Failed Build
**When:** After first push to GitHub
**Where:** GitHub → Actions tab → Click on failed workflow
**Show:** Red X, error details about testSubtraction

### Screenshot 2: Build History
**When:** After pushing the fix
**Where:** GitHub → Actions tab → Workflow runs list
**Show:** Both failed and successful builds

### Screenshot 3: Commits with Status
**When:** After pushing the fix
**Where:** GitHub → Repository main page → Commits
**Show:** Commits with ❌ and ✅ icons

---

## 🛠️ Prerequisites

### Required:
- **Git**: https://git-scm.com/download/win
- **GitHub Account**: https://github.com/join
- **Maven** or IntelliJ IDEA (with Maven plugin)

### Check if installed:
```bash
git --version
mvn --version
```

---

## ⚠️ Important Reminders

1. **DO NOT FIX THE BUG** before your first push!
2. Repository **MUST BE PUBLIC** for grading
3. Take screenshots at **each stage**
4. **Submit before the deadline** (penalties apply)
5. Include **GitHub URL** in your submission

---

## 🐛 The Bug Explained

**File:** `src/main/java/org/example/Calc.java`

**Current code (line 12):**
```java
public int subtract(int x, int y) {
    return x*y;  // ❌ This multiplies! Bug!
}
```

**The test expects:**
```java
assertEquals(2, c.subtract(4, 2));  // Expects 4 - 2 = 2
```

**What actually happens:**
```
4 * 2 = 8  // ❌ Wrong!
```

**After fix:**
```java
public int subtract(int x, int y) {
    return x-y;  // ✅ This subtracts correctly
}
```

---

## 🎓 Learning Objectives

This tutorial teaches you:
- ✓ Setting up CI/CD with GitHub Actions
- ✓ Writing unit tests with JUnit 5
- ✓ Using Maven for builds
- ✓ Git workflow with CI integration
- ✓ Test-driven development
- ✓ Debugging with CI feedback

---

## 🆘 Need Help?

### For detailed instructions:
→ Read **`TUTORIAL_STEPS.md`**

### For step-by-step checklist:
→ Use **`CHECKLIST.md`**

### For command reference:
→ Check **`QUICK_COMMANDS.md`**

### Common issues:
→ See "Common Issues & Solutions" in **`CHECKLIST.md`**

---

## 🚀 Ready to Start?

### Recommended path:
1. Read this file (✅ you're here!)
2. Open **`TUTORIAL_STEPS.md`** for detailed guide
3. Keep **`QUICK_COMMANDS.md`** open for reference
4. Use **`CHECKLIST.md`** to track progress

### Fast path (experienced):
1. Review "Super Quick Start" above
2. Follow the commands
3. Use **`CHECKLIST.md`** to verify completion

---

## 📊 Submission Requirements

Submit on Stream:
- ✓ Screenshot 1: Failed build details
- ✓ Screenshot 2: Build history (failed + successful)
- ✓ Screenshot 3: Commits with status icons
- ✓ GitHub repository URL (must be PUBLIC)

**Deadline:** Check Stream for exact deadline
**Penalty:** 10% per day late

---

## 🎯 Success Criteria

Your submission is complete when:
- ✅ GitHub repository is public
- ✅ GitHub Actions workflow runs automatically
- ✅ You have evidence of failed build
- ✅ You have evidence of successful build
- ✅ Both commits are visible with status icons
- ✅ All screenshots are clear and complete
- ✅ GitHub URL is submitted

---

## 🎉 Good Luck!

You've got this! Follow the steps, take your screenshots, and submit on time.

**Need more details?** → Open **`TUTORIAL_STEPS.md`**

**Want to track progress?** → Use **`CHECKLIST.md`**

**Quick commands needed?** → Check **`QUICK_COMMANDS.md`**

---

*Last updated: Tutorial 4 setup complete*
*All code changes implemented, ready for Git workflow*

