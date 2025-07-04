# 🗓️ Compiler Roadmap Calendar (2025–2026)

---

## ✅ High-Level Calendar

| Phase | Timeframe | Goals |
|-------|-----------|-------|
| **Phase 1** | July 1 – July 21 | Learn Scala FP + mini-projects |
| **Phase 2** | July 22 – Aug 25 | Build a mini FP language with REPL & typechecker |
| **Phase 3** | Aug 26 – Sept 29 | Learn logic/type theory & implement small typed systems |
| **Phase 4** | Sept 30 – Nov 10 | Learn CBPV + Category Theory + build CBPV IR |
| **Phase 5** | Nov 11 – Jan 26 | Write compiler backend + VM + full CBPV pipeline |
| **Polish & Extras** | Jan 27 – Feb 23 | GC, optimization, blog posts, polish, bonus ideas |

---

## 🗓️ Month-by-Month Breakdown

### **July 2025**
- 📚 **Week 1 (July 1–7)**: 
  - Read 2–3 chapters of *FP in Scala*
  - Implement `List`, `Tree`, and `Map` in Scala
- 🔧 **Week 2 (July 8–14)**:
  - Job starts (40h/week)
  - Build arithmetic expression evaluator
- 🧠 **Weeks 3–4 (July 15–21)**:
  - State monad simulation project
  - Design grammar for mini language

---

### **August 2025**
- 🛠️ **July 22 – August 25**:
  - Implement lexer → parser → AST
  - Write interpreter (call-by-name)
  - Build REPL
  - Add type checker for simple types

---

### **September 2025**
- 📖 Study *How to Prove It* – 2–3 chapters/week
- 🔬 Projects:
  - Command-line proof assistant
  - Lambda calculus evaluator with beta-reduction
  - Type checker using De Bruijn indices

---

### **October – Early November 2025**
- 📘 Read *Introduction to Category Theory*
- 📄 Study Levy’s CBPV materials
- 🧱 Projects:
  - Define CBPV IR
  - Lambda → CBPV transformation
  - Add functor/monad abstractions
  - Free monad DSL + interpreter

---

### **Mid-November – January 2026**
- 🏗️ Build VM:
  - Design bytecode instruction set
  - Implement bytecode interpreter
  - Handle closures and environments
- 🚀 Compile CBPV IR → bytecode
- (Optional) Add garbage collection

---

### **February 2026**
- 🎯 Polish compiler, cleanup, refactor
- 🛠️ Add pattern matching or lazy evaluation
- ✍️ Document the language or write blog/devlog

---

## 🔁 Weekly Template (Post July 9th)

| Day | Task Type | Example |
|-----|-----------|---------|
| Weekdays (1–2 hr) | Reading / Coding | FP Scala / Parser tweaks |
| Saturday (2–4 hr) | Coding Sprint | REPL, CBPV IR, VM features |
| Sunday (1–2 hr) | Review / Plan / Blog | Weekly check-in, document progress |

---

## 📌 Progress Checkpoints

- ✅ **July 21**: Strong FP Scala foundation + 2–3 mini projects
- ✅ **August 25**: REPL + type-checked mini FP language
- ✅ **Sept 29**: Lambda calculus + simple proof assistant
- ✅ **Nov 10**: CBPV IR + theory understanding complete
- ✅ **Jan 26**: Full compiler + VM working end-to-end
- ✅ **Feb 23**: Polished project, optional extras, documented
