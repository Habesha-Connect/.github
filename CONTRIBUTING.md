# Habesha Connect - Commit Rules & Conventions

## Commit Message Format

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification for all commit messages across all Habesha Connect repositories.

### Format

```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

### Structure Rules

1. **First line** (subject): Maximum 72 characters
2. **Body** (optional): Wrapped at 72 characters, separated by blank line from subject
3. **Footer** (optional): Reference issues, breaking changes
4. **Language**: English only for consistency
5. **Tense**: Present imperative ("add" not "added" or "adds")
6. **Capitalization**: Lowercase first letter of description
7. **No period** at end of subject line

---

## Types

| Type | Description | Example |
|------|-------------|---------|
| `feat` | New feature | `feat(auth): add OTP verification via TeleRivet` |
| `fix` | Bug fix | `fix(payments): correct service fee calculation for amounts over 1000 ETB` |
| `docs` | Documentation changes | `docs(api): update payment endpoint examples` |
| `style` | Code style (formatting, spacing) | `style(components): format button component with prettier` |
| `refactor` | Code refactoring without feature changes | `refactor(workers): extract matching algorithm to separate service` |
| `perf` | Performance improvements | `perf(jobs): optimize worker matching query with indexing` |
| `test` | Adding or modifying tests | `test(bookings): add integration tests for acceptance flow` |
| `chore` | Build process, dependencies, tooling | `chore(deps): update React to 18.3.0` |
| `ci` | CI/CD changes | `ci(github): add automated deployment workflow` |
| `revert` | Reverting previous commit | `revert: revert feat(auth): add OTP verification` |

### Breaking Changes

Breaking changes must be indicated by:
- Appending `!` after the type: `feat!:` 
- OR adding `BREAKING CHANGE:` in the footer

```
feat!(api): change payment response structure

BREAKING CHANGE: Payment response now includes fee breakdown object instead of flat fields
```

---

## Scopes

Scopes should be lowercase and hyphenated. Choose from the following approved scopes:

### Frontend Scopes (habesha-connect-web)
| Scope | Description |
|-------|-------------|
| `auth` | Authentication, login, registration |
| `ui` | Base UI components (Button, Input, Modal) |
| `layout` | Layout components (Header, Footer, Sidebar) |
| `dashboard` | Dashboard pages |
| `jobs` | Job posting, browsing, management |
| `workers` | Worker profile, browsing, verification |
| `bookings` | Booking creation and management |
| `payments` | Payment processing and history |
| `ratings` | Rating and review system |
| `disputes` | Dispute filing and resolution |
| `notifications` | In-app notifications |
| `profile` | User profile management |
| `admin` | Admin portal pages |
| `forms` | Form components and validation |
| `routing` | Route configuration and navigation |
| `state` | State management changes |
| `styles` | Styling, theming, design tokens |
| `i18n` | Internationalization, translations |
| `a11y` | Accessibility improvements |
| `perf` | Performance optimizations |

### Backend Scopes (habesha-connect-api)
| Scope | Description |
|-------|-------------|
| `auth` | Authentication service |
| `users` | User management |
| `clients` | Client-specific endpoints |
| `workers` | Worker-specific endpoints |
| `verification` | Verification process |
| `pricing` | Fixed pricing system |
| `jobs` | Job management |
| `bookings` | Booking management |
| `payments` | Payment processing |
| `ratings` | Rating system |
| `disputes` | Dispute resolution |
| `notifications` | Notification service |
| `sms` | SMS integration (TeleRivet) |
| `admin` | Admin endpoints |
| `analytics` | Analytics and reporting |
| `middleware` | API middleware |
| `validation` | Input validation |
| `security` | Security improvements |

### Database Scopes (habesha-connect-database)
| Scope | Description |
|-------|-------------|
| `schema` | Schema changes |
| `migrations` | Database migrations |
| `seeds` | Seed data |
| `indexes` | Index management |
| `views` | Database views |
| `functions` | Stored procedures/functions |
| `triggers` | Database triggers |
| `perf` | Query optimization |

### Shared/Cross-Cutting Scopes
| Scope | Description |
|-------|-------------|
| `deps` | Dependencies |
| `config` | Configuration files |
| `build` | Build scripts and tools |
| `docs` | Documentation |
| `types` | TypeScript type definitions |

---

## Examples

### Good Commit Messages

```
feat(auth): add phone number OTP authentication flow
```
```
fix(payments): prevent duplicate payment processing for same booking

Added unique constraint check before processing payment to ensure
a booking cannot be paid for multiple times. Returns 409 Conflict
if payment already exists for the booking.

Closes JIRA-456
```
```
refactor(workers): extract verification logic to dedicated service

Moved all verification-related logic from WorkerService to new
VerificationService for better separation of concerns. This enables:
- Independent testing of verification logic
- Easier maintenance of verification rules
- Preparation for future verification methods

No breaking changes. All existing tests pass.
```
```
feat!(api): change worker matching response format

Redesigned the matching response to include detailed match scores
and ranking explanations for better transparency.

BREAKING CHANGE: The /jobs/{id}/matches endpoint now returns
{workers: [...], summary: {...}} instead of flat array.
```
```
docs(api): add comprehensive payment webhook documentation
```
```
test(bookings): cover worker acceptance and rejection scenarios

