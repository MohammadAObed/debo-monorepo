# 0001 - development environment setup

> status: accepted  
> tags: instruction, workflow, global, windows, web, mobile

## rule

> update windows system via settings.
>
> install/update core development tools: google chrome, visual studio code, git for windows (includes git bash), node.js lts (includes npm), pnpm, autoHotkey.
>
> install/update mobile development tools: android studio (includes sdk + emulator tools).
>
> verify installations in git bash using: `git --version`, `node --version`, `npm --version`, `pnpm --version`.
>
> install vscode extensions grouped by purpose:

### core productivity & code quality

> - prettier (esbenp.prettier-vscode) → format on save.
> - eslint (dbaeumer.vscode-eslint) → lint on save.
> - githistory (donjayamanne.githistory).
> - gitlens (eamodio.gitlens).
> - error lens (usernamehw.errorlens).
> - better comments (aaron-bond.better-comments).
> - todo tree (gruntfuggly.todo-tree).
> - path intellisense (christian-kohler.path-intellisense).
> - material icon theme (pkief.material-icon-theme).
> - code spell checker (streetsidesoftware.code-spell-checker).
> - turbo console log (chakrounanas.turbo-console-log).
> - abracadabra refactor magic (nicoespeon.abracadabra).
> - batch rename extension (jannisx11.batch-rename-extension).
> - regex text generator (rioj7.regex-text-gen).
> - github pull requests (github.vscode-pull-request-github).

### web development

> - live server (ritwickdey.liveserver).
> - html css support (ecmel.vscode-html-css).
> - css peek (pranaygp.vscode-css-peek).
> - colorize (kamikillerto.vscode-colorize).
> - vs color picker (lihui.vs-color-picker).
> - markdown all in one (yzhang.markdown-all-in-one).
> - javascript (es6) snippets (xabikos.javascriptsnippets).
> - pretty typescript errors (yoavbls.pretty-ts-errors).
> - prettify typescript (mylesmurphy.prettify-ts).

### react & react native

> - react native tools (msjsdiag.vscode-react-native).
> - react native snippets (jundat95.react-native-snippet).
> - react component tree (habeebarul.react-component-tree).
> - typescript react snippets (infeng.vscode-react-typescript).

### mobile development

> - android emulator (diemasmichiels.emulate).
> - expo tools (expo).

### database & backend

> - sqlite viewer (qwtel.sqlite-viewer).
> - sqltools (mtxr.sqltools).
> - vscode sqlite (alexcvzz.vscode-sqlite).

## reason

> standardizes development environment setup across windows systems. ensures consistent tooling for web and mobile development. reduces onboarding friction. improves debugging and productivity consistency.

## revisit

> if environment becomes containerized (devcontainers/docker) or automated bootstrap scripts replace manual setup.  
> if extension ecosystem changes significantly or becomes deprecated.

# 0002 - git identity configuration

> status: accepted  
> tags: instruction, workflow

## rule

> configure git identity globally using git bash:
>
> git config --global user.name "yourgithubusername"  
> git config --global user.email "your-email@example.com"
>
> this identity is used for all commits on the system.
>
> github login is required only when pushing code for the first time.

## reason

> ensures commits are correctly attributed and linked to github accounts.

## revisit

> if git identity becomes per-repository instead of global.

# 0003 - vscode default terminal setup (git bash)

> status: accepted  
> tags: instruction, workflow

## rule

> set vscode default terminal profile to git bash via:
>
> terminal → new terminal → select default profile → git bash
>
> all new terminals must use git bash.

## reason

> ensures consistent shell environment across development workflows.

## revisit

> if shell environment changes (powershell, wsl, zsh).

# 0004 - github account setup

> status: accepted  
> tags: instruction, workflow

## rule

> create and maintain a github account.
>
> authentication happens automatically on first git push.
>
> no manual login required for local git usage.

## reason

> enables version control and repository access.

## revisit

> if authentication moves to cli token-based setup or unified dev auth system.

# 0005 - github issues and project workflow

> status: accepted  
> tags: instruction, workflow

## rule

> use github issues as primary task tracking system. create all work items as issues and organize them via github **projects**.
>
> use vscode extension (github.vscode-pull-request-github) to create, view, and manage issues and pull requests, or use github web ui when needed.

## reason

> centralizes task tracking. enables structured planning. improves traceability between tasks and code. keeps development workflow consistent across ide and github.

## revisit

> if a different project management system replaces github issues.

# 0006 - expo account setup

> status: accepted  
> tags: instruction, workflow, mobile

## rule

> create and maintain an expo account via expo.dev.
>
> login using:
>
> expo login
>
> enter credentials when prompted.

## reason

> enables react native development services and deployment workflows.

## revisit

> if expo authentication system changes or becomes token-based only.

# 0007 - google & ai-assisted usage

> status: accepted  
> tags: instruction, workflow

## rule

> use google search and ai tools for:
>
> coding help, documentation lookup, debugging, and resolving unclear setup steps.
>
> validate outputs before applying changes.

