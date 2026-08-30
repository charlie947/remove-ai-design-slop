---
name: remove-ai-design-slop
description: >
  Stop your AI-generated graphics looking like everyone else's. Turn a list of rules,
  tells or mistakes into a graphic that looks like a real reference document rather
  than an AI card grid. Use when the user says "my graphics look AI-made", "remove the
  AI slop", "make this look designed", "wikipedia style", "signs of", "anatomy of", or
  has a long list a normal card layout cannot hold. Produces 1080x1350 for LinkedIn or
  Instagram.
---

# Remove AI Design Slop

## CRITICAL: Auto-start on load

Go straight to Step 1. Do not summarise. Do not explain the format. Start.

## The problem this solves

AI-generated graphics all look the same, and they look the same for a reason. Given no
brand reference to read, a model reaches for the same handful of moves every time: a
purple-to-blue gradient, a coloured strip down a card edge, emoji standing in for icons,
a motivational band across the bottom, and a uniform grid of identical rectangles.

The fix is two halves. **Stop making the tells.** And **borrow a world**, so the layout
arrives pre-trusted instead of looking like a template.

## The 29 tells, and none of them are about taste

A tell is what a model reaches for when it has nothing of yours to read. Check your work
against these before you ship it.

**Colour and type**
1. One accent, held absolutely.
2. The accent is the subject's colour, not your house palette.
3. Colour on the glyphs, never a fill behind a word.
4. Never two accented phrases.
5. Never the purple-to-blue gradient.
6. Two typefaces, capped there.
7. A type scale in real numbers, not big, medium, small.
8. Monospace is for a string you type or an interface you are drawing.
9. Nothing is italic.

**Delete these on sight**
10. The coloured strip down a card edge.
11. Emoji standing in for drawn icons.
12. The loop arrow.
13. A motivational band across the bottom.
14. A bar or meter with no real number behind it.
15. Stock hands on a keyboard, and the robot.

**Layout**
16. On a dense list, every row takes exactly one line.
17. No orphan word alone on a last line.
18. Dead space is a content shortage, never a layout fault.
19. One full sentence per cell is the only thing that fills it.
20. A device starts somewhere and finishes somewhere, never mid-air.
21. Arrowheads meet the line they belong to.
22. The topic is visible in the drawing, not only in the title.
23. Never shrink the type to rescue a fit.
24. Vary the box sizes.

**What matters most**
25. Nobody reads the small text at feed size. They read the shape.
26. A clean checklist will pass a build that is still not good.
27. Never ship the first version.
28. Four variants means four ideas, not one text set three ways.
29. One template reused for everybody makes yours look like theirs.

## Then borrow a world

A borrowed world does the persuading before a word is read. Pick a document everybody
already recognises and make your graphic BE that thing: a Wikipedia article, a spreadsheet,
a code editor, an inbox, a file tree, a printed spec sheet.

It arrives pre-trusted, so the reader spends their attention on your content instead of
decoding your design. And it stops the scroll, because it does not look like a graphic.

It also holds far more. Twenty-nine rules, a sidebar, an infobox and six citations fit on
one portrait canvas and still read at feed size. A card layout tops out around twelve.

**It only works if it is accurate.** One wrong element and it reads as a template.

## Step 1 — Get the list

Ask for the rules, numbered, shortest first.

Each rule is **one line, one sentence, under about 70 characters.** If a rule needs two
lines the illusion breaks and it starts to look like a blog post.

Twenty to forty is the range. Under fifteen, use cards. Over forty, the type drops below
readable.

If the user hands you a paragraph, cut it into single-line rules yourself and show them
the list before building anything.

## Step 2 — Group into four to six sections

Name them the way a reference document would: a plain noun phrase, no verbs, no wit.
`Colour and type`, `Things to delete`, `Layout`.

The last section is always **Sources**.

## Step 3 — The Sources block is the proof

Real reference documents carry citations. Yours carries **direct quotes with dates.**

Pull six real quotes from wherever the rules came from: your own feedback, client notes,
code review comments, support tickets.

```
1. "I never ever used the loop arrow. I hate seeing that." (18/06/2026)
2. "I don't like the power ending you've added here." (25/08/2026)
```

This is the part nobody can copy. A stranger can rebuild your layout in an hour. They
cannot produce six dated quotes from inside your own work.

**Never invent a quote.** If you have four real ones, ship four. An entry with four true
citations beats one with six invented, and the difference is visible to anyone reading
carefully.

## Step 4 — Build the chrome

Using a Wikipedia article as the world, four parts, each of which has to be right.

**Left sidebar, about 220px.** The globe mark, the wordmark, then the real navigation in
its real order: Main page, Contents, Featured content, Current events, Random article.
Then an `Interaction` group, then a `Tools` group. Slip ONE of your own links into the
nav. One is funnier than three.

**Article tabs across the top.** Article / Talk on the left. Read / View source / View
history on the right, with a search box. All in `#3366CC`.

**The infobox, floated right, about 390px.** Grey header bar, then a drawn specimen of
the thing you are describing, then a caption, then a `Classification` table.

Draw the specimen in CSS. Do not generate it. It is the one picture on the page and a
generated one will not match the rest.

**Serif for headings, sans for body.** Getting this backwards is the fastest way to make
it look fake.

## Step 5 — The type scale

```
Article title      38px serif
Section heading    23px serif, thin rule underneath
Body and rules     16px sans, line-height 1.35
Infobox            12px sans
Sources            11px sans, italic, two columns
```

Canvas 1080x1350, rendered at 2x for a 2160x2700 PNG. Everything left-aligned.

## Step 6 — Fit it

The last rule must clear the footer. Measure it, do not eyeball it.

If it overflows, in this order: cut a rule, tighten line-height by 0.02, drop the body by
0.4px. Never below 15px on the body.

## Generated or coded, and how to choose

A borrowed world can be generated as an image rather than coded, and often should be. But
realism and correct text trade against each other, and the axis is **word count**.

- **Under about 200 words of short labels** — generate the whole thing. Spell every label
  verbatim in the prompt and close with *"every single word must be real, correctly spelled
  English."*
- **Over that** — generated type returns invented words and drops rows. A twenty-row page
  briefed at about 700 words came back with eleven rows and body text reading `spvertok`,
  with every word spelled correctly in the prompt. No amount of re-prompting fixed it.
- **The hybrid** — generate the document **blank**, with no words on it at all, then set
  every word in HTML on top. Use `mix-blend-mode: multiply` so the ink sits in the surface
  rather than on it. Photoreal texture, correct spelling, any word count.

**The tell that you are over budget is rows going missing.** A generation returning eleven
of twenty items is not a bad seed to re-roll, it is the ceiling.

## Before you ship

- [ ] Every quote in Sources is real and carries a date
- [ ] Every rule fits on one line
- [ ] The last rule clears the footer
- [ ] Nothing is centred
- [ ] Serif on headings, sans on body
- [ ] The specimen is drawn, not generated
- [ ] None of the 29 tells above are in your own graphic

## What breaks it

**Rules that wrap to two lines.** It stops reading as a reference and starts reading as an
article someone wrote.

**Invented citations.** The one thing that cannot be faked is the thing worth having.

**A generated infobox image.** It will not match the CSS around it and it is the first
thing the eye lands on.

**Too much of your own branding.** One nav link and the footer. The format does the work.
