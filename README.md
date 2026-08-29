# root-first

A Claude skill for learning technical concepts the way your brain actually remembers them: **root first, definition second.**

Most technical and programming terms weren't invented in a vacuum — they were borrowed from everyday physical life, ancient languages, and ordinary human tools, then repurposed once someone needed a word for a new idea. `root-first` digs up that original, concrete meaning before you ever touch the technical definition, so the concept clicks instead of just being memorized.

## Usage

```
/root-first <word>
```

That's it. Give it any word or term you're about to learn — `interface`, `polymorphism`, `harness`, `agent`, whatever — and it does the rest.

## What it actually does

1. Searches the web (etymonline.com first) for the word's real etymology
2. Breaks the word down into its root pieces and tells you what each one literally meant
3. Tells you the word's original, literal meaning — before it ever became a technical term
4. Flags the moment (if there was one) where the word turned figurative/abstract
5. Reconstructs the mental image the person who coined or chose the word probably had in their head
6. Then asks you two questions:
   - **Which domain** do you want to see this concept applied in? It'll explain the concept *in that domain*, explicitly tying it back to the root meaning it just gave you — not a generic dictionary definition.
   - **Is there another concept** you want to compare it against? It'll run the full process on that word too, and then spell out exactly how the two relate.

## Example: `harness`

```
/root-first harness
```

**root-first** traces `harness` back through Old French to a Germanic root roughly meaning "military gear, equipment for a horse" — the original picture is very literal: straps and gear **strapped onto** an animal so it can pull a load or do its job. Its response ends with something like:

> **What was in the coiner's head?**
> The mental picture is simple: **strapping equipment onto something so it can do its job** — like harnessing a horse so it can pull a cart.

Then it asks:

> - Given the root meaning I just gave you for "harness," which domain do you want to see this concept applied in?
> - Is there another concept you'd like to compare against "harness"?

Say **"AI"**, and it explains what an *AI harness* is — the scaffolding of prompts, tools, and context that lets a model actually get work done — while explicitly pointing back to that same "strapping gear onto something so it can pull its load" image. Suddenly a phrase like *"customize your agent with extensions, skills, and prompt templates"* reads less like jargon and more like exactly what the word always meant: harness it up, give it the gear, let it work.

Say **"agent"** for the comparison question, and it traces `agent`'s roots too (Latin *agere*, "to do, to drive, to set in motion"), then lays out the connection: an *agent* is the one doing the work — the horse — while a *harness* is the gear that lets it do that work effectively. Two words, two root images, one picture once you put them side by side.

## Why bother

If you've ever learned a term like `abstraction` or `encapsulation` and it felt like an arbitrary label you just had to memorize — this is the fix. Almost every one of these words has a concrete, physical origin story, and once you see it, the "arbitrary" label turns into the *only* word that could've possibly been chosen.

## Installation

Copy `SKILL.md` into your Claude skills folder, or load it as a `.skill` package. Once installed, just type `/root-first <word>` in any conversation.
