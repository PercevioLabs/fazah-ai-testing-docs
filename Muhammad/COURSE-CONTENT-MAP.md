# Course Content Map — Introduction to Software Engineering (Theory)

This map is the **ground truth** for the audit. Every "Expect" line in every scenario
must be supported by the content recorded here. If a fact is not in this map, an auditor
must treat a confident Fazah claim of it (attributed to these slides) as unsupported.

> **Source of truth:** the five uploaded `.pptx` decks were opened and their slide text
> extracted before this map was written. Content below is drawn only from those slides
> (Sommerville-style *Software Engineering* lecture decks). Do **not** grade Fazah against
> general Software Engineering knowledge that is absent from these slides.

## Filename vs. internal chapter number (IMPORTANT AMBIGUITY)

The five files are named `Ch1..Ch5`, but three decks display a **different** internal
chapter number on their title slide. Preserve this mismatch — it is used deliberately in
the chapter-ambiguity scenarios (S017) and only there.

| File name | Displayed (internal) chapter title | Slides | Match? |
|---|---|---:|:--:|
| `Ch1 Introduction.pptx` | **Chapter 1** – Introduction | 29 | ✅ matches |
| `Ch2 SW Processes.pptx` | **Chapter 2** – Software Processes | 58 | ✅ matches |
| `Ch3 Req Eng.pptx` | **Chapter 4** – Requirements Engineering | 88 | ❌ file "Ch3", internal "Chapter 4" |
| `Ch4 Testing.pptx` | **Chapter 8** – Software Testing | 64 | ❌ file "Ch4", internal "Chapter 8" |
| `Ch5 Agile SW Dev.pptx` | **Chapter 3** – Agile Software Development | 66 | ❌ file "Ch5", internal "Chapter 3" |

**Consequence for auditing:** a bare phrase like "Chapter 4" is ambiguous — it could mean
the 4th file (`Ch4 Testing`) or the deck whose internal title is "Chapter 4" (`Ch3 Req Eng`).
"Chapter 3" is similarly ambiguous (`Ch3 Req Eng` file vs. `Ch5 Agile` internal). Good
behavior is to clarify or to clearly state the interpretation before proceeding.

---

## File 1 — `Ch1 Introduction.pptx`

- **File name:** `Ch1 Introduction.pptx`
- **Displayed chapter title:** Chapter 1 – Introduction (29 slides)
- **Filename vs. internal mismatch:** none.

**Main sections**
- Professional software development (what software engineering is)
- Software products (generic vs. customized)
- Essential attributes of good software
- Software engineering activities / process activities
- Software engineering diversity & application types
- Internet / web software engineering
- Software engineering ethics

**Important definitions**
- **Software** = computer programs and associated documentation.
- **Software engineering** = an engineering discipline concerned with **all aspects of
  software production**, from early system specification through to maintaining the system
  after it has gone into use.
- **Generic products** = stand-alone systems marketed and sold to any customer (e.g. graphics
  programs, project-management tools, CAD, dentist appointment systems).
- **Customized (bespoke) products** = software commissioned by a specific customer (e.g.
  embedded control systems, air-traffic control, traffic-monitoring systems).

**Important comparisons**
- **Generic vs. customized products** — including who owns the specification (developer owns
  it for generic; customer owns it for customized).
- **Software engineering vs. computer science** — CS = theory/fundamentals; SE = practicalities
  of developing and delivering useful software.
- **Software engineering vs. system engineering** — system engineering covers hardware, software
  and process engineering; SE is part of that broader process.

**Important lists (exam-friendly)**
- **Four essential attributes of good software:** Maintainability, Dependability and security,
  Efficiency, Acceptability.
- **Four fundamental SE / software process activities:** Software specification, software
  development, software validation, software evolution.
- **Application types:** stand-alone, interactive transaction-based, embedded control,
  batch processing, entertainment, modeling & simulation, data collection, systems of systems.
