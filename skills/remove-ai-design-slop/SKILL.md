---
name: remove-ai-design-slop
description: >
  Stop your AI-generated graphics looking like everyone else's. Turn a list of rules,
  tells or mistakes into a graphic that looks like a real reference document rather
  than an AI card grid. Use when the user says "my graphics look AI-made", "remove the
  AI slop", "make this look designed", "wikipedia style", "signs of", "anatomy of", or
  has a long list a normal card layout cannot hold. Produces 1080x1350 for LinkedIn or
  Instagram.
tier: Claude free tier at claude.ai. No paid plan, no API key, no install.
outcome: One 1080x1350 graphic holding 20 to 40 rules, that reads as a real reference document instead of an AI card grid.
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
9. Italic only where the borrowed world uses it. Never as your own emphasis.

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

## The prompt

**What you get: one 1080x1350 graphic that reads as a real reference document instead of an
AI card grid, holding 20 to 40 rules on a single canvas.**

**Runs on the free tier of Claude at claude.ai.** No paid plan, no API key, no install. Paste
the prompt, replace the two bracketed blocks, and ask for a screenshot at the end.

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

Ask for a screenshot when it is done, and read it at full size before you use it.

## Step 1 — Get the list

**First, settle what the graphic is ABOUT, because the 29 tells above play two roles and
they are not the same job.**

- **As your QA checklist** they always apply. Whatever you build, it must not commit them.
- **As the SUBJECT** they are the default only when the user has not given you a list. If
  they say "make me one of these" with no content, build the 29 tells themselves. If they
  hand you their own rules, theirs is the subject and the 29 stay a checklist.

Say which one you are doing in a sentence before you go further. Getting this wrong is the
single fastest way to stall.

Then ask for the rules, numbered, shortest first.

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

**This is the hardest step in the skill and it is not a lookup, so here is the method.** The
quote and its date are almost never adjacent. The quote sits in prose and the date sits in a
heading, a commit, a filename or the sentence before it. So search for the QUOTES first and
resolve dates second.

```bash
# 1. every quoted string in your notes, with its file and line
grep -rnoE '[“"][^”"]{25,160}[”"]' <your-notes-dir> | head -60

# 2. for each one you want, read 6 lines either side to find its date
grep -rn -B3 -A3 '<a distinctive phrase from the quote>' <your-notes-dir>
```

**A quote whose date you cannot find does not go in.** Ship four sourced rather than six
half-sourced. Expect to look at roughly three times as many quotes as you keep.

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
Sources            11px sans, two columns
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

## What good looks like

Six things, each of which can come back wrong. Check them on the render, not the code.

1. **Cover the sidebar with your hand. The article still reads as an article.** If it only
   works because of the chrome, the content is too thin.
2. **Every rule sits on one line.** Count the wrapped ones. Any above zero and the graphic
   reads as broken next to the rows that fit.
3. **Every source has a date.** Count them. A quote without one is not a citation, and a
   reader who checks will find that first.
4. **A stranger names the subject in five seconds** from the title and the lead alone.
   Ask someone who has not seen it. If they describe the format instead of the topic, the
   borrowed world has eaten the content.
5. **Nothing is centred, and only the tagline is italic.** Both are things a real Wikipedia
   page gets right and a generated one gets wrong.
6. **The last rule clears the footer.** Measure the gap. Under 10px and it reads as clipped.

**The one that fails most often is 3.** Finding six quote-and-date pairs is real work, and
the temptation is to write a plausible date beside a real quote. Ship four instead.


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
