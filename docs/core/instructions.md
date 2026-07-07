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

# 0002 - dev folder

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