- **Costs (per slide 8):** ~60% development, ~40% testing; for custom software, evolution
  costs often exceed development costs.

**Important examples**
- Generic vs. customized product examples (CAD, dentist appointments vs. air-traffic control).
- Web/cloud: web services, cloud computing (pay per use), AJAX/HTML5 rich interfaces.

**Software engineering ethics (slides 26–29)**
- Wider responsibilities than technical skill; honesty; ethics is more than obeying the law.
- **Issues of professional responsibility:** Confidentiality, Competence, Intellectual property
  rights, Computer misuse.

**Useful assessment topics:** definition of software/SE; four attributes of good software;
generic vs. customized; four process activities; application types; ethics responsibilities.

**Useful lesson / slide topics:** "What is software engineering", attributes of good software,
ethics for first-year students, application-type survey.

**Topics NOT sufficiently covered here (do not expect depth):** detailed process models
(that is Ch2), requirements techniques (Ch3), testing levels (Ch4), agile practices (Ch5).

---

## File 2 — `Ch2 SW Processes.pptx`

- **File name:** `Ch2 SW Processes.pptx`
- **Displayed chapter title:** Chapter 2 – Software Processes (58 slides)
- **Filename vs. internal mismatch:** none.

**Main sections**
- Software process models
- Process activities
- Coping with change
- Process improvement

**Important definitions**
- **Software process** = a structured set of activities required to develop a software system.
- **Software process model** = an abstract representation of a process from some perspective.
- **Plan-driven process** = all activities planned in advance; progress measured against the plan.
- **Agile process** = planning is incremental; easier to change to reflect changing requirements.
- **Prototype** = an initial version of a system used to demonstrate concepts and try out design
  options.

**Process models covered**
- **Waterfall model** — plan-driven, separate/distinct phases. Phases: Requirements analysis and
  definition → System and software design → Implementation and unit testing → Integration and
  system testing → Operation and maintenance. Main drawback: hard to accommodate change once
  underway; suited to stable, well-understood requirements and large systems-engineering projects.
- **Incremental development** — specification, development, validation interleaved; may be
  plan-driven or agile. Benefits: reduced cost of change, easier customer feedback, faster delivery.
  Problems: reduced process visibility, system structure tends to degrade without refactoring.
- **Integration and configuration (reuse-oriented)** — system assembled from existing configurable
  components / COTS. Key stages: requirements specification, software discovery/evaluation,
  requirements refinement, application system configuration, component adaptation and integration.

**Important comparisons**
- **Plan-driven vs. agile processes** (most real processes mix both; "no right or wrong processes").
- **Waterfall vs. incremental development** (change accommodation, visibility, structure).
- **Change anticipation vs. change tolerance**; **incremental development vs. incremental delivery**.
- **Process maturity approach vs. agile approach** to process improvement.

**Important lists**
- **Four basic process activities:** specification, development (design & implementation),
  validation, evolution.
- **Coping with change:** change anticipation (e.g. prototyping) and change tolerance (e.g.
  incremental development); techniques = system prototyping and incremental delivery.
- **Benefits of prototyping:** improved usability, closer match to real needs, improved design
  quality, improved maintainability, reduced development effort.
- **Process improvement cycle:** measurement → analysis → change.
- **SEI Capability Maturity Model levels:** Initial, Repeatable, Defined, Managed, Optimising.

**Important examples**
- COTS reuse; throw-away prototypes; V-model (testing phases in a plan-driven process).

**Useful assessment topics:** waterfall phases & drawbacks; incremental development benefits/problems;
reuse-oriented stages; prototyping; incremental delivery advantages/problems; CMM levels.

**Useful lesson / slide topics:** waterfall vs. incremental lesson; "coping with change";
process-improvement / CMM overview.

**Topics NOT sufficiently covered:** Agile *methods/practices* in detail (XP, Scrum are Ch5);
requirements techniques (Ch3); testing techniques (Ch4). Ch2 mentions requirements engineering
and testing stages only at a process-overview level.