## reason

> improves development speed and reduces uncertainty during setup and implementation.

## revisit

> if ai tools become fully integrated into the development environment.

# 0008 - windows startup applications

> status: accepted  
> tags: instruction, workflow, windows

## rule

> open the windows startup folder using `shell:startup`.
>
> place shortcuts for applications that should start automatically with windows.
>
> recommended applications:
>
> - visual studio code.
> - google chrome (preferred profile).
> - autohotkey scripts.

## reason

> reduces repetitive startup tasks and keeps the development environment ready after login.

# 0009 - taskbar pinning

> status: accepted  
> tags: instruction, workflow, windows

## rule

> pin frequently used applications to the windows taskbar for quick access (visual studio code & google chrome).

## reason

> reduces navigation time and improves workflow efficiency.

# 0010 - always-on-top shortcut

> status: accepted  
> tags: instruction, workflow, windows, autohotkey

## rule

> create an autohotkey script named `alwaysontop.ahk`.
>
> add:
>
> ```ahk
> ^]::WinSet, AlwaysOnTop, , A
> ```
>
> place the script in the windows startup folder.
>
> use `ctrl + ]` to toggle always-on-top for the active window.
>
> useful for keeping windows such as android emulators visible while working.

## reason

> improves multitasking by keeping important windows visible.

## revisit

> if autohotkey or windows provides a built-in alternative.

# 0011 - google chrome extensions

> status: accepted  
> tags: instruction, workflow, chrome

## rule

> install recommended google chrome extensions:
>
> - google translate.
> - colorzilla.
> - youtube playback speed control.
> - recent tabs.
> - whatfont.

## reason

> improves browsing, development, and daily productivity.

## revisit

> if extensions become deprecated or better alternatives exist.

# 0012 - keyboard shortcuts

> status: accepted  
> tags: reference, windows, vscode, chrome

## rule

### windows

> - ctrl + shift + esc → task manager.
> - alt + tab → switch applications.
> - win + v → clipboard history.
> - win + d → desktop.
> - win + e → file explorer.
> - win + l → lock pc.
> - win + r → run dialog.
> - win + s → search.
> - win + i → settings.
> - win + shift + s → snipping tool.
> - win + . → emoji panel.
> - ctrl + ] → toggle always-on-top.

> - ctrl + c → copy.
> - ctrl + x → cut.
> - ctrl + v → paste.
> - ctrl + z → undo.
> - ctrl + y → redo.
> - ctrl + a → select all.
> - ctrl + s → save.
> - ctrl + p → print.
> - ctrl + n → new.
> - ctrl + f → find.

### google chrome

> - ctrl + n → new window.
> - ctrl + t → new tab.
> - ctrl + w → close tab.
> - ctrl + shift + t → reopen closed tab.
> - ctrl + tab → next tab.
> - ctrl + shift + tab → previous tab.
> - ctrl + l / alt + d → address bar.
> - ctrl + f → find.
> - ctrl + r / f5 → reload.
> - ctrl + h → history.
> - ctrl + j → downloads.
> - ctrl + shift + n → incognito.
> - ctrl + shift + b → bookmarks bar.
> - ctrl + shift + i → developer tools.
> - ctrl + shift + c → inspect element.

### visual studio code

> - ctrl + tab → next editor.
> - ctrl + p → quick open.
> - ctrl + shift + p → command palette.
> - ctrl + b → toggle sidebar.
> - ctrl + ` → terminal.
> - ctrl + , → settings.
> - ctrl + k ctrl + s → keyboard shortcuts.
> - ctrl + / → toggle comment.
> - ctrl + space → intellisense.
> - ctrl + . → quick fix.
> - ctrl + f → find.
> - ctrl + shift + f → global search.
> - ctrl + g → go to line.
> - f12 → go to definition.
> - alt + f12 → peek definition.
> - alt + left → navigate back.
> - alt + right → navigate forward.
> - alt + up/down → move line.
> - shift + alt + up/down → copy line.
> - home → line start.
> - end → line end.
> - ctrl + home → file start.
> - ctrl + end → file end.
> - ctrl + shift + \ → matching bracket.
> - ctrl + ] → indent.
> - ctrl + [ → outdent.
> - ctrl + k ctrl + 0 → fold all.
> - ctrl + k ctrl + j → unfold all.
> - ctrl + d → select next occurrence.
> - ctrl + shift + l → select all occurrences.

## reason

> provides a centralized reference for frequently used shortcuts.

## revisit

> if shortcuts change significantly across supported versions.

# 0013 - code design principles

> status: accepted  
> tags: rule, workflow, coding

## rule

> design shared and non-shared code with a balance between simplicity, clarity, and flexibility.
>
> aim for simplicity: make code easy to use by requiring the least amount of code and the fewest places to change.
>
> aim for clarity: make names understandable from their name and usage context. use documentation comments such as tsdoc when needed to improve understanding.
>
> aim for flexibility: make code easy to modify when requirements change. invest extra effort when the long-term value justifies the complexity.

## reason

> creates code that is easier to use, understand, maintain, and evolve.

## revisit

> if development practices or architecture principles change significantly.

# 0014 - github repository creation workflow

> status: accepted  
> tags: instruction, workflow, github

## rule

> create a new github repository:
>
> - open github and create a new repository.
> - set repository name, description, and visibility.
> - add readme, gitignore, and license when needed.
>
> clone the repository:
>
> - copy the repository https url.
> - open vscode git bash terminal.
> - navigate to the target folder.
> - run `git clone https://github.com/your-username/your-repo-name.git`.
> - open the cloned folder in vscode.

