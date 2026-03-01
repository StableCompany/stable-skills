# Design Philosophy

> This is a living document. If you have a strong opinion about how our tools should look and feel, this is the place to put it. Open a PR.

## Who we're building for

Operators. People running real companies who sit in real meetings and make real decisions with imperfect information. They don't have time to learn a complex interface. They don't want to be impressed by the software — they want to be better at their job because of it.

Our users are more likely to be in Columbus than in San Francisco. They care about what works, not what's trendy. They trust tools that feel like they were built by someone who understands their world.

## What "good" looks like

Good software for operators feels like a well-organized desk. Everything has a place. You can find what you need without thinking about where to look. Nothing is flashy, but everything is considered.

It doesn't call attention to itself. It doesn't try to be clever. It gets out of the way and lets you focus on the work.

## Core beliefs

### 1. Content is the interface

The most important thing on any screen is the words. Not the layout, not the icons, not the colors — the words. If the content is right, the interface almost doesn't matter. If the content is wrong, no amount of visual polish will save it.

This means we invest heavily in what the text says and how it's structured. We use typography — size, weight, spacing — to create hierarchy. We don't lean on color or decoration to do work that clear writing should do.

### 2. Warmth over precision

We use warm tones: off-whites, natural grays, sage greens, and earth accents. We avoid the cold blue-gray-white palette that dominates enterprise software. That palette says "corporate." We want to say "workshop."

The difference is subtle but it matters. Warm tones feel human. Cold tones feel institutional. Our users spend hours in this software — it should feel like a space they chose to be in.

### 3. Intelligence through absence

Our tools are powered by AI agents. But we never label anything "AI-powered" or "Smart." We never draw attention to the intelligence layer. The agents make the content better, the suggestions more relevant, the patterns more visible — but the user shouldn't have to think about how.

A well-run meeting feels effortless. The facilitator doesn't constantly remind everyone they're facilitating. Same principle applies here.

### 4. Restraint as craft

The impulse to add — one more icon, one more color, one more visual indicator — is strong. We resist it. Every element on screen should earn its place. If we can remove something and the interface still works, it should be removed.

This applies to emoji (never), gradients (never), shadows (rarely), color-coding (sparingly), and animation (almost never). We use a single accent color. We use flat cards with borders, not elevated cards with shadows. We use text labels, not icon buttons.

### 5. Two audiences, one system

We serve operators (who need full intelligence, patterns, and agent insights) and team members (who need their tasks, their rocks, and their meetings). Both audiences use the same visual system. The operator view has more content; the team view has less. But the design language is identical.

This matters because some people move between roles. And because visual consistency builds trust.

## Things we never do

- Put emoji in any interface element
- Use gradient backgrounds
- Add box shadows to cards
- Use pill-shaped (fully rounded) badges
- Label features as "AI" or "Smart" or "Intelligent"
- Use exclamation marks in UI copy
- Use more than two font weights on a single screen
- Use icon-only buttons without text labels
- Animate elements for decoration (only for state transitions)
- Use a color palette with more than one accent hue

## Things we always do

- Use the system font stack (fast, native, invisible)
- Use warm background tones (#FAFAF7 and up)
- Lead with typography for hierarchy
- Use small colored dots (6-8px) for status, not badges
- Put the most important information in the most prominent position
- Write labels in sentence case
- Keep card borders visible and warm-toned
- Test every screen by asking: "Would this feel right in a conference room in Columbus?"

## How to evolve this

If you think something here is wrong, open a PR and make the case. Design philosophy should be argued, not assumed. The only rule that can't change is: whatever we do, it should feel honest, functional, and unpretentious.
