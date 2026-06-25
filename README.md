# 🎭 mask — write in the unmistakable voice of a famous character

**English** | [中文](./README.zh.md)

> One sentence, many masks, many voices. Kill the "AI tone" for good.

AI-written copy always has a tell: too stiff or too soft, never the lived-in voice of a real person with an actual personality.

`mask` is a [Claude Code](https://claude.com/claude-code) skill. You ask it to write or rewrite copy *in the voice of* a character, and it pulls that character's **linguistic fingerprint** (self-reference, catchphrases, sentence rhythm, diction) so the output is instantly recognizable.

## See it in one glance

The same flat line — **"Thanks everyone for joining today, you all worked hard, let's talk again next time."**

| Mask | Rewritten |
|---|---|
| 🕵️ **Sherlock Holmes** | Thank you — though I observe the real work has scarcely begun. The untouched agenda, the two who slipped out early: we reconvene, and next time we finish what we start. Elementary. |
| 🟢 **Yoda** | Grateful, I am. Worked hard today, you all have. Meet again, we shall — much left to do, there is. Hmm. |
| 🎭 **Shakespeare** | I thank thee, gentles all, for this day's labour. 'Tis but a pause, not an end; anon we shall convene again, and speak further upon these matters. |

> Chinese audience? See the [中文 README](./README.zh.md) for the 西游记 / 红楼梦 / 三国 / 水浒 characters.

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

## License

[MIT](./LICENSE)
