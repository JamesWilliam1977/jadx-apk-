```markdown
# jadx-apk- Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `jadx-apk-` Java codebase. You'll learn about file naming, import/export styles, commit conventions, and how to write and organize tests. This guide is ideal for contributors looking to maintain consistency and efficiency when working on this repository.

## Coding Conventions

### File Naming
- **Pattern:** camelCase
- **Example:**  
  ```java
  // Good
  public class ApkParser { ... }
  
  // Bad
  public class apk_parser { ... }
  ```

### Import Style
- **Pattern:** Relative imports are used.
- **Example:**  
  ```java
  import com.example.jadxapk.utils.StringUtils;
  ```

### Export Style
- **Pattern:** Named exports (explicit class names).
- **Example:**  
  ```java
  public class ApkUtils { ... }
  ```

### Commit Message Convention
- **Type:** Conventional commits
- **Prefixes:** `test`, `chore`
- **Average length:** ~51 characters
- **Example:**  
  ```
  test: add unit tests for ApkParser edge cases
  chore: update dependencies to latest versions
  ```

## Workflows

### Creating a Test
**Trigger:** When adding new features or fixing bugs  
**Command:** `/create-test`

1. Create a new test file following the `*.test.*` pattern (e.g., `ApkParser.test.java`).
2. Write test cases covering the new or changed functionality.
3. Use the same import and export conventions as production code.
4. Commit with a message starting with `test:`.

### Chore or Maintenance Tasks
**Trigger:** When performing non-feature tasks (e.g., dependency updates)  
**Command:** `/chore-task`

1. Make the necessary maintenance changes.
2. Commit with a message starting with `chore:`.
3. Ensure no production logic is unintentionally altered.

## Testing Patterns

- **Framework:** Unknown (refer to existing test files for structure)
- **File Pattern:** Test files are named with `.test.` in the filename (e.g., `ApkParser.test.java`).
- **Example:**
  ```java
  // ApkParser.test.java
  import org.junit.Test;
  import static org.junit.Assert.*;

  public class ApkParserTest {
      @Test
      public void testParseValidApk() {
          // test logic here
      }
  }
  ```
- **Placement:** Tests are typically placed alongside or near the code they test.

## Commands
| Command         | Purpose                                         |
|-----------------|-------------------------------------------------|
| /create-test    | Scaffold a new test file for a feature or bug   |
| /chore-task     | Start a maintenance or chore commit             |
```
