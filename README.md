# Physics Cheatsheet: CH5–CH6 + Work & Energy

A printable, exam-friendly formula and SI-unit cheatsheet for introductory physics (General Physics), typeset in LaTeX. The content is in Traditional Chinese with English terms alongside.

普通物理 CH5–CH6＋功與能量速查表：依運動類型分類，列出物理量、完整 SI 單位與常用公式，適合 open-book 考試時翻查。

## Download

| Version | File | Best for |
| --- | --- | --- |
| Colour | [`cheatsheet.pdf`](cheatsheet.pdf) | Screen reading, colour printers |
| Black & white | [`cheatsheet-bw.pdf`](cheatsheet-bw.pdf) | Monochrome / laser printers (no grey fills) |

Both are 4 pages of A4, portrait, two columns.

## Contents

| § | Topic |
| --- | --- |
| 0 | 題型判斷 Exam Checklist: which conservation law or formula to reach for, with section references |
| 1 | 直線運動 Linear Motion |
| 2 | 質心 Center of Mass |
| 3 | 動量守恆與碰撞 Momentum & Collisions (elastic, inelastic, 2-D, ballistic pendulum) |
| 4 | 圓周運動 Circular Motion |
| 5 | 轉動運動 Rotational Motion (torque, moment of inertia table, angular momentum) |
| 6 | 彈簧系統 Spring System |
| 7 | 滾動運動 Rolling Motion |
| 8 | 功、能量與功率 Work, Energy & Power |
| 9 | 導出單位完整展開 SI Unit Expansion |

Each section follows the same layout: a table of quantities with full SI units, boxed key formulas, and "注意" notes on the conditions where each formula applies.

The layout is built for quick lookup:

- No section is split across pages or across columns.
- Every derived unit is expanded to SI base units, for example 1 J = 1 N·m = 1 kg·m²/s².

## Building

The document uses XeLaTeX with `xeCJK`. The simplest way to build it is [Tectonic](https://tectonic-typesetting.github.io/), which downloads the packages it needs automatically:

```sh
tectonic cheatsheet.tex      # colour version  -> cheatsheet.pdf
tectonic cheatsheet-bw.tex   # black & white   -> cheatsheet-bw.pdf
```

A TeX Live install works too (`xelatex cheatsheet.tex`, run twice so the page count in the footer resolves).

### Fonts

The default fonts are macOS system fonts:

- **PingFang TC** for Chinese
- **Helvetica Neue** for Latin text

On other systems, change the `\setCJKmainfont`, `\setCJKsansfont` and `\setmainfont` lines at the top of `cheatsheet.tex`. For example, use Noto Sans TC for Chinese and any sans-serif font for Latin text.

### Black & white mode

`cheatsheet-bw.tex` defines `\BW` and then `\input`s `cheatsheet.tex`. All content lives in `cheatsheet.tex`, so edit only that file and rebuild both PDFs.

## License

[MIT](LICENSE)
