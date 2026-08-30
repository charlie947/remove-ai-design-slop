---
name: remove-ai-design-slop
description: >
  Stop your AI-generated graphics looking like everyone else's. Build the four files that make everything come out on brand, check your work against the 29 tells, and turn a long list into a graphic that reads as a real reference document rather than an AI card grid. Use when the user says "my graphics look AI-made", "remove the AI slop", "make this look designed", "make this on brand", "wikipedia style", "signs of", "anatomy of", or has a long list a normal card layout cannot hold.
tier: Claude free tier at claude.ai. No paid plan, no API key, no install.
outcome: A REFERENCE.md, a DESIGN.md and four lines in CLAUDE.md that make every future graphic come out on brand, plus one 1080x1350 graphic holding 20 to 40 rules.
---

# Remove AI Design Slop

## CRITICAL: Auto-start on load

Ask which of the two jobs this is, in one line, then go. Do not summarise the skill.

**Job one, the system.** The user has no reference file yet. Start at Part One. This is the default when they say their graphics look AI-made, or off brand, or that they are fighting the model about fonts and spacing.

**Job two, the graphic.** The user already has a reference file, or they have a list of 20 to 40 rules and want it built. Skip to Part Three.

## The problem

AI-generated graphics all look the same, and they look the same for a reason. Given no brand reference to read, a model reaches for the same handful of moves every time: a purple-to-blue gradient, a coloured strip down a card edge, emoji standing in for icons, a motivational band across the bottom, and a uniform grid of identical rectangles.

You cannot fix that by prompting harder. The model has nothing of yours to read, so it has nothing to point at.

The fix is not a better prompt. It is a file.

---

# Part One. Build the reference

## Step 0 — Find the thing you already have

Almost everyone has one piece of design that was done properly. A deck a designer built. A brand guideline somebody wrote. A banner. A website. It is sitting in a folder and nobody has ever called it the reference.

That file is the reference. Ask the user what theirs is before anything else.

- **If a designer built it, ask them for the source file.** They will still have it.
- **If it lives in Figma, connect Figma to Claude and point at it directly.** In the Claude desktop app, click the + button by the chat box, hover Connectors, click Manage connectors, hit + next to Connectors, find Figma, and approve the login.
- **Then copy the link to the exact frame, not the file.** Right click the frame in Figma and choose Copy link. Do not take the address out of the browser bar. That link points at one thing instead of an entire filing cabinet, and it is the step everybody misses.
- **If there is no such file, screenshots are enough.** Five pieces of their own work that felt right, in a folder. That is the input for the next step.

## Step 1 — Pull the rules out of the work

Five pieces of design they already like, in a folder called `examples/`. Their best graphics, their banner, their website, a deck they reuse. Screenshots are fine.

Then paste this:

```
I am giving you five pieces of design I already like.

Write me one file called REFERENCE.md that any AI can read before it makes anything for me. It must cover:

1. Every colour as a hex code, and what each one is for
2. The fonts, the sizes, and the spacing between things
3. Where my logo goes and how much clear space it needs
4. Five things my brand must never do
5. One example, described in full, of it done right

Ask me about anything you cannot work out from the files.

Show me the file before you save it.
```

**Sample every hex off the real artefact. Never write one from memory.** Open each screenshot in a colour picker and read the value. A remembered hex is wrong by two or three in one channel, which is invisible to the eye and fails any comparison.

Run this once and the file lasts forever.

## Step 2 — Make Claude read it before it draws

A reference nobody opens is a mood board with extra steps.

```
Add this to CLAUDE.md, and create the file if it does not exist:

Before designing, generating or laying out anything, read REFERENCE.md in full.

Every colour, size and spacing value comes from that file.

If something I ask for is not covered there, ask me rather than choosing for yourself.

When you have finished, check your own output against REFERENCE.md, fix what fails, and only then show me.
```

That last line does more than the other three combined. It makes the model check its own work against the file before anything reaches the user.

## Step 3 — Turn the file into a design system

The reference says what is allowed. A design system says how to build. Different jobs.

```
Read REFERENCE.md and every file in /examples.

Write me DESIGN.md in the project root. It is the build rulebook, not a mood board. Cover:

1. The colour tokens, named by JOB (background, ink, accent, muted), each with its hex
2. The type scale, in real sizes, and which face goes where
3. The spacing scale, as a small set of values I reuse everywhere
4. The components I actually use, with what each one is for
5. A decision log at the bottom, where every choice we make from now on gets recorded

Work from what is IN the reference and the examples. Where they disagree, ask me.

Show me the file before you save it.
```

