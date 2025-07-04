# 🛤️ From Scala to Call-by-Push-Value VM

This roadmap is for building a compiler in Scala for a functional programming language, ultimately targeting a custom virtual machine with **call-by-push-value** semantics. It includes learning steps, resources, and mini-projects.

---

## ✅ Phase 1: [[Functional programming in Scala]]

> 📚 Goal: Master Scala and functional programming idioms.

### 📘 Core Resource:
- *Functional Programming in Scala* ("Red Book")

### 📌 Key Concepts:
- Pure functions, recursion, folds
- Higher-order functions
- Algebraic Data Types (ADTs)
- Functional error handling (Option, Either)
- Monads (State, IO, etc.)

### 🧩 Mini-Projects:
- [ ] Implement a purely functional `List`, `Tree`, `Map`
- [ ] Arithmetic expression evaluator
- [ ] State monad game (Tic-Tac-Toe, random walk, etc.)

---

## ✅ Phase 2: A Mini Functional Language (Call-by-Name)

> 📚 Goal: Build a simple interpreted FP language with syntax and types.

### 📘 Core Resource:
- *Crafting Interpreters* (optional support)

### 📌 Language Features:
- Lambdas, application, variables
- Let bindings
- Call-by-name evaluation

### 🧩 Mini-Projects:
- [ ] Lexer → Parser → AST
- [ ] Interpreter (call-by-name)
- [ ] REPL
- [ ] Type checker (simple types like `Int`, `Bool`, `T → U`)

---

## 🔍 Phase 3: Type Theory and Proofs

> 📚 Goal: Learn formal reasoning and basic type theory.

### 📘 Core Resource:
- *How to Prove It* – Daniel Velleman
- Simon Thompson - Type Theory

### 📌 Topics:
- Propositional and predicate logic
- Proofs, induction, quantifiers
- Set theory basics
- Foundations for type theory

### 🧩 Mini-Projects:
- [ ] Command-line proof assistant (natural deduction)
- [ ] Lambda calculus evaluator with beta-reduction
- [ ] Type checker with De Bruijn indices

---

## 🌀 Phase 4: Category Theory & CBPV

> 📚 Goal: Understand semantic structures of FP and CBPV.

### 📘 Core Resources:
- *Introduction to Category Theory* – Harold Simmons
- Paul Levy’s *Call-by-Push-Value* (paper or book)

### 📌 Topics:
- Functors, natural transformations
- Monads, adjunctions
- Value vs computation types
- Thunks, sequencing, forcing

### 🧩 Mini-Projects:
- [ ] Write a CBPV-inspired IR
- [ ] Transformer: λ-calculus → CBPV IR
- [ ] Implement functor/monad abstractions for your AST
- [ ] Free monad DSL + interpreter

---

## ⚙️ Phase 5: Compiler & VM Implementation

> 📚 Goal: Compile your language down to a working VM.

### 📌 Compiler Stages:
- Frontend: Parsing, AST, type checking
- Middle-end: CBPV IR lowering and optimizations
- Backend: Code generation to bytecode

### 📌 VM Features:
- Stack or register machine
- Support closures, environments, basic GC

### 🧩 Mini-Projects:
- [ ] Define your VM’s bytecode format and interpreter
- [ ] Closure and environment handling
- [ ] Compile CBPV IR to bytecode
- [ ] Implement a basic garbage collector (mark-and-sweep or ref counting)

---

## 📌 Bonus Ideas (Optional / Parallel)

- [ ] Optimizations: constant folding, inlining, DCE
- [ ] Pattern matching in the frontend
- [ ] Lazy evaluation via thunks
- [ ] Algebraic effects or effect handlers
- [ ] Step-by-step visual evaluator (e.g. browser UI or ASCII diagrams)

---

## 📅 Suggested Project Timeline

| Phase | Est. Time |
|-------|-----------|
| Phase 1 | 2–4 weeks |
| Phase 2 | 3–5 weeks |
| Phase 3 | 3–6 weeks |
| Phase 4 | 4–8 weeks |
| Phase 5 | 6–12 weeks |

---

## 📝 Notes

- Don’t rush through the theory: implement, experiment, and revisit.
- It’s okay to read parts of multiple books when needed (esp. for context).
- You don’t need to finish all category theory before CBPV.
- Consider blogging or documenting what you build — teaching helps retention.
