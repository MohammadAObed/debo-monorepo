# 0001 - development environment setup

> status: accepted  
> tags: instruction, workflow, global, windows, web, mobile

## rule

> update windows system via settings.
>
> install core development tools: google chrome, visual studio code, git for windows (includes git bash), node.js lts (includes npm), autoHotkey.
>
> install mobile development tools: android studio (includes sdk + emulator tools).
>
> verify installations in git bash using: `git --version`, `node --version`, `npm --version`.
>
> install vscode extensions grouped by purpose:

### core productivity & code quality

> - prettier (esbenp.prettier-vscode) → format on save.
> - eslint (dbaeumer.vscode-eslint) → lint on save.
> - githistory (donjayamanne.githistory).
> - gitlens (eamodio.gitlens).
> - atlassian jira & bitbucket (atlassian.atlascode).
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

### web development

> - live server (ritwickdey.liveserver).
> - tailwind css intellisense (bradlc.vscode-tailwindcss).
> - html css support (ecmel.vscode-html-css).
> - css peek (pranaygp.vscode-css-peek).
> - color highlight (naumovs.color-highlight).
> - colorize (kamikillerto.vscode-colorize).
> - vs color picker (lihui.vs-color-picker).
> - markdown preview enhanced (shd101wyy.markdown-preview-enhanced).
> - markdown emoji (bierner.markdown-emoji).
> - javascript (es6) snippets (xabikos.javascriptsnippets).
> - vscode html color (anseki.vscode-color).

### react & react native

> - react native tools (msjsdiag.vscode-react-native).
> - react native snippets (jundat95.react-native-snippet).
> - react component tree (habeebarul.react-component-tree).
> - react redux snippets (equimper.react-native-react-redux).
> - typescript react snippets (infeng.vscode-react-typescript).
> - pretty typescript errors (yoavbls.pretty-ts-errors).
> - prettify typescript (mylesmurphy.prettify-ts).

### mobile development

> - android emulator (diemasmichiels.emulate).
> - expo tools (expo).

### database & backend

> - sqlite viewer (qwtel.sqlite-viewer).
> - sqltools (mtxr.sqltools).
> - vscode sqlite (alexcvzz.vscode-sqlite).
> - mongo snippets for node.js (roerohan.mongo-snippets-for-node-js).

### ai & copilot

> - codex / chatgpt (openai.chatgpt).
> - intellicode (visualstudioexptteam.vscodeintellicode).
> - intellicode api usage examples (visualstudioexptteam.intellicode-api-usage-examples).
> - github copilot (github.copilot).
> - github copilot chat (github.copilot-chat).

## reason

> standardizes development environment setup across windows systems. ensures consistent tooling for web and mobile development. reduces onboarding friction. improves debugging and productivity consistency.

## revisit

> if environment becomes containerized (devcontainers/docker) or automated bootstrap scripts replace manual setup.  
> if extension ecosystem changes significantly or becomes deprecated.
