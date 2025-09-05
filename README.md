# Cursor Writing

Rules that help AI write like a human: clear, direct, and specific. The rules live in `.cursor/rules/Writing.mdc` and can be used in Cursor or any other AI tool.

## what this is

`Writing.mdc` contains concise guidelines for:

- sentence structure
- voice and tone
- specificity and evidence
- title creation
- banned words and phrases
- patterns that make text sound like an AI
- punctuation and formatting

Use it to draft, edit, and rewrite blog posts, docs, and social posts without the usual AI telltales.

## quick start in Cursor

The repo already includes `.cursor/rules/Writing.mdc` with `alwaysApply: true`; Cursor will apply the rules to all chats in this workspace.

If you copy this into another project:

1. Create the directory: `.cursor/rules/`.
2. Put `Writing.mdc` inside it.
3. Keep the YAML header as is, or set `alwaysApply: true` to enable it by default.

## use with any AI (ChatGPT, Claude, others)

The top of `Writing.mdc` has a short YAML header used by Cursor. When you use the rules outside Cursor, remove those first four lines.

### copy the trimmed rules

On macOS you can copy the rules to your clipboard without the header:

```bash
curl -s https://raw.githubusercontent.com/jfilatow/cursor-writing/main/.cursor/rules/Writing.mdc \
  | sed '1,4d' \
  | pbcopy
# Now paste into your AI tool's system prompt or custom instructions
```

### ChatGPT

Use Custom Instructions or a new chat with a system message. Paste the trimmed rules after this lead-in:

```text
Role: editor. Enforce the following writing rules as hard constraints. Apply them to all drafts and rewrites. Do not restate the rules. Fix issues directly and keep facts intact. Keep sentences short and scannable.

[paste the trimmed rules here]
```

### Claude

Use a Project system prompt or the conversation-level system message. Paste the same trimmed rules with a short lead-in:

```text
You are my writing editor. Follow the rules below exactly; prefer simple, direct prose; remove filler; avoid AI-sounding phrases.

[paste the trimmed rules here]
```

### other tools

Any model that accepts a system prompt will work. Paste the trimmed rules at the top of the prompt, then ask for a draft or rewrite.

## example workflows

- draft: “Write a 600–800 word post about <topic>. Follow the rules above. Use sentence casing for headings, concrete examples, and data.”
- edit: “Rewrite the text below to follow the rules above; preserve meaning, structure, and links.”
- tighten: “Shorten the draft by 20%, remove hedging and filler, and keep key details.”

## contribute

This repo should evolve. Open issues and pull requests with:

- new rules that catch AI-sounding habits (cliché intros, needless hedging, overuse of transitions)
- small, precise wording tweaks
- examples that show bad vs good

Please keep sentence casing, short bullets, and consistent style. Explain why a change helps, and include one concrete example.

## credits

The rule set was reconstructed from public screenshots to make it easier to use across tools. If you have additions or corrections, propose them in a PR.

## attribution

- Original author: [Lee Robinson](https://github.com/leerob).
- Context: shared in a video conversation with Greg Isenberg (link pending; add here when available).
- Note: Five short bullets under `## Sentence structure` were inferred because they were not visible in the screenshots. They match the surrounding guidance but may differ slightly from the source. If Lee can share the exact wording, we’ll update the file.

If you know the canonical source or have the exact lines, please open an issue.

• Issues: https://github.com/jfilatow/cursor-writing/issues


