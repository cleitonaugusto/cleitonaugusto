# Cleiton Augusto Corrêa Bezerra

**Software Engineer — Rust · compiler correctness · Python · Java**

Systems analyst in the Brazilian federal court system (15+ years), now working
on correctness in quantum compilers and Rust tooling. I care about the
difference between software that *looks* right and software that *is* right:
real tests, validation against references, and honesty about a program's limits.

---

### 🐛 A correctness bug in Qiskit's transpiler, fixed in 2.5.1

[**Qiskit issue #16594**](https://github.com/Qiskit/qiskit/issues/16594) —
`CommutativeCancellation` cancelled a three gate sequence that equals an `X`
down to an empty circuit at optimization level 2 and above, silently changing
measured results. No error, no warning.

I found it with a differential fuzzer I wrote, reduced it to three gates,
characterized the fault surface across thousands of angles and pointed at the
failing line. Confirmed by a core maintainer, milestone 2.5.1, fixed in PR
#16599. I got the root cause wrong on the first try and said so in the thread.

---

### 🔧 Projects

- **[CleitonForge](https://github.com/cleitonaugusto/CleitonForge)** — the
  differential fuzzer that found the bug above. Weighted generator aimed at the
  numeric thresholds a compiler actually branches on, a shrinker that reduces a
  failure to a minimal witness, and an oracle layer that cross-checks every
  verdict against the exact operator before calling anything a bug.
- **[nqf-lint](https://github.com/cleitonaugusto/nqf-lint)** — pre-flight linter
  for quantum-chemistry setups. **Rust core + Python bindings (PyO3)**,
  published on both registries.
  `cargo install nqf-lint` · `pip install nqf-lint`
  [![crates.io](https://img.shields.io/crates/v/nqf-lint?logo=rust&label=crates.io)](https://crates.io/crates/nqf-lint)
  [![PyPI](https://img.shields.io/pypi/v/nqf-lint?logo=pypi&label=PyPI)](https://pypi.org/project/nqf-lint/)
- **[CleitonQ](https://github.com/cleitonaugusto/CleitonQ)** — post-quantum
  authentication for embedded systems: `no_std` Rust implementing FIPS
  203/204/205, protocol formally verified in ProVerif and Tamarin, written up as
  two individual IETF Internet-Drafts.
- **[async-graphql-dataloader](https://github.com/cleitonaugusto/async-graphql-dataloader)**
  — DataLoader for `async-graphql` in Rust, for the N+1 problem. 1,100+
  downloads.
- **[validation-gate](https://github.com/cleitonaugusto/validation-gate)** — a
  gate that refuses the shortcuts behind irreproducible ML-for-science claims:
  hash-sealed pre-registration, a mandatory trivial baseline, a blind holdout
  counted in a ledger. I ran it on my own research first and it failed 0 of 5.
  `pip install validation-gate`

---

### 📚 Books

**[Quantum Rust: Complete Bundle](https://leanpub.com/b/quantumrustcompletebundlequantum-rust-complete)**
(Leanpub) — *Quantum Circuit Benchmarking in Rust* and *Quantum Computing for
Rust Developers*.

---

### 🧰 Stack

**Languages:** Rust · Python · Java · SQL / PL-SQL
**Rust:** async · unsafe · PyO3 · `no_std` · published crates
**Testing:** differential and property-based testing · fuzzing · shrinking
**Backend:** REST APIs · FastAPI · Docker · CI/CD · Linux
**Java stack:** Spring · Hibernate · Maven · JBoss / WildFly
**Databases:** Oracle · Adabas

---

### 🎸🎹 Off the keyboard

Guitarist & pianist.

---

### 📫 Contact

- Email: augusto.cleiton@gmail.com
- GitHub: [@cleitonaugusto](https://github.com/cleitonaugusto)
- LinkedIn: [Cleiton Augusto Corrêa Bezerra](https://www.linkedin.com/in/cleiton-augusto-b619435b)

<sub>Open to fully remote work — Rust, compiler and correctness tooling, backend,
and scientific/technical software.</sub>
