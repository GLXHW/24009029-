# Quick Commands for Tutorial 4

## If you need to install Maven:
1. Download from: https://maven.apache.org/download.cgi
2. Extract and add to PATH
3. Or use IntelliJ's built-in Maven (recommended)

## Git Commands (run in tutorial4-main directory)

### Initial Setup:
```bash
cd tutorial4-main
git init
git add .
git commit -m "Initial commit with failing test"
```

### Create GitHub Repo and Push:
```bash
# After creating repo on GitHub (https://github.com/new)
git remote add origin https://github.com/YOUR-USERNAME/tutorial4.git
git branch -M main
git push -u origin main
```

### After Fixing the Code:
```bash
git add src/main/java/org/example/Calc.java
git commit -m "Fix subtract method to return correct result"
git push
```

## Maven Commands:
```bash
# Run tests
mvn clean test

# Just compile
mvn clean compile

# Clean build
mvn clean
```

## IntelliJ Maven (if Maven not in PATH):
1. Open Maven tool window (View > Tool Windows > Maven)
2. Expand Lifecycle
3. Double-click: clean, then test

## Fix the Bug:
In `src/main/java/org/example/Calc.java` line 12:
- Change: `return x*y;`
- To: `return x-y;`

Or simply copy the contents from `Calc.java.FIXED` file!