## reason

> provides a consistent starting workflow for new projects.

## revisit

> if repository creation workflow changes or becomes automated.

# 0015 - github issues and project workflow

> status: accepted  
> tags: rule, workflow, project-specific

## rule

> use github issues as primary task tracking system. create all work items as issues and organize them via github projects. use vs code extension (github.vscode-pull-request-github) to create, view, and manage issues and pull requests, or use github web ui when needed.

## reason

> centralizes work tracking. enables structured planning. improves traceability between tasks and code. keeps development workflow consistent across ide and github.

## revisit

> if a different project management system replaces github issues.

# 0016 - typescript workspace configuration

> status: accepted  
> tags: instruction, workflow, typescript

## rule

> when working in a typescript project:
>
> - use the workspace typescript version in vscode, not the vscode built-in version if it appears.
> - restart the typescript server when errors appear incorrect.
>
> commands:
>
> ctrl+shift+p → select typescript version → use workspace version.
>
> ctrl+shift+p → restart typescript server.

## reason

> ensures vscode uses the correct typescript configuration and avoids incorrect editor errors.

## revisit

> if vscode typescript handling changes.

# 0017 - reference projects usage

> status: accepted  
> tags: instruction, workflow, packages

## rule

> as a dev, use our shared projects as npm-style dependencies and references for building new projects.
>
> available reference projects:
>
> - typescript common.
> - react common.
> - react js common.
> - react native common.
>
> review project docs before using them.

## reason

> improves reuse, consistency, and development across related projects.

## revisit

> if project organization or dependency sharing strategy changes.

# 0018 - react native expo project creation

> status: accepted  
> tags: instruction, workflow, mobile, react-native

## rule

> create a new react native expo project:
>
> - install android studio and create an android emulator before running the project.
> - open vscode in the parent folder where the repository will be created.
> - create the expo project using typescript.
> - use the same name as the repository.
> - use the vscode integrated git bash terminal for project commands such as `npm install`.
>
> run the android emulator:
>
> - open vscode command palette (`ctrl+shift+p`).
> - select emulator → view android emulators.
> - choose the configured emulator to launch it.
> - when expo starts, press `a` in the terminal to open the app in the android emulator.

## reason

> provides a consistent react native setup workflow and avoids environment differences between projects.

## revisit

> if expo, android studio, or emulator workflows change significantly.

# 0019 - typescript troubleshooting workflow

> status: accepted  
> tags: instruction, workflow, typescript

## rule

> when encountering a typescript error that seems incorrect, restart the typescript server:
>
> ctrl+shift+p → restart typescript server.

## reason

> resolves incorrect editor state and refreshes typescript analysis.

## revisit

> if vscode or typescript provides a different troubleshooting workflow.

# 0020 - productivity tools usage

> status: accepted  
> tags: instruction, workflow, productivity

## rule

> learn and use the productivity practices and vscode extensions defined in the development environment setup.

## reason

> ensures installed tools provide their intended value and improve daily workflow.

## revisit

> if productivity tools or workflows change.

# 0021 - code organization rules

> status: accepted  
> tags: rule, coding

## rule

> do not use index files for folders.
>
> use path aliases such as `@` when they improve import clarity and maintainability.
>
> use clear variable names. avoid shortened names that reduce understanding.

## reason

> improves code readability and makes future changes easier.

## alternatives

> short variable names → rejected (reduces understanding over time).

## revisit

> if project structure or import conventions change.

# 0022 - documentation update habit

> status: accepted  
> tags: rule, workflow

## rule

> when adding or modifying files or content, check if related documentation needs to be added, updated, or removed.

## reason

> keeps documentation synchronized with the actual project state.

## revisit

> if documentation becomes fully automated.

# 0023 - shared code package rule

> status: accepted  
> tags: rule, architecture

## rule

> do not create common code directly inside projects.
>
> create reusable packages for code shared across projects.

## reason

> prevents duplicated code and keeps shared functionality centralized.

## revisit

> if project architecture changes.

# 0024 - commit linking rule

> status: accepted  
> tags: rule, workflow, project-specific

## rule

> include github issue references in commit messages using keywords (#id, closes #id, fixes #id, resolves #id) together with a normal descriptive commit message.

## reason

> enables automatic traceability between code changes and tracked work items.

## revisit

> if a different issue tracking system replaces github issues.
