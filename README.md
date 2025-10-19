## Massey University 159251 Course
#### Tutorial 4 - CI with GitHub Actions

### 🚀 Quick Start Guide

This project is set up for the CI tutorial. Follow these steps:

#### 1️⃣ Current Status
- ✅ Test file updated with `testSubtraction` 
- ✅ GitHub Actions workflow configured
- ❌ Bug exists in `Calc.subtract()` method (intentional!)

#### 2️⃣ What to Do
1. Push this code to your GitHub repository
2. Watch the build FAIL on GitHub Actions (take screenshot)
3. Fix the bug in `Calc.java` line 12
4. Push the fix and watch it PASS (take screenshot)
5. Submit screenshots + GitHub URL

#### 📚 Documentation Files
- **`PROJECT_SUMMARY.md`** - Complete overview and submission requirements
- **`TUTORIAL_STEPS.md`** - Detailed step-by-step instructions  
- **`QUICK_COMMANDS.md`** - Git and Maven command reference
- **`VISUAL_CHANGES.md`** - Visual guide of all changes
- **`Calc.java.FIXED`** - Reference for the bug fix

#### 🐛 The Bug
```java
// Current (line 12 in Calc.java)
return x*y;  // Wrong! Multiplies instead of subtracts

// Should be:
return x-y;  // Correct subtraction
```

#### ⚠️ Important
- **DO NOT** fix the bug before first push!
- Repository must be **PUBLIC** for grading
- Take screenshots of both FAILED and PASSED builds

#### 🔗 Next Steps
Start with **`PROJECT_SUMMARY.md`** for the complete tutorial guide!

---

### Project Structure
```
.
├── .github/workflows/build.yml  ← GitHub Actions CI
├── src/
│   ├── main/java/org/example/
│   │   └── Calc.java            ← Contains bug (fix later)
│   └── test/java/org/example/
│       └── CalcTest.java        ← Updated with new test
└── [Documentation files]
```