## The whole system is four files

```
your-project/
  CLAUDE.md        the four lines that make it read everything below
  REFERENCE.md     the rules
  DESIGN.md        the build system
  examples/        five things you were happy with
```

One of them is four lines long. Screenshots in a folder are inspiration. A file it reads first is a system.

## Never accept the first version

Ask for three or four variants and put them side by side. Otherwise you polish whatever came out first, which is the single most expensive habit in AI design.

---

# Part Two. The 29 tells

A tell is what a model reaches for when it has nothing of yours to read. None of these are matters of taste. Every one came out of a real graphic that got rejected, and every one is checkable in about two seconds on a finished render.

**They do two jobs, and mixing them up is what stalls a build.** As a checklist they always apply, whatever you are making. As the SUBJECT of a graphic they are the default only when the user has given you no list of their own. Say which one you are doing in a sentence before going further.

## Colour and type

1. Exactly one accent, used with absolute discipline everywhere it appears.
2. The accent is the subject's colour, never your own house palette.
3. Colour on the glyphs only. Never a fill, tint or pill behind a word.
4. Never two accented phrases, and never a generic word like in or to.
5. Never the purple-to-blue gradient. It is the single loudest tell.
6. Two typefaces, capped there. A third one reads as a template.
7. One type scale in real numbers, never big, medium and small.
8. Monospace is for a string you type or an interface you are drawing.
9. Italic only where the borrowed world uses it, never as your emphasis.

## Delete these on sight

10. The coloured strip down a card edge, top, left, right or bottom.
11. Emoji standing in for drawn icons. Draw the icon or drop it.
12. The loop arrow. Use a plain arrow, or let the motion say it.
13. A motivational band across the bottom. End on the last real row.
14. A bar or meter with no real quantity behind it. Data or nothing.
15. Stock hands on a keyboard, and the robot. Both say nobody chose.

## Layout

16. Every row on a dense list occupies exactly one line. A column where some run to two reads broken.
17. Text evenly weighted. No orphan word alone on a last line, and never a hard break doing the wrapping.
18. Dead space is a content shortage, never a layout fault. You cannot close it by moving it elsewhere.
19. One full sentence per cell is the only thing that fills it. Two words and a chip leaves it half empty.
20. A device starts somewhere and finishes somewhere, never mid-air. A finger traces it without lifting.
21. Arrowheads meet the line they belong to, and the line meets the box it points at, to the pixel.
22. The topic is visible in the drawing, not only in the title. Cover the words and it still says what it is.
23. Never reduce the type size to rescue a fit. Cut a row instead, and say out loud which one you cut.
24. Vary the box sizes. Identical rectangles say none of them matters more than any other.

## What matters most

25. Nobody reads the small text at feed size. They read the shape, and they decide in under two seconds.
26. A clean checklist will pass a build that is still not good. The checklist measures rules, not taste.
27. Never ship the first version. The one that lands is usually the third idea, not the third render.
28. Four variants means four ideas, not one text set three ways in different colours and called a board.
29. One template reused for everybody makes yours look like theirs. Borrow the arrangement, not the skin.

---

# Part Three. Borrow a world

Stopping the tells makes a graphic inoffensive. It does not make it good.

Pick a document everybody already recognises and make the graphic BE that thing: a Wikipedia article, a spreadsheet, a code editor, an inbox, a file tree, a printed spec sheet. The layout arrives pre-trusted, so the reader spends their attention on the content instead of decoding the design, and it stops the scroll because it does not look like a graphic at all.

It also holds far more. Twenty-nine rules, a sidebar, an infobox and six citations fit on one portrait canvas and still read at feed size. A card layout tops out around twelve.

**It only works if it is accurate.** One wrong element and it reads as a template.

| World | Fits a subject that is | What has to be right |
|---|---|---|
| Wikipedia article | a body of rules, tells or definitions | sidebar nav in its real order, Article and Talk tabs, a floated infobox, citations |
| Spreadsheet | numbers, comparisons, a running total | column letters, row numbers, the formula bar, one selected cell |
| Code editor | a config, a file, a set of settings | the file tree, line numbers, real syntax colours, a status bar |
| Inbox | a sequence of messages, or a triage system | a sender column, timestamps, unread weight, a folder rail |
| File tree | a folder structure or a system layout | indent guides, real file extensions, a collapsed folder or two |
| Printed spec sheet | specifications, a datasheet, a comparison | a part number, a revision, a units column, small print |

## The prompt

What you get: one 1080x1350 graphic that reads as a real reference document instead of an AI card grid, holding 20 to 40 rules on a single canvas.