Added 15 test cases covering:
- Normal acceptance flow
- Rejection with reason
- Expired job handling
- Race condition prevention
- SMS notification verification
```
```
chore(deps): update typescript to 5.3.3
```

### Bad Commit Messages (Avoid These)

```
fixed stuff
```
Problem: No type, vague description, past tense

```
feat: update
```
Problem: No scope, description too vague

```
WIP
```
Problem: No type or scope, not descriptive

```
feat(auth): Added OTP verification and fixed login bug and updated docs
```
Problem: Multiple unrelated changes, too long, past tense

```
.
```
Problem: Not a message

```
feat(authentication): add OTP verification via TeleRivet SMS gateway for Ethiopian phone numbers
```
Problem: Subject line exceeds 72 characters

---

## Branch Naming Conventions

Branch names should follow these patterns:

```
feature/<scope>-<description>
bugfix/<scope>-<description>
hotfix/<scope>-<description>
release/v<version>
chore/<description>
docs/<description>
refactor/<scope>-<description>
```

### Examples
```
feature/auth-phone-otp-verification
feature/jobs-advanced-filtering
bugfix/payments-fee-calculation-error
bugfix/bookings-duplicate-acceptance
hotfix/sms-delivery-timeout
release/v1.0.0
release/v1.2.1
chore/update-tailwind-config
docs/api-authentication-endpoints
refactor/workers-matching-algorithm
```

### Branch Naming Rules
- Use lowercase letters
- Separate words with hyphens
- Keep descriptions concise but descriptive
- Reference issue numbers when applicable: `feature/JIRA-123-user-auth`
- No special characters except hyphens
- No trailing or leading hyphens

---

## Commit Frequency

### Guidelines
- Commit logical units of change
- Each commit should do one thing well
- Commit working code (tests should pass)
- Commit early and often during development
- Squash before merging to main/develop if commits are messy

### When to Commit
- After completing a logical feature unit
- After fixing a bug
- After writing passing tests
- After significant refactoring
- After updating documentation

### When NOT to Commit
- Broken code that doesn't compile
- Work-in-progress without logical completion (use `wip` branches instead)
- Generated files (dist, build artifacts)
- Secrets or sensitive information
- Large binary files without Git LFS

---

## Pull Request Requirements

Before merging, PRs must:

1. **Follow commit conventions** - All commits in the PR must follow these rules
2. **Pass CI checks** - Lint, type-check, and tests must pass
3. **Include tests** - New features must include tests
4. **Update documentation** - API changes must update docs
5. **Have clean history** - Squash messy commits before merging

### PR Title Format
```
<type>(<scope>): <description>
```

Matches commit format but describes the entire PR scope.

---

## Git Hooks (Recommended)

### Pre-commit Hook
```bash
# Check for:
- Lint errors
- Type errors
- Test failures
- Debug statements (console.log)
- Large files
- Secrets/keys
```

### Commit-msg Hook
```bash
# Validate:
- Conventional commit format
- Subject line length (max 72 characters)
- Valid type and scope
- No trailing period
```

### Pre-push Hook
```bash
# Run:
- Full test suite
- Build verification
```

---

## Enforcement

### Automated Checks
- CI pipeline validates commit messages
- PR title validated against conventional commits
- Branch naming enforced via GitHub settings
- Pre-commit hooks recommended but not enforced

### Manual Review
- Code reviewers check commit quality
- Commit history reviewed before merge
- Non-conforming commits flagged during review

### Tools
- `commitlint` for commit message validation
- `husky` for git hooks
- `commitizen` for interactive commit creation
- GitHub Actions for CI enforcement

---

## Quick Reference Card

```
Commit: type(scope): description
Branch: type/scope-description
PR:     type(scope): description

Types:  feat, fix, docs, style, refactor, perf, test, chore, ci, revert

Rules:
- Lowercase, present tense
- Max 72 chars subject
- No period at end
- One logical change per commit
- Break with ! or BREAKING CHANGE footer
```

---

## Common Scenarios

### Adding a new feature
```bash
git checkout -b feature/auth-otp-verification
# ... make changes
git commit -m "feat(auth): add OTP verification via TeleRivet SMS"
git commit -m "test(auth): add OTP verification unit tests"
git commit -m "docs(auth): document OTP verification flow"
```

### Fixing a bug
```bash
git checkout -b bugfix/payments-fee-calculation
# ... make changes
git commit -m "fix(payments): correct fee calculation for amounts over 1000 ETB"
```

### Updating dependencies
```bash
git checkout -b chore/update-dependencies
# ... make changes
git commit -m "chore(deps): update React to 18.3.0"
git commit -m "chore(deps): update TypeScript to 5.3.3"
```

### Making breaking changes
```bash
git checkout -b feature/api-v2-payment-response
# ... make changes
git commit -m "feat!(api): restructure payment response format

BREAKING CHANGE: Payment response now includes nested fee object
instead of flat fields. Clients must update response parsing."
```

---

**Document Version:** 1.0.0
**Last Updated:** 2026-05-09
**Applies To:** All Habesha Connect repositories
**Enforcement:** CI validation + code review