# Remove AI Design Slop

A free Claude skill that stops your AI-generated graphics looking like everyone else's.

## The problem

AI graphics all look the same, and they look the same for a reason. Given no brand reference to read, a model reaches for the same handful of moves every time. A purple-to-blue gradient. A coloured strip down a card edge. Emoji instead of icons. A motivational band across the bottom. A grid of identical rectangles.

You cannot fix that by prompting harder. The model has nothing of yours to read, so it has nothing to point at.

The fix is not a better prompt. It is a file.

## What this does

**Part one builds the reference.** Four files, one of them four lines long, that every future graphic reads before it draws:

```
your-project/
  CLAUDE.md        the four lines that make it read everything below
  REFERENCE.md     the rules
  DESIGN.md        the build system
  examples/        five things you were happy with
```

The skill carries the exact prompt for each one. Run them once and the files last forever.

**Part two is the checklist.** 29 tells, every one out of a real graphic that got rejected, and every one checkable in about two seconds on a finished render.

**Part three is for a long list.** Under fifteen items, use cards. Over that, borrow a world: make the graphic BE a document everybody already recognises, a Wikipedia article or a spreadsheet or a file tree, so the layout arrives pre-trusted. Twenty-nine rules, a sidebar, an infobox and six citations fit on one 1080x1350 canvas and still read at feed size. Cards top out around twelve.

## Install

```bash
git clone https://github.com/charlie947/remove-ai-design-slop.git
cp -r remove-ai-design-slop/skills/* ~/.claude/skills/
```

Then say "remove the AI slop from this".

There is nothing to install for Part One. The prompts run on the free tier of Claude at claude.ai.

## Ending it with real quotes

Every reference document ends with a list of sources. Yours does the same, and this is the bit that makes the graphic yours rather than a template.

Each rule on your graphic came from somewhere. Somebody said it to you, or you wrote it down after something went wrong. Go and find four to six of those actual sentences, add the date each one was said, and put them in a numbered list at the bottom.

They look like this:

```
1. "I never ever used the loop arrow. I hate seeing that." (18/06/2026)
2. "I don't like the power ending you've added here." (25/08/2026)
```

Client feedback, a message from your boss, a code review comment, a support ticket, a note to yourself. Anywhere the rule actually came from.

Anyone can rebuild the layout in an hour. Nobody can rebuild those, because they happened to you.

Never make one up. Four real ones beat six invented, and anyone reading closely can tell the difference.

---

By [Charlie Hills](https://charliehills.substack.com). More free resources in the [Resource Vault](https://charliehills.substack.com/p/resource).
