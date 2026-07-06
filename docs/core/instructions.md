# 0001 - docs structure

> status: accepted  
> tags: rule, workflow

## rule

> entries separate stable rules from changeable workflows. workflows change when tools, apis, or services change, while rules only change if the underlying constraint changes.
>
> use 2 files for documentation in any repo: core and common, maintaining a flat documentation system.
>
> lowercase only.
>
> use markdown formatting only when it improves clarity or structure; allowed formatting includes inline code, code blocks, lists, bold, italic, and links; avoid formatting when it adds noise or does not improve clarity.
>
> inside blockquotes, content lines end with a period + two spaces; if followed by empty `>` line, trailing spaces are optional; empty `>` lines are separators only and have no punctuation or spaces.
>
> ensure formatting and rendering via markdown preview tools (e.g. yzhang.markdown-all-in-one).
>
> verify output before commit using vs code preview shortcuts (ctrl+k v).
>
> use this exact structure for every entry:

```md
# 000x - title

> status: draft | accepted | deprecated | rejected  
> tags: rule, procedure (classification labels for the entry, can include multiple values and may be extended when needed)

## rule

> required behavior or constraint.

## reason

> why this exists.

## alternatives

> (optional) rejected approaches (each point includes a short reason in parentheses).

## revisit

> (optional) condition under which this rule may need to be re-evaluated or changed.
```

## reason

> minimal complexity.  
> fast navigation (Ctrl+F).  
> reduced structural overhead.

## alternatives

> folder-based docs → rejected (adds unnecessary hierarchy).  
> index.md system → rejected (not needed for navigation).

## revisit

> if docs grow too large for single-file navigation.

# 0002 - github issues and project workflow

> status: accepted  
> tags: rule, workflow, project-specific

## rule

> use github issues as primary task tracking system. create all work items as issues and organize them via github projects. use vs code extension (github.vscode-pull-request-github) to create, view, and manage issues and pull requests, or use github web ui when needed.

## reason

> centralizes work tracking. enables structured planning. improves traceability between tasks and code. keeps development workflow consistent across ide and github.

## revisit

> if a different project management system replaces github issues.

# 0003 - commit linking rule

> status: accepted  
> tags: rule, workflow, project-specific

## rule

> include github issue references in commit messages using keywords (closes #id, fixes #id, resolves #id) together with a normal descriptive commit message.

## reason

> enables automatic traceability between code changes and tracked work items.

## revisit

> if a different issue tracking system replaces github issues.

# 0004 - dev folder

> status: accepted  
> tags: rule, workflow, project-specific

## rule

> `dev/` is a local developer sandbox.  
> contents are disposable and gitignored.  
> shared or production code must not live here.

## reason

> faster development.  
> reduced context switching.  
> isolated temporary work.

## alternatives

> temporary files outside repo → rejected (context switching).  
> shared utilities in `dev/` → rejected (belongs in `packages/`).
