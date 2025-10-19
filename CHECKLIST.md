# Tutorial 4 - Submission Checklist ✓

Use this checklist to ensure you complete all requirements!

## 📋 Pre-Submission Checklist

### Prerequisites
- [ ] Git installed and accessible from command line
- [ ] Maven installed (or using IntelliJ's built-in Maven)
- [ ] GitHub account created
- [ ] Reviewed the tutorial requirements

### Phase 1: Initial Setup (with bug)
- [ ] Project files reviewed and understood
- [ ] Identified the bug in `Calc.java` line 12 (returns `x*y` instead of `x-y`)
- [ ] **NOT FIXED YET** - Keep the bug for now!
- [ ] Created a new **PUBLIC** repository on GitHub named `tutorial4`
- [ ] Initialized Git in the project directory
  ```bash
  git init
  ```
- [ ] Added all files to Git
  ```bash
  git add .
  ```
- [ ] Made initial commit
  ```bash
  git commit -m "Initial commit with failing test"
  ```
- [ ] Added remote repository
  ```bash
  git remote add origin https://github.com/YOUR-USERNAME/tutorial4.git
  ```
- [ ] Pushed to GitHub
  ```bash
  git branch -M main
  git push -u origin main
  ```

### Phase 2: Observe Failing CI Build
- [ ] Went to GitHub repository in browser
- [ ] Clicked on "Actions" tab
- [ ] Verified workflow started automatically
- [ ] Waited for workflow to complete
- [ ] Confirmed build **FAILED** (red ❌)
- [ ] Clicked on the failed workflow to see details
- [ ] Saw error: `expected: <2> but was: <8>` in testSubtraction
- [ ] **📸 SCREENSHOT 1 TAKEN**: Failed build details from Actions tab

### Phase 3: Fix the Bug
- [ ] Opened `src/main/java/org/example/Calc.java`
- [ ] Located line 12 in the `subtract` method
- [ ] Changed from: `return x*y;`
- [ ] Changed to: `return x-y;`
- [ ] Saved the file
- [ ] (Optional) Ran tests locally to verify fix:
  ```bash
  mvn clean test
  ```
- [ ] Confirmed both tests now pass locally

### Phase 4: Observe Passing CI Build
- [ ] Staged the fixed file
  ```bash
  git add src/main/java/org/example/Calc.java
  ```
- [ ] Committed the fix
  ```bash
  git commit -m "Fix subtract method to return correct result"
  ```
- [ ] Pushed to GitHub
  ```bash
  git push
  ```
- [ ] Went back to Actions tab on GitHub
- [ ] Verified new workflow started
- [ ] Waited for workflow to complete
- [ ] Confirmed build **PASSED** (green ✅)
- [ ] **📸 SCREENSHOT 2 TAKEN**: Build history showing both failed and successful runs

### Phase 5: Document Commit History
- [ ] Went to repository main page
- [ ] Clicked on "Commits" or commit history
- [ ] Verified both commits are visible
- [ ] Confirmed status icons appear next to each commit:
  - ❌ Red X for "Initial commit with failing test"
  - ✅ Green checkmark for "Fix subtract method..."
- [ ] **📸 SCREENSHOT 3 TAKEN**: Commits page with status indicators

### Phase 6: Prepare Submission
- [ ] Verified repository is set to **PUBLIC**
  - Settings → General → Scroll to "Danger Zone"
  - Check visibility status
- [ ] Copied repository URL (example: `https://github.com/YOUR-USERNAME/tutorial4`)
- [ ] Have all 3 screenshots ready:
  1. Failed build details
  2. Build history with both runs
  3. Commits with status indicators
- [ ] Screenshots are clear and readable
- [ ] Screenshots show relevant information (not cropped too much)

### Phase 7: Final Verification
- [ ] Repository URL is correct and accessible
- [ ] Repository is PUBLIC (anyone can view without login)
- [ ] All commits are visible on GitHub
- [ ] GitHub Actions workflow file (`.github/workflows/build.yml`) is present
- [ ] Latest commit shows green checkmark (passing build)
- [ ] Both test cases are in `CalcTest.java`
- [ ] Bug is fixed in `Calc.java`

### Phase 8: Submit on Stream
- [ ] Logged into Stream submission system
- [ ] Found Tutorial 4 submission link
- [ ] Uploaded Screenshot 1 (failed build)
- [ ] Uploaded Screenshot 2 (build history)
- [ ] Uploaded Screenshot 3 (commits with status)
- [ ] Pasted GitHub repository URL
- [ ] Reviewed submission
- [ ] Submitted before deadline

## 📊 Expected Results Summary

### Initial Push (with bug):
```
Commit: "Initial commit with failing test"
Status: ❌ FAILED
Error: testSubtraction - expected: <2> but was: <8>
```

### After Fix:
```
Commit: "Fix subtract method to return correct result"
Status: ✅ PASSED
Tests run: 2, Failures: 0, Errors: 0
```

## ⚠️ Common Issues & Solutions

### Issue: Git not found
**Solution**: Install Git from https://git-scm.com/download/win and restart terminal

### Issue: Maven not found
**Solution**: Use IntelliJ's Maven tool window or install Maven from https://maven.apache.org/

### Issue: GitHub Actions not running
**Solution**: Check that `.github/workflows/build.yml` was pushed to repository

### Issue: Build passes on first push
**Solution**: You may have already fixed the bug! Revert the fix, push, then fix again.

### Issue: Repository is private
**Solution**: Go to Settings → General → Danger Zone → Change visibility → Make public

### Issue: Can't find Actions tab
**Solution**: Make sure you're on your repository's main page, then look for tabs near the top

### Issue: Tests pass locally but fail on CI
**Solution**: Check Java version - CI uses Java 11, make sure your code is compatible

### Issue: Tests fail locally but pass on CI
**Solution**: This shouldn't happen - verify you saved all files before committing

## 📝 Submission Checklist

Before submitting, verify you have:

1. ✅ Screenshot showing failed build details
2. ✅ Screenshot showing build history (failed + successful)
3. ✅ Screenshot showing commits with status icons
4. ✅ GitHub repository URL
5. ✅ Repository is PUBLIC
6. ✅ Latest build is passing

## 🎯 Grading Criteria

Your submission will be evaluated on:
- ✓ GitHub Actions workflow configured correctly
- ✓ Evidence of failed build (screenshot)
- ✓ Evidence of successful build after fix (screenshot)
- ✓ Commit history shows both states (screenshot)
- ✓ Repository is public and accessible
- ✓ Tests are properly implemented
- ✓ Bug fix is correct

## 🎓 Learning Outcomes

By completing this tutorial, you have:
- ✓ Set up a CI/CD pipeline using GitHub Actions
- ✓ Written unit tests with JUnit 5
- ✓ Used Maven for build automation
- ✓ Experienced the Git workflow with CI
- ✓ Observed test-driven development practices
- ✓ Debugged code based on CI feedback

---

Good luck with your submission! 🚀

**Questions?** Review the documentation files:
- `PROJECT_SUMMARY.md` - Complete overview
- `TUTORIAL_STEPS.md` - Detailed instructions
- `VISUAL_CHANGES.md` - Visual guide
- `QUICK_COMMANDS.md` - Command reference

