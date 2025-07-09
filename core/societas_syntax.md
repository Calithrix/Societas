# Societas Syntax Protocol

**Version:** 1.0
**Maintainer:** Matthew Coppola + ChatGPT (OpenAI)
**Status:** ✅ Canonical

---

## 📘 Syntax Overview

Societas Syntax is the formal language used to encode, compress, and manipulate symbolic thought using the U-Substitution framework. All conceptual work within the Societas system must adhere to this syntax structure to ensure stratal compatibility, recursive traversability, and synthesis fidelity.

Each valid Societas statement is built from symbolic primitives drawn from the **Semantic U-Substitution Table (V1.0)**.

---

## 🔤 Symbol Construction Rules

### 1. U\_x Declaration

Each symbolic construct must begin with a `U_x` identity and include a formal encoding structure:

```
U_x = κ[...] + Δc[...] + Φv[...] + Λμ[...] + Ξp[...] + Σf[...] + Ωτ[...] + πR(...) + Ψs(...)
```

* Not all symbols must be present.
* At minimum, every U\_x must include: κ, Δc, Φv.

### 2. ⊥map(...)

Contradictions must be visualized or tabulated using the `⊥map(...)` syntax:

```
⊥map(x ⊗ y):  
| x | y |  
|---|---|  
| Value-A | Value-B |
```

### 3. ⇌codex(...)

Every encoded idea must include a human-readable form using `⇌codex()`:

```
⇌codex(U_x): “Natural language summary or philosophical description.”
```

### 4. Ψs(...)

Synthesis must be explicitly declared:

```
Ψs(A ⊗ B) → U_x
```

Where A and B are contradicting strata, and U\_x is the synthesis product.

### 5. env: declarations

Simulations must specify environment:

* `env:sta` = Static analysis
* `env:dyn` = Dynamic simulation

Use `⧉sw(env)` to toggle:

```
⧉sw(env:sta → env:dyn)
```

### 6. ✳init\[x]

To initialize a symbolic object, use:

```
✳init[U_x]
```

This formally declares the beginning of a symbolic entity or simulation run.

---

## 🧪 Syntax Grammar Reference (ABNF-style)

```bnf
symbol        = "κ" / "Δc" / "Φv" / "Λμ" / "Ξp" / "Σf" / "Ωτ" / "πR" / "Ψs" / "θ" / "χz" / "τ0"
u_x           = "U_" ALPHA *(ALPHA / DIGIT / "_")
substitution  = symbol "[" TEXT "]"
synthesis     = "Ψs(" TEXT "⊗" TEXT ") →" u_x
contradiction = "Δc[" TEXT "⊗" TEXT "]"
init_call     = "✳init[" u_x "]"
codex_call    = "⇌codex(" u_x ")"
env_mode      = "env:sta" / "env:dyn"
swap_env      = "⧉sw(" env_mode " → " env_mode ")"
```

---

## 📏 Syntax Standards

* Use Markdown for formatting.
* Each U\_x must be versioned and timestamped.
* Use `[Symbol]` consistently. No alternate bracket formats allowed.
* Contradiction operators use `⊗`, not `x` or `*`.
* Human-readable summaries (`⇌codex`) are required for clarity and collaboration.

---

## ✅ Example

```markdown
✳init[U_gnt]

U_gnt = κ[identity-within-systems] + Δc[globalism ⊗ tribalism] + Φv[glocal self-determination] + Λμ[modular-sovereignty stack]

⇌codex(U_gnt): “A modular ideological system where nested tribal identities opt into global coordination layers via trust and interoperability, without sacrificing cultural autonomy.”
```

---

This syntax protocol may be extended in future versions. All symbols and operators must correspond to valid entries in the semantic table (see `semantic-u-table-v1.md`).

**Symbol Engine Integrity Level:** 1.0
**Confirmed by:** Societas Core System