Runs on the free tier of Claude at claude.ai. No paid plan, no API key, no install. Paste the prompt, replace the two bracketed blocks, and ask for a screenshot at the end.

```
<role>
You are a designer who builds reference-document graphics. You care more about a
stranger understanding the whole thing in five seconds than about how it looks.
</role>

<context>
AI-generated graphics all look the same because a model with no brand reference to
read reaches for the same moves every time. I want the opposite: a graphic that looks
like a document the reader already trusts, so the layout does the persuading and they
spend their attention on the content.
</context>

<subject>
[PASTE YOUR 20-40 RULES HERE, one per line. If you have none, use the 29 tells that
ship with this skill as the subject.]
</subject>

<sources>
[PASTE 4-6 REAL QUOTES, each with a date, from wherever these rules came from:
your own feedback, client notes, code review comments, support tickets.
If you have fewer than four, paste what you have. Never invent one.]
</sources>

<examples>
Three subjects that all work, to show the range. Yours goes in the same slot.

<example>
Subject: design tells. Sections: Colour and type, Things to delete, Layout.
Rule: "Never the purple-to-blue gradient."
Source: "I never ever used the loop arrow. I hate seeing that." (18/06/2026)
</example>

<example>
Subject: onboarding mistakes at a SaaS company. Sections: Signup, First session, Week one.
Rule: "The welcome email arrives before the account is provisioned."
Source: "I clicked the button in the email and it 404'd." (support ticket, 04/03/2026)
</example>

<example>
Subject: a glossary of terms a new hire keeps mishearing. Sections: Money, People, Process.
Rule: "ARR is booked revenue, not cash in the bank."
Source: "I assumed ARR meant we had it in the account." (onboarding call, 11/01/2026)
</example>
</examples>

<task>
Build a single 1080x1350 HTML page that reads as a genuine Wikipedia article.

1. Group my rules into four to six sections. Name each one as a plain noun phrase,
   no verbs and no wit. Number the rules continuously across all sections.
2. Draw the chrome accurately. Left sidebar about 220px with the globe, the wordmark
   and the real navigation in its real order. Article and Talk tabs on the left, with
   Read / View source / View history on the right. An infobox floated right at about
   390px with a grey header and a Classification table.
3. Put my sources in a final numbered section, each quote with its date.
4. Use a serif for the article title and section headings, and a sans for body text.
   Left-align everything.
5. Type scale: title 38px, headings 23px, body 16px at line-height 1.35, infobox 12px,
   sources 11px.
6. Colours: link blue #3366CC, rules #A2A9B1, infobox header #EAECF0, ink #202122.
</task>

<checks>
Run every check and print the result. If one fails, fix it and re-check.
- Every rule renders on ONE line. Count any that wrap to two. Must be zero.
- The last rule's bottom edge sits above the footer. Report the gap in pixels.
- Every quote in the sources section has a date beside it. Report the count.
- Nothing is centred. Report any text-align that is not left.
- No element extends past 1080 wide or 1350 tall. Report the largest overflow.
- Italic appears only where a real Wikipedia page uses it. List every italic element.
</checks>

<constraints>
Use only the sources I gave you. Do not invent a quote, a date or a citation.
If a rule wraps to two lines, shorten the rule rather than shrinking the type.
Keep the body at 15px or larger.
</constraints>
```

Ask for a screenshot when it is done, and read it at full size before using it.

**If they have a REFERENCE.md from Part One, add one line to the task block:** `Take every colour and every type value from REFERENCE.md rather than the ones listed above.` The borrowed world stays the same; the palette becomes theirs.

## Getting the list right

Each rule is one line, one sentence, under about 70 characters. If a rule needs two lines the illusion breaks and it starts to look like a blog post.

Twenty to forty is the range. Under fifteen, use cards. Over forty, the type drops below readable.

Sections get named the way a reference document would: a plain noun phrase, no verbs, no wit. `Colour and type`, `Things to delete`, `Layout`. The last section is always Sources.

If the user hands over a paragraph, cut it into single-line rules and show them the list before building anything.

## The Sources block is the proof

Real reference documents carry citations. Yours carries direct quotes with dates.

Pull them from wherever the rules came from: their own feedback, client notes, code review comments, support tickets.

This is the hardest step in the skill and it is not a lookup. The quote and its date are almost never adjacent. The quote sits in prose and the date sits in a heading, a commit, a filename or the sentence before it. So search for the quotes first and resolve dates second.

```bash
# 1. every quoted string in your notes, with its file and line
grep -rnoE '["][^"]{25,160}["]' <your-notes-dir> | head -60

# 2. for each one you want, read 3 lines either side to find its date
grep -rn -B3 -A3 '<a distinctive phrase from the quote>' <your-notes-dir>
```

