# Conventional Commits

## WTF is that and why should I care?

- https://www.conventionalcommits.org/
- unified way to commit changes to your repositories
- monorepo friendly (actually does not care)
- validable commit messages
- semver friendly
- squashing does not break it

## Format

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

- `verb: message`
- `verb(scope): message`

### Examples 

- `feat(integrations): add support for Google Worskpaces`
- ```
  fix(sso): broken gitlab auth

  closes #14
  ```

### Verbs

- `feat`
- `fix`
- `BREAKING CHANGE` (IMHO: too long)

- `refactor`

- `docs`
- `build`
- `deps`
- `ci`
- `chore`
- `perf`
- `test`
- [Angular Convention](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines)

- more?

### Scope (context)

**OPTIONAL!**

- What part of the repository is this related to
- 

### Commit message / description

- first line of commit message should be < 80 charaters long
- imperative
- multiline is OK
- IMHO: multiline is wanted when squashing commits

#### BREAKING CHANGE

- `BREAKING CHANGE: ...`
- `refactor!: ...`
- `refactor()!: ...`

- SemVer is happy

## Next release version is deterministic

### MAJOR vs MINOR vs PATCH

- based on commit messages (`BREAKING CHANGE`, `refactor!`) -> MAJOR
- `feat` -> MINOR
- `fix` -> PATCH

### Release notes / Changelog

- easily generatable from commit messages