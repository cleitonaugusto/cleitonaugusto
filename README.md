# Cleiton Augusto Corrêa Bezerra

**Software Engineer — Rust · protocol security · compiler correctness · Python**

Systems analyst in the Brazilian federal court system (15+ years), now working
on protocol security, quantum-compiler correctness, and Rust tooling. I care
about the difference between software that *looks* right and software that *is*
right: real tests, validation against references, and honesty about a program's
limits.

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

### 🛰️ A vulnerability class where a conformant relay strips authentication

Authentication attached to a message gets silently removed when a conformant
intermediary parses that message and rebuilds it from the fields it understood.
No attacker at the moment of removal, no error, no warning. I characterized the
class, then measured it against real software: MAVLink relays, DDS bridges,
CAN / ISO-TP gateways, SOME/IP gateways, gRPC-JSON transcoders (Envoy,
grpc-gateway, ConnectRPC), and DICOM de-identification. Several runs argued
against my own thesis, and I kept the ones that did.

Two IETF Internet-Drafts, a CWE submission, threat-catalogue entries written to
paste into ISO 21434 and FDA 524B files, and a preprint
([doi:10.5281/zenodo.21840073](https://doi.org/10.5281/zenodo.21840073)). Latest
write-up: [DICOM de-identification silently strips image provenance](https://dev.to/cleiton_augusto_/a-conformant-dicom-de-identifier-silently-strips-your-images-signature-7h2).

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

**[Quantum Computing for Rust Developers](https://www.amazon.com/dp/B0HHNQZBD3)**
— 2nd edition, September 2026. Paperback, 248 pages, ISBN 9798171107352.
Builds the differential fuzzer above from nothing, in Rust.

The second edition documents nine errors found in the first. The one worth
naming: I had written a demonstration to expose a sign bug, and the angles I
picked were the ones where that bug is invisible. The demo passed and proved
nothing.

**[Quantum Rust: Complete Bundle](https://leanpub.com/b/quantumrustcompletebundlequantum-rust-complete)**
(Leanpub) — the earlier edition, bundled with *Quantum Circuit Benchmarking in
Rust*.

---

### 🔀 Merged into other people's repositories in 2026

- **[Qiskit #16594](https://github.com/Qiskit/qiskit/issues/16594)** — the
  transpiler bug above, fixed in 2.5.1
- **[grpc-gateway #7282](https://github.com/grpc-ecosystem/grpc-gateway/pull/7282)**
  — security considerations documentation, merged by a maintainer
- **[Lift #4](https://github.com/rustnew/Lift/pull/4)** — a sign error in a gate
  decomposition, with a regression test. The first test I wrote passed on the
  broken code, because the sequence I picked was a palindrome
- **[NVIDIA CUDA-Q #5192](https://github.com/NVIDIA/cuda-quantum/issues/5192)** —
  a controlled swap losing its control in OpenQASM 2 translation. I corrected
  the toffoli wiring in the proposed fix; the implementation NVIDIA shipped uses
  the corrected version
- **[Deltakit](https://github.com/Deltakit/deltakit-compile/pull/14)**
  (Riverlane) — issue assigned to me, pull request open on their compiler.
  While verifying it I found that comparing detector error models has zero power
  against a class of fault, reported as
  [issue #347](https://github.com/Deltakit/deltakit/issues/347) with a
  four-instruction reproduction and a
  [DOI](https://doi.org/10.5281/zenodo.22239105)

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
- Writing: [dev.to/@cleiton_augusto_](https://dev.to/cleiton_augusto_)
- LinkedIn: [Cleiton Augusto Corrêa Bezerra](https://www.linkedin.com/in/cleiton-augusto-b619435b)

<sub>Open to fully remote work — Rust, compiler and correctness tooling, backend,
and scientific/technical software.</sub>
