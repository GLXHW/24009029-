# Visual Guide: What Has Changed

## 📝 File: CalcTest.java

### ✅ DONE - Added testSubtraction

```diff
package org.example;

import static org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.Test;

public class CalcTest {
  Calc c = new Calc();

    @Test
    void testAddition() {
        assertEquals(4, c.add(2,2));
    }

+   @Test
+   void testSubtraction() {
+       assertEquals(2, c.subtract(4,2));
+   }

}
```

---

## 📝 File: Calc.java

### ❌ TODO - You Need to Fix This Later

**Current (BUGGY) Code:**
```java
package org.example;

public class Calc {

    public int add(int x, int y) {
        return x+y;
    }

    public int subtract(int x, int y) {
        return x*y;  // ❌ BUG: This multiplies instead of subtracts!
    }
}
```

**After Fix (Step 6 in tutorial):**
```java
package org.example;

public class Calc {

    public int add(int x, int y) {
        return x+y;
    }

    public int subtract(int x, int y) {
        return x-y;  // ✅ FIXED: Now correctly subtracts
    }
}
```

**Change Required:** Line 12
```diff
- return x*y;
+ return x-y;
```

---

## 📝 File: .github/workflows/build.yml

### ✅ DONE - GitHub Actions CI Configuration Created

```yaml
name: Java CI with Maven

on:
  push:
    branches: [ main, master ]
  pull_request:
    branches: [ main, master ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v3
    
    - name: Set up JDK 11
      uses: actions/setup-java@v3
      with:
        java-version: '11'
        distribution: 'temurin'
        cache: maven
    
    - name: Build with Maven
      run: mvn clean compile
    
    - name: Run tests
      run: mvn clean test
```

**This file will:**
- ✅ Run automatically on every push to main/master
- ✅ Set up Java 11 environment
- ✅ Compile the code
- ✅ Run all tests
- ❌ FAIL initially (because of subtract bug)
- ✅ PASS after you fix the bug

---

## 📝 File: .gitignore

### ✅ DONE - Created to Ignore Build Artifacts

```gitignore
# Maven
target/
pom.xml.tag
pom.xml.releaseBackup
pom.xml.versionsBackup
pom.xml.next
release.properties
dependency-reduced-pom.xml
buildNumber.properties
.mvn/timing.properties

# IDE
.idea/
*.iml
.vscode/
.settings/
.classpath
.project

# OS
.DS_Store
Thumbs.db
```

---

## 🎬 Expected GitHub Actions Results:

### First Push (with bug):
```
❌ Run tests - FAILED
   java.lang.AssertionError: expected: <2> but was: <8>
   at CalcTest.testSubtraction(CalcTest.java:16)
```

### After Fix:
```
✅ Run tests - PASSED
   Tests run: 2, Failures: 0, Errors: 0, Skipped: 0
```

---

## 📸 Screenshots You Need:

### Screenshot 1: Failed Build
```
GitHub → Actions tab → Click on failed workflow run
Should show: ❌ Red X with error message about testSubtraction
```

### Screenshot 2: Build History
```
GitHub → Actions tab → Workflow runs list
Should show:
  ✅ Fix subtract method to return correct result
  ❌ Initial commit with failing test
```

### Screenshot 3: Commits with Status
```
GitHub → Repository main page → Commits
Should show each commit with green ✅ or red ❌ icon
```

---

## 🔄 Complete Workflow:

```
1. Write Test (testSubtraction)                    ✅ DONE
   ↓
2. Test Fails Locally (subtract returns 8, not 2) ⏸️ YOUR TURN
   ↓
3. Push to GitHub                                  ⏸️ YOUR TURN
   ↓
4. CI Detects Failure ❌                          ⏸️ YOUR TURN
   ↓
5. Fix Bug (change x*y to x-y)                    ⏸️ YOUR TURN
   ↓
6. Test Passes Locally                             ⏸️ YOUR TURN
   ↓
7. Push Fix to GitHub                              ⏸️ YOUR TURN
   ↓
8. CI Detects Success ✅                          ⏸️ YOUR TURN
   ↓
9. Take Screenshots & Submit                       ⏸️ YOUR TURN
```

---

## 💡 Tips:

1. **Don't fix the bug before the first push!** The tutorial requires you to see a failing build first.

2. **Use IntelliJ's Maven tool** if Maven is not in your PATH:
   - View → Tool Windows → Maven
   - Expand Lifecycle → Double-click "test"

3. **Quick fix**: When ready to fix, just replace the content of `Calc.java` with the content from `Calc.java.FIXED`!

4. **Check Actions early**: After your first push, immediately go to the Actions tab to ensure the workflow starts.

5. **Repository visibility**: Confirm it's PUBLIC in Settings → General → Danger Zone

---

Good luck! 🎓

