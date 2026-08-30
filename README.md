# Remove AI Design Slop

A free Claude skill that stops your AI-generated graphics looking like everyone else's.

## The problem

AI graphics all look the same, and they look the same for a reason. Given no brand
reference to read, a model reaches for the same handful of moves every time. A
purple-to-blue gradient. A coloured strip down a card edge. Emoji instead of icons. A
motivational band across the bottom. A grid of identical rectangles.

## What this does

Two halves.

**It names the 29 tells**, so you can check your own work against them. Every one came out
of a real graphic that got rejected.

**Then it borrows a world.** Your graphic becomes a document everybody already recognises,
a Wikipedia article or a spreadsheet or a file tree, so the layout arrives pre-trusted and
the reader spends their attention on your content instead of decoding your design.

It also holds far more than a card grid. Twenty-nine rules, a sidebar, an infobox and six
citations fit on one 1080x1350 canvas and still read at feed size. Cards top out around
twelve.

## Install

```bash
git clone https://github.com/charlie947/remove-ai-design-slop.git
cp -r remove-ai-design-slop/skills/* ~/.claude/skills/
```

Then say "remove the AI slop from this" and hand it your list.

## The part that matters

The Sources block. Real reference documents carry citations, so yours does too, and yours
are direct quotes with dates from wherever your rules came from.

That is the half nobody can copy. Anyone can rebuild the layout in an hour. Nobody else has
six dated quotes from inside your own work.

Never invent one. If you only have four real quotes, ship four.

---

By [Charlie Hills](https://charliehills.substack.com). More free resources in the
[Resource Vault](https://charliehills.substack.com/p/resource).
