# game spec prompt (fill in with the kids at 14:20–14:35)

paste into Claude Code from inside the game's folder (`cd ~/code/europaskolan/<game-name> && claude`).

```
Build a simple browser game as ONE self-contained index.html file
(HTML + CSS + JS inline, no build step, no external libraries, no network).
Use emoji or simple canvas shapes for graphics, no image files.

Game name: <NAME>
What it's about: <ONE SENTENCE, e.g. "a cat catching falling stars in space">
What the player does: <e.g. "moves left/right to catch good things and dodge bad things">
Controls: <arrow keys / WASD / mouse / touch / space to jump>
How you score / win: <e.g. "+1 per star, lose a life for rocks, highest score after 60s">
What makes it fun: <e.g. "it gets faster, rare rainbow worth 5 points, silly sounds">
Round length: about 60–90 seconds.

Requirements:
- Start screen with the title, how to play, and a big Play button.
- Score, timer and lives visible on screen.
- Game-over screen with the score and a Play Again button.
- Gets a bit harder over time.
- Put all tunable numbers (speed, time, points, emoji) in a CONFIG object
  at the top of the script so we can tweak them quickly.
- Must work when opened directly with `open index.html`.

When done, tell me how to play it in 3 bullet points.
```

## improve loop (15:15–16:15)
after each play test ask: what's fun? what's confusing? ONE thing to change?
then prompt one change at a time, e.g.:
- "make the player a 🦖 and the bad things 🌋"
- "add a sound when you catch something (use WebAudio beeps, no files)"
- "add a level 2 after 30 seconds with a new enemy"
- "it's too hard, make things fall slower at the start"

## demo prep (16:30)
what is our game? how do you play? what did we change after testing?

## save work
```
git init && git add -A && git commit -m "our game"
gh repo create <name> --public --source=. --push   # or share index.html in slack
```
