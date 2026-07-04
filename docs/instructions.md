# 0001 - docs structure

> status: accepted  
> type: rule

## rule

> flat documentation system  
> lowercase only  
> use 2 trailing spaces at end of each line for markdown line breaks  
> ensure formatting + rendering via markdown preview tools (e.g. yzhang.markdown-all-in-one)  
> verify output before commit using VS Code preview shortcuts (Ctrl+K V)  
> use this exact structure for every entry:

```md
# 000x - title

> status: accepted | draft | deprecated  
> type: rule | instruction | prompt

## rule

> required behavior or constraint

## reason

> why this exists

## alternatives

> rejected approaches (each point includes a short reason in parentheses)

## revisit (optional)

> condition under which this rule may need to be re-evaluated or changed
```

## reason

> minimal complexity  
> fast navigation (Ctrl+F)  
> reduced structural overhead

## alternatives

> folder-based docs → rejected (adds unnecessary hierarchy)  
> index.md system → rejected (not needed for navigation)

## revisit

> if docs grow too large for single-file navigation

# 0002 - dev folder

> status: accepted  
> type: rule

## rule

> `dev/` is a local developer sandbox  
> contents are disposable and gitignored  
> shared or production code must not live here

## reason

> faster development  
> reduced context switching  
> isolated temporary work

## alternatives

> temporary files outside the repo → rejected (context switching)  
> shared utilities in `dev/` → rejected (belongs in `packages/`)
