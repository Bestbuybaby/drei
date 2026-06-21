```markdown
# drei Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches best practices and conventions for contributing to the `drei` repository, a TypeScript project built with React. You'll learn about file organization, code style, commit message patterns, and how to write and locate tests within the codebase.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `myComponent.tsx`, `useCustomHook.ts`

### Import Style
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { MyComponent } from './myComponent';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In myComponent.tsx
    export const MyComponent = () => { ... };
    ```

### Commit Messages
- Follow the **Conventional Commits** specification.
- Prefix commits with the type, such as `chore`.
- Keep commit messages concise (average 75 characters).
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Creating a New Component
**Trigger:** When adding a new reusable React component  
**Command:** `/new-component`

1. Create a new file using camelCase, e.g., `myComponent.tsx`.
2. Implement the component using TypeScript and React.
3. Export the component using a named export.
    ```typescript
    export const MyComponent = () => { ... };
    ```
4. Add relative imports for any dependencies.
5. Write a corresponding test file named `myComponent.test.tsx`.

### Updating Dependencies
**Trigger:** When dependencies need to be updated  
**Command:** `/update-deps`

1. Update the relevant dependencies in `package.json`.
2. Run the package manager to install updates.
3. Commit changes with a conventional commit message:
    ```
    chore: update [dependency] to version x.y.z
    ```

### Writing Tests
**Trigger:** When adding or updating features  
**Command:** `/write-test`

1. Create a test file with the pattern `*.test.*` (e.g., `myComponent.test.tsx`).
2. Write tests for the corresponding component or module.
3. Use the project's preferred testing framework (unspecified; check existing tests for reference).
4. Run tests to ensure correctness.

## Testing Patterns

- Test files follow the pattern `*.test.*` (e.g., `myComponent.test.tsx`).
- Place test files alongside the component/module or in a dedicated `__tests__` directory.
- The testing framework is not specified; refer to existing test files for conventions.

## Commands
| Command          | Purpose                                    |
|------------------|--------------------------------------------|
| /new-component   | Scaffold a new React component             |
| /update-deps     | Update project dependencies                |
| /write-test      | Create and run tests for a component/module|
```