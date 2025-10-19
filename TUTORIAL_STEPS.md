# Tutorial 4 - CI Setup Steps

## Current Status
✅ Test file updated with `testSubtraction` test case
✅ GitHub Actions workflow file created (`.github/workflows/build.yml`)
❌ `subtract` method still has bug (returns `x*y` instead of `x-y`)

## Steps to Complete the Tutorial

### Step 1: Verify Maven Build Fails with Current Code
Since you don't have Maven in your PATH from the command line, you can:
- Use IntelliJ IDEA's Maven tool window (right sidebar) to run: `clean test`
- Or install Maven and add it to PATH, then run: `mvn clean test`

**Expected Result:** The build should FAIL because `testSubtraction` expects `subtract(4,2)` to return `2`, but it returns `8` (4*2).

### Step 2: Initialize Git Repository and Push to GitHub

1. Open terminal in the `tutorial4-main` directory
2. Initialize Git (if not already done):
   ```bash
   git init
   git add .
   git commit -m "Initial commit with failing test"
   ```

3. Create a new repository on GitHub:
   - Go to https://github.com/new
   - Name it `tutorial4` (or any name you prefer)
   - DO NOT initialize with README
   - Make sure it's set to **PUBLIC**

4. Add remote and push:
   ```bash
   git remote add origin https://github.com/YOUR-USERNAME/tutorial4.git
   git branch -M main
   git push -u origin main
   ```

### Step 3: Watch the Build Fail on GitHub Actions
1. Go to your GitHub repository
2. Click on the "Actions" tab
3. You should see a workflow run starting automatically
4. Click on it to watch it fail (red X)
5. **TAKE SCREENSHOT 1:** The failed build in Actions

### Step 4: Fix the subtract Method
Open `src/main/java/org/example/Calc.java` and change line 12:

**FROM:**
```java
return x*y;
```

**TO:**
```java
return x-y;
```

### Step 5: Verify Tests Pass Locally
Run Maven tests again:
```bash
mvn clean test
```

**Expected Result:** Both tests should now PASS ✅

### Step 6: Commit and Push the Fix
```bash
git add .
git commit -m "Fix subtract method to return correct subtraction result"
git push
```

### Step 7: Watch the Build Succeed on GitHub Actions
1. Go back to your GitHub repository's Actions tab
2. You should see a new workflow run
3. This time it should succeed (green checkmark ✅)
4. **TAKE SCREENSHOT 2:** Showing both the failed and successful builds

### Step 8: Get the Workflow Status
Go to your repository main page and you should see:
- A list of commits
- Each commit will have a status icon (✅ for success, ❌ for failure)

**TAKE SCREENSHOT 3:** Showing the commits with their build statuses

## What to Submit
1. Screenshot 1: Failed build in GitHub Actions
2. Screenshot 2: Build history showing both failed and successful builds
3. Screenshot 3: Commits page showing which commits passed/failed
4. GitHub repository URL (make sure it's PUBLIC)

## Files Modified/Created
- `src/test/java/org/example/CalcTest.java` - Added testSubtraction test
- `.github/workflows/build.yml` - GitHub Actions CI configuration
- `src/main/java/org/example/Calc.java` - TO BE FIXED: Change line 12 from `x*y` to `x-y`