A quote whose date you cannot find does not go in. Ship four sourced rather than six half-sourced. Expect to look at roughly three times as many quotes as you keep.

Never invent one. An entry with four true citations beats one with six invented, and the difference is visible to anyone reading carefully.

This is the part nobody can copy. A stranger can rebuild the layout in an hour. They cannot produce six dated quotes from inside someone else's work.

## Build the chrome

Four parts, each of which has to be right.

**Left sidebar, about 220px.** The globe mark, the wordmark, then the real navigation in its real order: Main page, Contents, Featured content, Current events, Random article. Then an `Interaction` group, then a `Tools` group. Slip one of the user's own links into the nav. One is funnier than three.

**Article tabs across the top.** Article and Talk on the left. Read, View source and View history on the right, with a search box. All in `#3366CC`.

**The infobox, floated right, about 390px.** Grey header bar, then a drawn specimen of the thing being described, then a caption, then a `Classification` table.

Draw the specimen in CSS. Do not generate it. It is the one picture on the page and a generated one will not match the rest.

**Serif for headings, sans for body.** Getting this backwards is the fastest way to make it look fake.

## The type scale

```
Article title      38px serif
Section heading    23px serif, thin rule underneath
Body and rules     16px sans, line-height 1.35
Infobox            12px sans
Sources            11px sans, two columns
```

Canvas 1080x1350, rendered at 2x for a 2160x2700 PNG. Everything left-aligned.

## Fit it

The last rule must clear the footer. Measure it, do not eyeball it.

If it overflows, in this order: cut a rule, tighten line-height by 0.02, drop the body by 0.4px. Never below 15px on the body.

---

# Generated or coded, and how to choose

A borrowed world can be generated as an image rather than coded, and often should be. But realism and correct text trade against each other, and the axis is word count, not prompt quality.

- **Under about 200 words of short labels** — generate the whole thing. Spell every label verbatim in the prompt and close with "every single word must be real, correctly spelled English."
- **Over that** — generated type returns invented words and drops rows. A twenty-row page briefed at about 700 words came back with eleven rows and body text reading `spvertok`, with every word spelled correctly in the prompt. No amount of re-prompting fixed it.
- **The hybrid** — generate the document blank, with no words on it at all, then set every word in HTML on top. Use `mix-blend-mode: multiply` so the ink sits in the surface rather than on it. Photoreal texture, correct spelling, any word count.

The tell that you are over budget is rows going missing. A generation returning eleven of twenty items is not a bad seed to re-roll, it is the ceiling.

---

# What good looks like

Six things, each of which can come back wrong. Check them on the render, not the code.

1. **Cover the sidebar with your hand. The article still reads as an article.** If it only works because of the chrome, the content is too thin.
2. **Every rule sits on one line.** Count the wrapped ones. Any above zero and the graphic reads as broken next to the rows that fit.
3. **Every source has a date.** Count them. A quote without one is not a citation, and a reader who checks will find that first.
4. **A stranger names the subject in five seconds** from the title and the lead alone. Ask someone who has not seen it. If they describe the format instead of the topic, the borrowed world has eaten the content.
5. **Nothing is centred, and only the tagline is italic.** Both are things a real Wikipedia page gets right and a generated one gets wrong.
6. **The last rule clears the footer.** Measure the gap. Under 10px and it reads as clipped.

The one that fails most often is 3. Finding six quote-and-date pairs is real work, and the temptation is to write a plausible date beside a real quote. Ship four instead.

## Before you ship

- [ ] REFERENCE.md exists and every colour in it was sampled, not remembered
- [ ] CLAUDE.md carries the four lines, and the last one is the check line
- [ ] Every quote in Sources is real and carries a date
- [ ] Every rule fits on one line
- [ ] The last rule clears the footer
- [ ] Nothing is centred
- [ ] Serif on headings, sans on body
- [ ] The specimen is drawn, not generated
- [ ] Three or four variants were made, not one
- [ ] None of the 29 tells above are in your own graphic

## What breaks it

**No reference file.** Everything in Part Two and Part Three is downstream of Part One. A perfect layout in the wrong colours is still off brand.

**Rules that wrap to two lines.** It stops reading as a reference and starts reading as an article somebody wrote.

**Invented citations.** The one thing that cannot be faked is the thing worth having.

**A generated infobox image.** It will not match the CSS around it and it is the first thing the eye lands on.

**Too much of your own branding.** One nav link and the footer. The format does the work.