---

## File 3 — `Ch3 Req Eng.pptx`  ⚠️ internal "Chapter 4"

- **File name:** `Ch3 Req Eng.pptx`
- **Displayed chapter title:** **Chapter 4 – Requirements Engineering** (88 slides)
- **Filename vs. internal mismatch:** ❗ file says "Ch3", title slide says "Chapter 4".

**Main sections**
- Functional and non-functional requirements
- Requirements engineering processes
- Requirements elicitation
- Requirements specification
- Requirements validation
- Requirements change

**Important definitions**
- **Requirements engineering** = the process of establishing the services a customer requires
  from a system and the constraints under which it operates and is developed.
- **User requirements** = statements (natural language + diagrams) of services and operational
  constraints, written for customers.
- **System requirements** = a structured document of detailed function/service/constraint
  descriptions; may be part of a contract.
- **Functional requirements** = statements of services the system should provide, how it reacts
  to inputs, how it behaves in situations (may state what it should *not* do).
- **Non-functional requirements** = constraints on services/functions (timing, standards, process),
  often applying to the system as a whole; may be more critical than functional ones.
- **Domain requirements** = constraints on the system from the domain of operation.

**Important comparisons**
- **Functional vs. non-functional requirements** (core comparison for this deck).
- **User requirements vs. system requirements.**
- **Goal vs. verifiable non-functional requirement** (e.g. "easy to use" vs. "after 4 hours of
  training, ≤2 errors/hour").
- **Non-functional classifications:** product / organisational / external requirements.

**Important examples (all Mentcare-based)**
- **Mentcare stakeholders:** patients, doctors, nurses, medical receptionists, IT staff, medical
  ethics manager, health-care managers, medical records staff.
- **Mentcare functional requirement examples:** search appointment lists for all clinics; daily
  per-clinic patient list; 8-digit employee number identification.
- **Mentcare non-functional examples:** availability Mon–Fri 08:30–17:30, downtime ≤5s/day
  (product); health-authority identity-card authentication (organizational); HStan-03-2006-priv
  privacy provision (external).
- **iLearn / KidsTakePics** photo-sharing scenario (Jack the teacher) — a worked user story/scenario.
- **Insulin pump** requirement examples and tabular specification.

**Important lists**
- **RE generic activities:** elicitation, analysis, validation, management.
- **Elicitation stages:** requirements discovery, classification & organization, prioritization &
  negotiation, specification.
- **Elicitation techniques:** interviewing (closed/open), ethnography, stories & scenarios, use cases.
- **Requirements validation checks:** validity, consistency, completeness, realism, verifiability.
- **Review checks:** verifiability, comprehensibility, traceability, adaptability.
- **Ways of writing a system requirements spec:** natural language, structured natural language,
  design description languages, graphical notations, mathematical specifications.
- **Requirements document structure:** preface, introduction, glossary, user requirements
  definition, system architecture, system requirements specification, system models, system
  evolution, appendices, index.
- **Requirements management:** identification, change management process, traceability policies,
  tool support; change management = problem analysis → change analysis & costing → change
  implementation.

**Important fact:** fixing a requirements error after delivery may cost up to **100×** the cost
of fixing an implementation error.

**Useful assessment topics:** functional vs. non-functional; NFR classifications; elicitation
techniques; validation checks; requirements document structure; scenarios/use cases.

**Useful lesson / slide topics:** "functional vs. non-functional" mini-lesson; elicitation
techniques; Mentcare-based worked examples; scenarios & user stories.

**Topics NOT sufficiently covered:** process models beyond RE context (Ch2); testing techniques
(Ch4); Scrum/XP mechanics (Ch5, though "user stories" and "agile & requirements" appear briefly).

---

## File 4 — `Ch4 Testing.pptx`  ⚠️ internal "Chapter 8"

- **File name:** `Ch4 Testing.pptx`
- **Displayed chapter title:** **Chapter 8 – Software Testing** (64 slides)
- **Filename vs. internal mismatch:** ❗ file says "Ch4", title slide says "Chapter 8".

**Main sections**
- Development testing
- Test-driven development
- Release testing
- User testing

**Important definitions**
- **Testing** = intended to show that a program does what it is intended to do and to discover
  defects before use. Can reveal the **presence** of errors, **not their absence**.
- **Verification** = "Are we building the product **right**?" (conform to specification).
- **Validation** = "Are we building the **right** product?" (do what the user really requires).
- **Inspections (static verification)** = examining the static system representation to discover
  problems; do **not** require execution; can be used before implementation.
- **Testing (dynamic verification)** = exercising and observing product behavior with test data.
- **Development testing** = all testing carried out by the team developing the system.
- **Release testing** = testing a release intended for use outside the development team; usually a
  **black-box** process; goal = convince supplier the system is good enough for use.
- **User testing** = users/customers test the system in their own environment.
- **Test-driven development (TDD)** = interleave testing and code development; tests written
  **before** code; passing the tests drives development.
- **Regression testing** = testing to check that changes have not broken previously working code.

**Important comparisons**
- **Verification vs. validation** (core comparison for this deck).
- **Inspections vs. testing** (static vs. dynamic; complementary, not opposing).
- **Validation testing vs. defect testing** (successful test = works vs. successful test = exposes a defect).
- **Development testing vs. release testing** (who does it; defect vs. validation focus).
- **Alpha vs. beta vs. acceptance testing.**

**Important lists**
- **Three stages of testing:** development testing, release testing, user testing.
- **Three levels of development testing:** unit testing (functionality of objects/methods),
  component testing (component interfaces), system testing (component interactions / emergent behavior).
- **Two kinds of unit test case:** normal-operation tests and abnormal-input tests.
- **Testing strategies:** partition (equivalence) testing, guideline-based testing.
- **Interface types:** parameter, shared memory, procedural, message passing.
- **Interface errors:** interface misuse, interface misunderstanding, timing errors.
- **TDD process:** identify small increment → write automated test → run (fails) → implement → re-run → next.
- **Benefits of TDD:** code coverage, regression testing, simplified debugging, system documentation.
- **Types of user testing:** alpha testing, beta testing, acceptance testing.
- **Acceptance testing stages:** define criteria → plan → derive tests → run → negotiate results → reject/accept.

**Important examples (all Mentcare/weather-station-based)**
- Weather-station object testing & state transitions.
- Mentcare allergy/prescription requirements-based tests.
- George-the-nurse Mentcare usage scenario (scenario testing).

**Useful assessment topics:** verification vs. validation; testing stages/levels; unit/component/
system testing; interface errors; partition testing; TDD; alpha/beta/acceptance; release testing.

**Useful lesson / slide topics:** "verification vs. validation"; testing levels; TDD walkthrough;
interface-error examples; acceptance-testing process.

**Topics NOT sufficiently covered:** requirements techniques (Ch3); agile management/Scrum (Ch5,
though TDD and agile acceptance testing appear here); detailed process models (Ch2).

---

## File 5 — `Ch5 Agile SW Dev.pptx`  ⚠️ internal "Chapter 3"

- **File name:** `Ch5 Agile SW Dev.pptx`
- **Displayed chapter title:** **Chapter 3 – Agile Software Development** (66 slides)
- **Filename vs. internal mismatch:** ❗ file says "Ch5", title slide says "Chapter 3".

**Main sections**
- Agile methods
- Agile development techniques
- Agile project management (Scrum)
- Scaling agile methods

**Important definitions**
- **Agile development** = specification, design, implementation and testing interleaved; system
  developed as a series of versions/increments; minimal documentation, focus on working code.
- **Plan-driven development** = separate development stages with outputs planned in advance (not
  necessarily waterfall — plan-driven incremental is possible).
- **Extreme Programming (XP)** = a very influential agile method (late 1990s); "extreme" iterative
  development; new versions several times per day, increments to customers every 2 weeks.
- **Refactoring** = constant code improvement to make future changes easier.
- **Scrum** = an agile method focused on **managing** iterative development rather than specific
  practices; provides a project-management framework.

**Important comparisons**
- **Plan-driven vs. agile development** (core comparison for this deck).
- **XP vs. Scrum** (XP = technical practices; Scrum = management framework).
- **Scaling up vs. scaling out** agile methods.
- **Agile principles vs. organizational practice** (frictions).

**Important lists**
- **Agile Manifesto — four values:** Individuals and interactions over processes and tools;
  Working software over comprehensive documentation; Customer collaboration over contract
  negotiation; Responding to change over following a plan.
- **Principles of agile methods:** customer involvement, incremental delivery, people not process,
  embrace change, maintain simplicity.
- **XP practices:** incremental planning, small releases, simple design, test-first development,
  refactoring, pair programming, collective ownership, continuous integration, sustainable pace,
  on-site customer.
- **Key/influential XP practices:** user stories for specification, refactoring, test-first
  development, pair programming.
- **Scrum phases:** initial (outline planning) phase, sprint cycles, project closure phase.
- **Scrum terminology:** development team (≤7), potentially shippable product increment, product
  backlog, product owner, Scrum (daily meeting), ScrumMaster, sprint (2–4 weeks), velocity.
- **Scrum benefits:** manageable chunks, unstable requirements don't hold up progress, team
  visibility, on-time increments, trust between customers and developers.
- **Scaling / multi-team Scrum:** role replication, product architects, release alignment,
  Scrum of Scrums.

**Important examples**
- "Prescribing medication" user story & task cards.
- Test-case description for dose checking.
- IBM agility-at-scale model.

**Useful assessment topics:** Agile Manifesto values; agile principles; XP practices; Scrum roles
& terminology; sprint cycle; plan-driven vs. agile; scaling agile.

**Useful lesson / slide topics:** "Explain Scrum"; Agile Manifesto; XP practices; plan-driven vs.
agile decision factors.

**Topics NOT sufficiently covered:** detailed requirements techniques (Ch3); detailed testing
levels (Ch4, though TDD/test-first appears here); waterfall internals (Ch2).

---

## Cross-chapter connections (for revision-guide and multi-file scenarios)

These links appear across decks and are safe to use in cross-chapter tasks:

- **Incremental development** appears in Ch1 (web), Ch2 (process model) and Ch5 (agile core).
- **Prototyping** links Ch2 (coping with change) and Ch3 (requirements validation technique).
- **Test-driven / test-first development** links Ch4 (TDD section) and Ch5 (XP practice).
- **User stories / scenarios** link Ch3 (elicitation) and Ch5 (XP specification).
- **Verification & validation** links Ch2 (validation activity), Ch4 (V&V core).
- **Plan-driven vs. agile** links Ch2 (process types) and Ch5 (agile vs. plan-driven).
- **Requirements change / evolution** links Ch2 (evolution), Ch3 (requirements change/management).
- **Acceptance testing in agile** links Ch4 (user testing) and Ch5 (embedded customer).

## Known source-content limitations (auditor awareness)

- Several slides are **figure-only** (title + a diagram, no body text) — e.g. Ch2 V-model and
  process-improvement-cycle slides, Ch3 spiral/use-case diagrams, Ch4 equivalence-partition and
  sequence-chart slides. Fazah cannot quote text that is not present; do not penalize it for not
  reproducing a diagram, but a *fabricated* verbatim quote from such a slide is a red flag.
- Decks contain **minor typos** in the original slides (e.g. "donw", "acustomer", "importaant",
  "dsitributed"). These are in the source, not Fazah errors.
- These decks are the **Theory Section** only. There is no lab/practical content here; requests
  for lab exercises are outside the supplied material.
