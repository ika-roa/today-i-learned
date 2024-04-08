# Amending commits for release notes
## Idea
- Solve issue of "overspecification" in release notes if a feature was implemented and released in, e.g., alpha and required a bug fix. In this case, the alpha release notes should contain the fix, but once a beta/release is released only the feature should be mentioned:

- A commit "complements" a previous commit
	- show only original commit's message
	- keyword: `fixup`, e.g., `fixup: <sha>`
- A commit "reverts" a previous commit:
    -   If the **reverting** commit is part of the changelog, but the **reverted** one is not, show the **reverting commit's message**
    -   If the **reverting and reverted** commit are part of the changelog, show **neither**
    -   If the **reverted** commit is part of the changelog, but the **reverting** one is not, show the **reverted commit's message**
    -   keyword: `revert`, e.g., `revert: <sha>`
-    A commit "overrides" a previous commit:
    -   If the **overriding** commit is part of the changelog, but the **overridden** one is not, show the **overriding commit's message**
    -   If the **overriding and overridden** commit are part of the changelog, show the **overriding commit's message**
    -   If the **overridden** commit is part of the changelog, but the **overriding** one is not, show the **overridden commit's message**
    -   keyword: `override`, e.g., `override: <sha>`

## Original commit
feat: Add new feature

/#SWX-1234
sha: 123456789

## New commit
fix: Fix bug in new feature

/#SWX-1234

fixup: 123456789