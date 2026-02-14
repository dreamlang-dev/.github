# Dream Software Foundation

**Engineering the last programming language.**

---

The Dream Software Foundation (DSF) stewards [Dream](https://dreamlang.dev) -- a programming language designed to unify formal verification, automatic parallelism, content-addressable code, and AI-native tooling into a single coherent system.

Everything the DSF produces is open source under the Apache 2.0 + MIT dual license.

## What is Dream?

Dream occupies a space that no existing language fills. Most languages force a choice: safety or speed, verification or usability, parallelism or simplicity. Dream's thesis is that these are false dichotomies created by historical accident, not fundamental tradeoffs.

**Type system.** Quantitative Type Theory with usage tracking ({0, 1, w} for erased, linear, and unrestricted bindings), row-polymorphic algebraic effects, SMT-backed refinement types, session types, and gradual verification via the `?` operator -- any spec can defer to runtime checking where full proofs are impractical.

**Execution model.** Hybrid -- interaction combinators (HVM2-style) for automatic GPU parallelism of pure code, BEAM-inspired lightweight actors for effectful and stateful concurrency. The runtime chooses the strategy. The programmer writes the logic.

**Code identity.** Content-addressable definitions identified by SHA3-512 hash of normalized AST. Code is stored in a content-addressable database, not text files. Rename a function and nothing breaks. Move a definition between modules and the hash stays the same.

**Compilation targets.** JavaScript + TypeScript declarations (web), WebAssembly Components + WIT (interop), SPIR-V / WGSL / PTX (GPU compute), native via LLVM (release builds) and a fast self-hosted backend (debug builds), freestanding bare-metal (embedded).

**AI-native design.** Compiler-as-library API for constrained decoding, typed holes for AI code generation, structured JSON error messages, explicit types over inference, Result types over exceptions. Dream treats AI tooling as a first-class design constraint, not an afterthought.

## Governance

Dream follows the **Language Designer + AI Deliberation** model. A single Language Designer holds final authority over all design decisions. Every decision must be published with written rationale that engages the strongest counterarguments.

Language evolution happens through **DEPs** (Dream Enhancement Proposals). What makes the DEP process unusual is that AI deliberation runs at every transition -- not as a single gate, but as a continuous adversarial companion:

```
Proposal --> AI Pass 1 --> Delphi Community Review --> AI Pass 2 --> Designer Draft --> AI Pass 3 --> Final Decision
```

**Pass 1** stress-tests the raw proposal through five adversarial roles (Performance Engineer, Language Theorist, Tooling Maintainer, Ecosystem Pragmatist, Red Team). **Pass 2** synthesizes sealed community feedback with the AI analysis. **Pass 3** audits the Designer's draft decision for logical soundness, gap coverage, and consistency with precedent.

Community feedback is collected through **Delphi** -- a sealed deliberation platform where reviewers submit independent assessments without seeing each other's responses. This eliminates anchoring, authority bias, and bandwagon effects that distort open forum discussion.

The AI panel is advisory, never authoritative. The Language Designer can override any AI assessment but must explain why in writing.

Read the full governance documents:

- [DSF Charter](https://github.com/dreamlang-dev/dreamlang/blob/main/docs/governance/CHARTER.md)
- [DEP Process](https://github.com/dreamlang-dev/dreamlang/blob/main/docs/governance/DEP-PROCESS.md)
- [AI Deliberation Protocol](https://github.com/dreamlang-dev/dreamlang/blob/main/docs/governance/AI-DELIBERATION.md)
- [Decision Framework](https://github.com/dreamlang-dev/dreamlang/blob/main/docs/governance/DECISION-FRAMEWORK.md)
- [Delphi Sealed Deliberation](https://github.com/dreamlang-dev/dreamlang/blob/main/docs/governance/DELPHI.md)

## Repositories

| Repository | Description |
|------------|-------------|
| [dreamlang](https://github.com/dreamlang-dev/dreamlang) | Monorepo -- language spec, book, website, governance docs, build tooling |
| dream | Compiler (Zig) -- coming soon |
| dreampay | Open-source payment platform for digital creators |
| delphi | Sealed community deliberation platform |

## The Book

*Dream: Engineering the Last Programming Language* is being written alongside the language. The book covers the formal foundations, design rationale, and implementation of every major feature -- from QTT and interaction nets to algebraic effects and content-addressable code. Early chapters are available at [dreamlang.dev/book](https://dreamlang.dev/book).

## Project Status

Dream is in an active design and prototype phase. A Zig-based compiler prototype exists with a working parser and lexer. The language specification, book, and implementation plan are still evolving.

This is a good time to get involved if you want to shape the language before it solidifies.

## Get Involved

- **Submit a DEP.** Anyone can propose changes to the language through the [DEP process](https://github.com/dreamlang-dev/dreamlang/blob/main/docs/governance/DEP-PROCESS.md).
- **Participate in Delphi reviews.** When a DEP enters community review, provide sealed feedback through the [Delphi platform](https://delphi.dreamlang.dev).
- **Contribute code.** The compiler, tooling, and standard library all accept contributions.
- **File issues.** Bug reports, spec ambiguities, and documentation gaps are valuable contributions.
- **Read the book.** Understanding the design rationale makes every other kind of contribution better.

## Links

- Website: [dreamlang.dev](https://dreamlang.dev)
- Delphi: [delphi.dreamlang.dev](https://delphi.dreamlang.dev)

## License

All DSF-stewarded code and specifications are released under the **Apache 2.0 + MIT dual license** unless otherwise noted.

---

*dream.*
