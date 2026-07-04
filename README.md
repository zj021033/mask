# 🎭 mask — make AI copy stop sounding like AI

**English** | [中文](./README.zh.md)

> One sentence, many masks, many voices. A Claude Code skill for rewriting bland AI copy with recognizable character-level linguistic fingerprints.

[Install](#install) · [Try it](#try-it-in-20-seconds) · [Characters](#characters-v110) · [Contribute](#want-a-character-thats-missing-contribute)

If this makes one piece of AI copy feel human, star the repo so more writers and builders can find it.

AI-written copy always has a tell: too stiff or too soft, never the lived-in voice of a real person with an actual personality.

`mask` is a [Claude Code](https://claude.com/claude-code) skill. You ask it to write or rewrite copy *in the voice of* a character, and it pulls that character's **linguistic fingerprint** (self-reference, catchphrases, sentence rhythm, diction) so the output is instantly recognizable.

## Install

Fastest path:

```bash
npx skills add zj021033/mask --skill mask
```

```bash
git clone https://github.com/zj021033/mask ~/.claude/skills/mask
```

Update later:

```bash
cd ~/.claude/skills/mask && git pull
```

Single-file install:

```bash
mkdir -p ~/.claude/skills/mask
curl -o ~/.claude/skills/mask/SKILL.md \
  https://raw.githubusercontent.com/zj021033/mask/main/SKILL.md
```

For Cursor, Codex-style CLI agents, Gemini CLI, or plain chat, paste [`SKILL.md`](./SKILL.md) into your rules / `AGENTS.md` / system prompt.

## See it in one glance

The same flat line — **"Thanks everyone for joining today, you all worked hard, let's talk again next time."**

| Mask | Rewritten |
|---|---|
| 🕵️ **Sherlock Holmes** | Thank you — though I observe the real work has scarcely begun. The untouched agenda, the two who slipped out early: we reconvene, and next time we finish what we start. Elementary. |
| 🟢 **Yoda** | Grateful, I am. Worked hard today, you all have. Meet again, we shall — much left to do, there is. Hmm. |
| 🎭 **Shakespeare** | I thank thee, gentles all, for this day's labour. 'Tis but a pause, not an end; anon we shall convene again, and speak further upon these matters. |

> Chinese audience? See the [中文 README](./README.zh.md) for the 西游记 / 红楼梦 / 三国 / 水浒 characters.

More examples:

- [Same line, five masks](./examples/same-line-five-masks.md)

## Try it in 20 seconds

After installing, paste one of these:

```text
write like Sherlock Holmes: Thanks for waiting. The new version is ready, and we fixed the bug you reported.
```

```text
rewrite this in the voice of Yoda: We need to slow down, check the logs, and avoid guessing.
```

```text
draft a product launch note as Shakespeare. Make it short.
```

The point is not "make it funny." The point is to preserve meaning while replacing generic AI phrasing with a concrete voice.

## How to use

After installing, just tell Claude Code:

```
write like Sherlock Holmes: <your copy>
rewrite this in the voice of Yoda: <your copy>
draft a thank-you note as Shakespeare
```

Two modes: **write fresh** or **rewrite** (keep the meaning, swap the voice).

## Characters (v1.1.0)

**English:** Sherlock Holmes · Yoda · Shakespeare

**中文 (Chinese):** 孙悟空 · 猪八戒 · 唐僧 · 牛魔王 · 红孩儿 · 林黛玉 · 王熙凤 · 张飞 · 诸葛亮 · 鲁智深

> Match the language to the culture: Chinese copy uses the Chinese characters; English copy uses the English ones.
> Roadmap: more Western voices (detectives, wizards, pirates…) and the rest of the Chinese classics.

## Design idea: store the *fingerprint*, not the *label*

"Sherlock: smart, arrogant" gives you nothing — that's a personality label. What makes a voice recognizable is the concrete linguistic trace: the clipped deduction, "you see but you do not observe," the inferential chain.

So every profile centers on **linguistic fingerprint + real quotes (source-labeled) + a before/after rewrite demo**. Quotes are only kept if they're verifiable canon or widely-known popular lines, each marked with its source.

## Want a character that's missing? Contribute 🙌

Three steps, template included:

1. Add `<character>.md` under `personas/<source>/`, following the template in [`SKILL.md`](./SKILL.md).
2. Add a row to the character index in `SKILL.md`.
3. Bump `VERSION` and add a `CHANGELOG.md` line.

Label your sources. Open a PR — let's grow the mask library together.

Good first contributions:

- Public-domain literary characters
- Regional / historical voices with clear source material
- More before/after examples for existing characters
- Shorter, sharper persona files that improve recognizability

## License

[MIT](./LICENSE)
