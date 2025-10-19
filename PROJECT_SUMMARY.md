# Tutorial 4 - CI Setup Summary

## ✅ Completed Setup

### 1. Project Files Created/Modified:

#### Modified Files:
- **`src/test/java/org/example/CalcTest.java`**
  - ✅ Added `testSubtraction()` test method
  - Tests that `subtract(4, 2)` returns `2`
  - **This test will FAIL** with current code (returns 8 instead of 2)

#### New Files Created:
- **`.github/workflows/build.yml`**
  - GitHub Actions CI configuration
  - Runs on push/PR to main/master branch
  - Sets up Java 11 and runs Maven tests
  
- **`.gitignore`**
  - Ignores Maven target directory and IDE files

- **`Calc.java.FIXED`**
  - Fixed version of Calc.java for reference
  - Line 12 changed from `return x*y;` to `return x-y;`

- **`TUTORIAL_STEPS.md`**
  - Detailed step-by-step instructions

- **`QUICK_COMMANDS.md`**
  - Quick reference for Git and Maven commands

### 2. Current Bug Status:
❌ **`src/main/java/org/example/Calc.java` line 12**
```java
public int subtract(int x, int y) {
    return x*y;  // BUG: Should be x-y
}
```

## 📋 What You Need to Do Next:

### Step 1: Install Prerequisites
If not already installed:
- **Git**: https://git-scm.com/download/win
- **Maven**: Use IntelliJ's built-in Maven or download from https://maven.apache.org/

### Step 2: Test Locally (Optional but Recommended)
```bash
cd "F:\10月项目\新建文件夹 (6)\tutorial4-main\tutorial4-main"
mvn clean test
```
Expected: Build FAILS with testSubtraction error

### Step 3: Create GitHub Repository
1. Go to https://github.com/new
2. Repository name: `tutorial4` (or your choice)
3. Set to **PUBLIC** ⚠️ (Required for submission)
4. Do NOT initialize with README
5. Click "Create repository"

### Step 4: Push to GitHub
```bash
cd "F:\10月项目\新建文件夹 (6)\tutorial4-main\tutorial4-main"
git init
git add .
git commit -m "Initial commit with failing test"
git remote add origin https://github.com/YOUR-USERNAME/tutorial4.git
git branch -M main
git push -u origin main
```

### Step 5: Watch Build Fail on GitHub Actions
1. Go to your repository on GitHub
2. Click "Actions" tab
3. Watch the build fail (red ❌)
4. **📸 SCREENSHOT 1**: Capture the failed build

### Step 6: Fix the Bug
Edit `src/main/java/org/example/Calc.java` line 12:
```java
// Change from:
return x*y;

// To:
return x-y;
```

**Quick way**: Copy contents from `Calc.java.FIXED` file!

### Step 7: Test Fix Locally (Optional)
```bash
mvn clean test
```
Expected: Both tests PASS ✅

### Step 8: Push the Fix
```bash
git add src/main/java/org/example/Calc.java
git commit -m "Fix subtract method to return correct result"
git push
```

### Step 9: Watch Build Succeed
1. Go back to GitHub Actions tab
2. Watch the new build succeed (green ✅)
3. **📸 SCREENSHOT 2**: Capture both failed and successful builds
4. **📸 SCREENSHOT 3**: Go to repository main page, show commits with status icons

## 📤 What to Submit on Stream:

1. **Screenshot 1**: Failed build details from GitHub Actions
2. **Screenshot 2**: Build history showing both failed and successful workflows
3. **Screenshot 3**: Commits page with status indicators
4. **GitHub URL**: Link to your public repository

Example URL format: `https://github.com/YOUR-USERNAME/tutorial4`

## 📁 Final Project Structure:
```
tutorial4-main/
├── .github/
│   └── workflows/
│       └── build.yml          ← CI configuration
├── .gitignore                 ← Git ignore file
├── pom.xml                    ← Maven configuration
├── src/
│   ├── main/
│   │   └── java/
│   │       └── org/
│   │           └── example/
│   │               └── Calc.java          ← HAS BUG (to fix later)
│   └── test/
│       └── java/
│           └── org/
│               └── example/
│                   └── CalcTest.java      ← Updated with testSubtraction
├── Calc.java.FIXED            ← Reference for the fix
├── TUTORIAL_STEPS.md          ← Detailed instructions
├── QUICK_COMMANDS.md          ← Command reference
└── PROJECT_SUMMARY.md         ← This file
```

## 🎯 Learning Objectives Achieved:
- ✅ Understanding CI/CD concepts
- ✅ Setting up GitHub Actions workflow
- ✅ Writing unit tests with JUnit 5
- ✅ Using Maven for build automation
- ✅ Git workflow: commit, push, observe CI
- ✅ Intentional test failures and fixes
- ✅ Observing CI feedback loop

## ⚠️ Important Notes:
1. Repository MUST be PUBLIC for grading
2. Take screenshots BEFORE and AFTER fixing the bug
3. Make sure .github/workflows/build.yml is committed
4. Verify Actions tab shows workflow runs

Good luck with your tutorial! 🚀

