# 六十四卦速查表 · 64-Hexagram Lookup Reference

Companion reference for the double check in [`INSTRUCTIONS.zh-CN.md`](../INSTRUCTIONS.zh-CN.md). It uses the **King Wen (文王) sequence**, the default order named in the specification. The supplied specification does not embed this table; it is provided here so that either lookup path (A or B) can be checked by hand or by an implementation.

## How to read it

- Lines are read **bottom to top**. Yang ⚊ = `1`, yin ⚋ = `0`.
- The **lower trigram** is lines 1–3 and the **upper trigram** is lines 4–6, each read bottom to top.
- For a casting, use the polarity of each line **before** change for the 本卦 and **after** change (6 → yang, 9 → yin) for the 之卦.

## Trigram bits (bottom to top)

| Trigram | Symbol | English | Bits | Lines |
|---|---|---|---|---|
| 乾 | ☰ | Heaven | `111` | ⚊⚊⚊ |
| 兑 | ☱ | Lake | `110` | ⚊⚊⚋ |
| 离 | ☲ | Fire | `101` | ⚊⚋⚊ |
| 震 | ☳ | Thunder | `100` | ⚊⚋⚋ |
| 巽 | ☴ | Wind | `011` | ⚋⚊⚊ |
| 坎 | ☵ | Water | `010` | ⚋⚊⚋ |
| 艮 | ☶ | Mountain | `001` | ⚋⚋⚊ |
| 坤 | ☷ | Earth | `000` | ⚋⚋⚋ |

## Check B: upper × lower trigram matrix

Rows are the **upper** trigram (lines 4–6); columns are the **lower** trigram (lines 1–3). Each cell is *number 名*.

| 上＼下 | 乾 ☰ | 兑 ☱ | 离 ☲ | 震 ☳ | 巽 ☴ | 坎 ☵ | 艮 ☶ | 坤 ☷ |
|---|---|---|---|---|---|---|---|---|
| **乾 ☰** | 1 乾 | 10 履 | 13 同人 | 25 无妄 | 44 姤 | 6 讼 | 33 遁 | 12 否 |
| **兑 ☱** | 43 夬 | 58 兑 | 49 革 | 17 随 | 28 大过 | 47 困 | 31 咸 | 45 萃 |
| **离 ☲** | 14 大有 | 38 睽 | 30 离 | 21 噬嗑 | 50 鼎 | 64 未济 | 56 旅 | 35 晋 |
| **震 ☳** | 34 大壮 | 54 归妹 | 55 丰 | 51 震 | 32 恒 | 40 解 | 62 小过 | 16 豫 |
| **巽 ☴** | 9 小畜 | 61 中孚 | 37 家人 | 42 益 | 57 巽 | 59 涣 | 53 渐 | 20 观 |
| **坎 ☵** | 5 需 | 60 节 | 63 既济 | 3 屯 | 48 井 | 29 坎 | 39 蹇 | 8 比 |
| **艮 ☶** | 26 大畜 | 41 损 | 22 贲 | 27 颐 | 18 蛊 | 4 蒙 | 52 艮 | 23 剥 |
| **坤 ☷** | 11 泰 | 19 临 | 36 明夷 | 24 复 | 46 升 | 7 师 | 15 谦 | 2 坤 |

## Check A: six-line pattern table

Pattern is bottom to top (line 1 first). 上 = upper trigram, 下 = lower trigram.

