# Claude Code session: setup test

Open the **Code** tab in the Claude desktop app → pick folder `~/code/europaskolan` → paste these prompts one at a time.

## 1. Context check
```
What are the rules for this folder? Then list the files here and say what each is for.
```
✅ It should repeat CLAUDE.md (single index.html, no libraries, one change at a time) and recognise all 5 files.

## 2. Tooling check
```
Check my tools: run git --version, gh --version, gh auth status, node --version, npx --version. Tell me what's missing and how to fix it.
```
✅ All present and `gh` logged in.
❌ If `gh` is missing or logged out: in your own terminal run `brew install gh` then `gh auth login`, because the login opens a browser.

## 3. Run the starter game
```
Open index.html in my default browser.
```
✅ Star Catcher opens; Play works with arrows and mouse.

## 4. Edit loop (the loop you'll run with Uma)
```
Make the player a 🦖 and the stars 🍕.
```
Refresh the browser. ✅ The change is visible.
Note: time from prompt to visible change = ____ s.

## 5. Undo
```
Undo that last change.
```
✅ Back to 🐱 and ⭐. You need this before a kid's idea breaks the game.

## 6. Git baseline
```
Initialise git here, add a .gitignore for .DS_Store, and commit everything as "starter".
```
✅ `git log` shows one commit. From now on you can say "commit this" after each working version, and "go back to the last commit" if something breaks.

## 7. Co-facilitators' games (once you have links from Slack)
```
Clone <github-url> into a subfolder and open it in my browser. If it needs a local server, start one with npx serve.
```
✅ The game plays. Look at how they structured their prompt and files.

## 8. Full dry run (timed)
```
Create a folder called practice and build a game there using PROMPT_TEMPLATE.md, with this idea: <silly idea, e.g. "a penguin sliding down a mountain dodging trees, collect fish">.
```
Time from idea to playable = ____ min.
Then do 2 improve-loop changes, e.g.:
```
Add a beep sound when you collect something.
```
```
It's too hard at the start, make it slower for the first 15 seconds.
```
Time per change = ____ min.

## 9. Session ergonomics
- [ ] Permission prompts: if it asks before every edit, allow file edits in this folder for the session so the loop with Uma isn't slow.
- [ ] Increase text size (Cmd +) so Uma can read along.
- [ ] Code tab and browser side by side.

## Reset before the event
```
Delete the practice folder, make sure index.html is back to the starter version, and commit.
```
