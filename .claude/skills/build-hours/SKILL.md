```markdown
# build-hours Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `build-hours` TypeScript codebase. It covers file organization, import/export styles, commit message habits, and testing patterns. By following these guidelines, contributors can maintain consistency and quality throughout the project.

## Coding Conventions

### File Naming
- **Style:** kebab-case
- **Example:**  
  ```
  user-service.ts
  build-hours-utils.ts
  ```

### Import Style
- **Relative imports are used throughout the codebase.**
- **Example:**
  ```typescript
  import { calculateHours } from './utils/calculate-hours';
  ```

### Export Style
- **Named exports are preferred.**
- **Example:**
  ```typescript
  // In utils/calculate-hours.ts
  export function calculateHours(...) { ... }
  ```

### Commit Patterns
- **Freeform commit messages (no strict prefixes)**
- **Average length:** ~54 characters
- **Example:**  
  ```
  Add new calculation for overtime hours
  ```

## Workflows

### Adding a New Feature
**Trigger:** When implementing new functionality  
**Command:** `/add-feature`

1. Create a new file using kebab-case naming (e.g., `feature-name.ts`).
2. Implement the feature using TypeScript.
3. Use relative imports for any dependencies.
4. Export functions or constants using named exports.
5. Write corresponding tests in a `*.test.ts` file.
6. Commit your changes with a clear, concise message.

### Refactoring Existing Code
**Trigger:** When improving or restructuring code  
**Command:** `/refactor`

1. Identify the code to refactor.
2. Update file names to kebab-case if needed.
3. Change imports to relative if not already.
4. Ensure all exports are named.
5. Update or add tests as necessary.
6. Commit with a descriptive message.

### Writing Tests
**Trigger:** When adding or updating tests  
**Command:** `/write-test`

1. Create a test file matching `*.test.ts` pattern (e.g., `calculate-hours.test.ts`).
2. Write tests for all exported functions.
3. Use the project's preferred testing framework (unknown; check existing tests for style).
4. Run tests to verify correctness.
5. Commit with a message describing the test coverage.

## Testing Patterns

- **Test files use the `*.test.ts` pattern.**
- **Testing framework is not specified; check existing test files for conventions.**
- **Example:**
  ```typescript
  // calculate-hours.test.ts
  import { calculateHours } from './calculate-hours';

  describe('calculateHours', () => {
    it('should return correct total', () => {
      expect(calculateHours([1, 2, 3])).toBe(6);
    });
  });
  ```

## Commands
| Command       | Purpose                                     |
|---------------|---------------------------------------------|
| /add-feature  | Scaffold and implement a new feature        |
| /refactor     | Refactor or restructure existing code       |
| /write-test   | Add or update tests for a module or feature |
```