| # | 卦 | 名 | Pinyin | English (common rendering) | Pattern | 上 | 下 |
|--:|:-:|---|---|---|---|---|---|
| 1 | ䷀ | 乾 | Qián | The Creative | `111111` | 乾 ☰ | 乾 ☰ |
| 2 | ䷁ | 坤 | Kūn | The Receptive | `000000` | 坤 ☷ | 坤 ☷ |
| 3 | ䷂ | 屯 | Zhūn | Difficulty at the Beginning | `100010` | 坎 ☵ | 震 ☳ |
| 4 | ䷃ | 蒙 | Méng | Youthful Folly | `010001` | 艮 ☶ | 坎 ☵ |
| 5 | ䷄ | 需 | Xū | Waiting | `111010` | 坎 ☵ | 乾 ☰ |
| 6 | ䷅ | 讼 | Sòng | Conflict | `010111` | 乾 ☰ | 坎 ☵ |
| 7 | ䷆ | 师 | Shī | The Army | `010000` | 坤 ☷ | 坎 ☵ |
| 8 | ䷇ | 比 | Bǐ | Holding Together | `000010` | 坎 ☵ | 坤 ☷ |
| 9 | ䷈ | 小畜 | Xiǎo Xù | Small Taming | `111011` | 巽 ☴ | 乾 ☰ |
| 10 | ䷉ | 履 | Lǚ | Treading | `110111` | 乾 ☰ | 兑 ☱ |
| 11 | ䷊ | 泰 | Tài | Peace | `111000` | 坤 ☷ | 乾 ☰ |
| 12 | ䷋ | 否 | Pǐ | Standstill | `000111` | 乾 ☰ | 坤 ☷ |
| 13 | ䷌ | 同人 | Tóng Rén | Fellowship | `101111` | 乾 ☰ | 离 ☲ |
| 14 | ䷍ | 大有 | Dà Yǒu | Great Possession | `111101` | 离 ☲ | 乾 ☰ |
| 15 | ䷎ | 谦 | Qiān | Modesty | `001000` | 坤 ☷ | 艮 ☶ |
| 16 | ䷏ | 豫 | Yù | Enthusiasm | `000100` | 震 ☳ | 坤 ☷ |
| 17 | ䷐ | 随 | Suí | Following | `100110` | 兑 ☱ | 震 ☳ |
| 18 | ䷑ | 蛊 | Gǔ | Work on the Decayed | `011001` | 艮 ☶ | 巽 ☴ |
| 19 | ䷒ | 临 | Lín | Approach | `110000` | 坤 ☷ | 兑 ☱ |
| 20 | ䷓ | 观 | Guān | Contemplation | `000011` | 巽 ☴ | 坤 ☷ |
| 21 | ䷔ | 噬嗑 | Shì Kè | Biting Through | `100101` | 离 ☲ | 震 ☳ |
| 22 | ䷕ | 贲 | Bì | Grace | `101001` | 艮 ☶ | 离 ☲ |
| 23 | ䷖ | 剥 | Bō | Splitting Apart | `000001` | 艮 ☶ | 坤 ☷ |
| 24 | ䷗ | 复 | Fù | Return | `100000` | 坤 ☷ | 震 ☳ |
| 25 | ䷘ | 无妄 | Wú Wàng | Innocence | `100111` | 乾 ☰ | 震 ☳ |
| 26 | ䷙ | 大畜 | Dà Chù | Great Taming | `111001` | 艮 ☶ | 乾 ☰ |
| 27 | ䷚ | 颐 | Yí | Nourishment | `100001` | 艮 ☶ | 震 ☳ |
| 28 | ䷛ | 大过 | Dà Guò | Great Excess | `011110` | 兑 ☱ | 巽 ☴ |
| 29 | ䷜ | 坎 | Kǎn | The Abysmal | `010010` | 坎 ☵ | 坎 ☵ |
| 30 | ䷝ | 离 | Lí | The Clinging | `101101` | 离 ☲ | 离 ☲ |
| 31 | ䷞ | 咸 | Xián | Influence | `001110` | 兑 ☱ | 艮 ☶ |
| 32 | ䷟ | 恒 | Héng | Duration | `011100` | 震 ☳ | 巽 ☴ |
| 33 | ䷠ | 遁 | Dùn | Retreat | `001111` | 乾 ☰ | 艮 ☶ |
| 34 | ䷡ | 大壮 | Dà Zhuàng | Great Power | `111100` | 震 ☳ | 乾 ☰ |
| 35 | ䷢ | 晋 | Jìn | Progress | `000101` | 离 ☲ | 坤 ☷ |
| 36 | ䷣ | 明夷 | Míng Yí | Darkening of the Light | `101000` | 坤 ☷ | 离 ☲ |
| 37 | ䷤ | 家人 | Jiā Rén | The Family | `101011` | 巽 ☴ | 离 ☲ |
| 38 | ䷥ | 睽 | Kuí | Opposition | `110101` | 离 ☲ | 兑 ☱ |
| 39 | ䷦ | 蹇 | Jiǎn | Obstruction | `001010` | 坎 ☵ | 艮 ☶ |
| 40 | ䷧ | 解 | Xiè | Deliverance | `010100` | 震 ☳ | 坎 ☵ |
| 41 | ䷨ | 损 | Sǔn | Decrease | `110001` | 艮 ☶ | 兑 ☱ |
| 42 | ䷩ | 益 | Yì | Increase | `100011` | 巽 ☴ | 震 ☳ |
| 43 | ䷪ | 夬 | Guài | Breakthrough | `111110` | 兑 ☱ | 乾 ☰ |
| 44 | ䷫ | 姤 | Gòu | Coming to Meet | `011111` | 乾 ☰ | 巽 ☴ |
| 45 | ䷬ | 萃 | Cuì | Gathering Together | `000110` | 兑 ☱ | 坤 ☷ |
| 46 | ䷭ | 升 | Shēng | Pushing Upward | `011000` | 坤 ☷ | 巽 ☴ |
| 47 | ䷮ | 困 | Kùn | Oppression | `010110` | 兑 ☱ | 坎 ☵ |
| 48 | ䷯ | 井 | Jǐng | The Well | `011010` | 坎 ☵ | 巽 ☴ |
| 49 | ䷰ | 革 | Gé | Revolution | `101110` | 兑 ☱ | 离 ☲ |
| 50 | ䷱ | 鼎 | Dǐng | The Cauldron | `011101` | 离 ☲ | 巽 ☴ |
| 51 | ䷲ | 震 | Zhèn | The Arousing | `100100` | 震 ☳ | 震 ☳ |
| 52 | ䷳ | 艮 | Gèn | Keeping Still | `001001` | 艮 ☶ | 艮 ☶ |
| 53 | ䷴ | 渐 | Jiàn | Development | `001011` | 巽 ☴ | 艮 ☶ |
| 54 | ䷵ | 归妹 | Guī Mèi | The Marrying Maiden | `110100` | 震 ☳ | 兑 ☱ |
| 55 | ䷶ | 丰 | Fēng | Abundance | `101100` | 震 ☳ | 离 ☲ |
| 56 | ䷷ | 旅 | Lǚ | The Wanderer | `001101` | 离 ☲ | 艮 ☶ |
| 57 | ䷸ | 巽 | Xùn | The Gentle | `011011` | 巽 ☴ | 巽 ☴ |
| 58 | ䷹ | 兑 | Duì | The Joyous | `110110` | 兑 ☱ | 兑 ☱ |
| 59 | ䷺ | 涣 | Huàn | Dispersion | `010011` | 巽 ☴ | 坎 ☵ |
| 60 | ䷻ | 节 | Jié | Limitation | `110010` | 坎 ☵ | 兑 ☱ |
| 61 | ䷼ | 中孚 | Zhōng Fú | Inner Truth | `110011` | 巽 ☴ | 兑 ☱ |
| 62 | ䷽ | 小过 | Xiǎo Guò | Small Excess | `001100` | 震 ☳ | 艮 ☶ |
| 63 | ䷾ | 既济 | Jì Jì | After Completion | `101010` | 坎 ☵ | 离 ☲ |
| 64 | ䷿ | 未济 | Wèi Jì | Before Completion | `010101` | 离 ☲ | 坎 ☵ |

## Verification

Checked by script when this file was produced:

- 64 distinct six-line patterns and 64 distinct (upper, lower) trigram pairs, so every cell above appears exactly once.
- The trigram bit patterns match Appendix 1 of the specification.
- King Wen pairing structure holds for all 32 consecutive pairs (1–2, 3–4, …): the second hexagram of each pair is the first turned upside down, or its complement when the pattern is symmetric.
- Hexagrams 12 (否) and 16 (豫) match the [worked example](../examples/github-meaningful-content-before-2028.md), which was checked against published references.
- Hexagrams 3, 9, 29, 41, 49, 55, 61, 63 and 64 were spot-checked against the six-line patterns on the [YiAtlas King Wen reference](https://yiatlas.com/en/hexagrams); all nine matched.

These checks catch table-construction errors; they do not make an independent source of truth. The English column gives short renderings adapted from common translations; wording varies between editions, so rely on the number, Chinese name and pattern, not the English wording. For authoritative text, consult a published edition.
