# Hackathon prep: my setup plan (Sat 21 Nov)

Event starts 14:20 (game design), first build 14:35. Goal: be fully set up and practiced well before then.

## 1. Install tools
- [ ] Claude Code: `curl -fsSL https://claude.ai/install.sh | bash`
      (or use the **Code** tab in the Claude desktop app)
- [ ] New terminal tab → `claude --version` prints a version
- [ ] GitHub CLI: `brew install gh` → `gh auth login` (GitHub.com, HTTPS, browser)
- [ ] `gh auth status` shows logged in
- [ ] Join the Europa-Hack Slack (link in the facilitation guide)

## 2. Set up workspace
- [ ] `mkdir -p ~/code/europaskolan`
- [ ] Put these files from the chat into it:
  - `index.html` (Star Catcher starter game)
  - `PROMPT_TEMPLATE.md` (spec prompt + improve loop)
  - `CLAUDE.md` (keep-it-simple rules Claude Code reads automatically)
  - `SETUP_PLAN.md` (this file)
  - `CODE_SESSION.md` (prompts to paste for step 4)
- [ ] `open ~/code/europaskolan/index.html` → Star Catcher plays in the browser

## 3. Co-facilitators' games
- [ ] Get repo / file links from Slack
- [ ] Clone 1–2: `cd ~/code/europaskolan && gh repo clone <owner>/<repo>`
- [ ] Run: `open <repo>/index.html`, or `npx serve <repo>` if it loads assets
- [ ] Note anything useful in their setup (prompts, structure) to reuse

## 4. Switch to Claude Code and test the setup I'll run with Uma
Follow `CODE_SESSION.md` in the Code tab (desktop app → Code → folder `~/code/europaskolan`).
- [ ] `cd ~/code/europaskolan && claude` (log in on first run)
- [ ] Check it picked up CLAUDE.md: ask "what are the rules for this folder?"
- [ ] Smoke test: "open index.html in my browser"
- [ ] Edit test on the starter: "make the player a 🦖 and stars 🍕"; refresh, confirm it worked
- [ ] Full dry run with a throwaway idea:
  - `mkdir practice && cd practice && claude`
  - Fill in PROMPT_TEMPLATE.md with a silly idea, paste it in
  - Time it: idea → playable game = ____ min
  - Do 2 improve-loop changes, time each = ____ min
- [ ] Save test: `git init && git add -A && git commit -m "practice"`
      (optionally `gh repo create … --source=. --push`)
- [ ] Set up the screen: terminal and browser side by side, font big enough for a 9-year-old to read
- [ ] Laptop charged, charger packed
- [ ] Ready by ~13:45
