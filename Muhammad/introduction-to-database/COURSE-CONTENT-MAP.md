# Course Content Map — Introduction to Database (Oracle PL/SQL)

This map is the **ground truth** for the audit. Every "Expect" line in every scenario must be
supported by the content recorded here. If a fact is not in this map, an auditor must treat a
confident Fazah claim of it (attributed to these slides) as unsupported.

> **Source of truth:** the eight lecture PDFs were opened and their text extracted before this map
> was written. Content below is drawn only from those slides. This is an **Oracle PL/SQL programming
> course** (the "database" course teaches PL/SQL, Oracle's procedural extension to SQL). The slides
> are written in **Arabic prose with English code and keywords**; this audit's prompts and docs are
> in English, but the *code, keywords, and examples* below are exactly as they appear in the slides.
> Do **not** grade Fazah against general SQL/PL-SQL knowledge that is absent from these slides.

## The lecture files (what a teacher selects in Fazah)

| File | Topic | Slides | Notes |
|---|---|---:|---|
| `Lec1.pdf` | Intro to PL/SQL: blocks, variables, data types, scope | 22 | core |
| `Lec2.pdf` | Conditional statements: IF / CASE | 22 | core |
| `Lec3.pdf` | Iterative statements: loops | 17 | core |
| `Lec4.pdf` | `SELECT ... INTO`, `%TYPE`, `%ROWTYPE`, aggregates | 8 | core |
| `Lec5.pdf` | **Explicit** cursors | 13 | core |
| `Lec5_1.pdf` | **Implicit** cursors & SQL cursor attributes | 2 | supplement to Lec5 |
| `Lec6.pdf` | Procedures & Functions | 14 | some example slides are images |
| `Lec7.pdf` | Exceptions | 11 | ⚠ mostly image slides — little extractable text |

### IMPORTANT AMBIGUITIES TO PRESERVE (used only in the ambiguity scenarios)

1. **Duplicate files.** `Lec5_1.pdf` and `Lec5_11.pdf` are **byte-identical duplicates** (same file,
   both = implicit cursors). If both appear in a course, "Lecture 5.1" is ambiguous between two
   identical files.
2. **"The cursor lecture" / "Lecture 5" is ambiguous** between `Lec5.pdf` (**explicit** cursors) and
   `Lec5_1.pdf` (**implicit** cursors). Good behavior is to clarify or state which it will use.

Use these only in S017 (and where a scenario deliberately references "the cursor lecture" / "Lec 5").

---

## Lec1 — Introduction to PL/SQL

**Main topics:** what PL/SQL is · characteristics · the PL/SQL block · printing · comments ·
variables · data types · assignment/comparison/DEFAULT · arithmetic · NOT NULL & CONSTANT ·
nested blocks & variable scope.

**Key definitions / facts**
- **PL/SQL** = *Procedural Language extension of SQL*; a procedural language, an extension of SQL,
  developed by **Oracle** in the early 1990s to enhance SQL's capabilities.
- **Characteristics:** use SQL inside a PL/SQL unit; error handling; supports object-oriented
  programming; supports web applications.
- **The PL/SQL block** has three parts:
  - **Declarative** (optional) — for variables, cursors, and subprograms.
  - **Executable** (mandatory) — between `BEGIN` and `END`; the runnable PL/SQL statements.
  - **Exception** (optional) — where errors are handled.
- **Print:** `dbms_output.put_line('welcome to pl sql course');` inside `begin ... end;`.
- **Comments:** single line = `--` at the start of the line; multi-line = `/*` … `*/`.
- **Variables:** must start with a letter; max **30** characters; may contain digits, `_`, or `$`.
- **General variable syntax:** `name datatype := value;` (e.g. `msg varchar2(30) := 'welcome...';`).
- **Assignment vs comparison:** `:=` assigns a value; `=` compares; `DEFAULT` can assign a value
  instead of `:=` ( `:=` ≡ `DEFAULT` ).
- **Data types:** `NUMBER(precision,scale)` (number) · `VARCHAR2(max)` / `CHAR(max)` (text) ·
  `Boolean` (logical) · `DATE` (date/time) · `LOB` (images/audio/video).
- **NOT NULL** variable must be given an initial value. **CONSTANT** must be given an initial value
  and cannot be changed later (`n constant number(2) := 5;`).
- **Arithmetic:** `+ - * /`; `||` concatenates text and variables.
- **Nested blocks & scope:** a variable defined in the **outer** block is usable in the **inner**
  block; a variable defined in the **inner** block is NOT visible in the outer block (error). When
  inner and outer blocks declare the same variable name, each block uses its own variable.

**Examples in the deck:** circle-area exercise (`area = π r²`, π = 3.14); student-record exercise
(3 variables: id, name, age → print → change name to "محمد"/age 19 → reprint); salary scope example
(outer 3000 / inner 1500).

**Good for:** definitions, block structure, data-type tables, variable rules, scope questions,
"trace the output" of a small block. **Thin on:** anything beyond basic variables/scope.

---

## Lec2 — Conditional statements (IF / CASE)

**Main topics:** `IF` · `IF..ELSE` · `IF..ELSIF` · nested `IF` · `CASE` · searched `CASE`.

**Key facts**
- **IF**: `if <condition> then <statements>; end if;`
- **IF..ELSE**: adds an `else` branch.
- **IF..ELSIF**: multiple `elsif` branches then `else`. Deck example: grade bands with
  `if mark between 90 and 100 then 'A' elsif ... 'B'/'C'/'D'/'F' else 'Please enter correct mark'`.
- **Nested IF**: an `if` inside an `if` (e.g. validate `mark between 0 and 100` first, then grade).
- **CASE** (selector form): `CASE grade WHEN 'A' THEN ... WHEN 'B' THEN ... ELSE ... END CASE;`
  Deck: grade → 'Excellent' / 'Very good' / 'Well done' / 'You passed' / 'Better try again' /
  'No such grade'.
- **Searched CASE**: `CASE WHEN grade = 'A' THEN ... WHEN grade = 'B' THEN ... ELSE ... END CASE;`
- Input via substitution variable, e.g. `mark number := :enter_your_mark`.

**Good for:** IF vs CASE comparison, grade-classifier examples, "which construct fits" questions,
MCQs, trace-the-output. **Thin on:** loops/cursors (other lectures).

---

## Lec3 — Iterative statements (loops)

**Main topics:** simple `LOOP` · `WHILE` loop · `FOR` loop · nested loops.

**Key facts**
- **Simple LOOP:** `LOOP ... EXIT WHEN <cond>; ... END LOOP;` (or `IF <cond> THEN EXIT; END IF;`).
- **WHILE loop:** `WHILE <condition> LOOP ... END LOOP;` (checks the condition first).
- **FOR loop:** `FOR i IN 1..5 LOOP ... END LOOP;`; **reverse:** `FOR i IN REVERSE 1..5 LOOP ...`.
- **Nested loops:** a loop inside a loop (deck prints `i||j` across `for i in 1..3` / `for j in 2..3`).
- **`mod(x, y)`** used to test even/odd in a loop example.

**Good for:** three-loop comparison (simple vs while vs for), reverse/counter behavior, nested-loop
output tracing, MCQs, "write a loop that…" exercises. **Thin on:** anything outside loops.

---

## Lec4 — `SELECT ... INTO` and %TYPE / %ROWTYPE

**Main topics:** retrieving a **single row** into variables · `%TYPE` · `%ROWTYPE` · aggregate
functions. Uses the Oracle **HR sample schema** (`employees`, `jobs`).

**Key facts**
- **`SELECT col1, col2 INTO var1, var2 FROM table WHERE ...;`** reads one row into variables.
- **`%TYPE`**: declare a variable with the same type as a column, e.g.
  `i employees.employee_id%TYPE;` (avoids hard-coding the type).
- **`%ROWTYPE`**: declare a record matching a whole row, e.g. `job_rec jobs%ROWTYPE;` then read via
  `job_rec.min_salary`, `job_rec.max_salary`.
- **Aggregates:** `SELECT MAX(salary), MIN(salary) INTO mx, mn FROM employees;`.
- Deck data: `employees` (employee_id, last_name, salary…), `jobs` (job_id, job_title, min_salary,
  max_salary), examples like `IT_PROG`, salary `>= 10000` check.

**Good for:** `%TYPE` vs `%ROWTYPE` comparison, single-row query examples, aggregate examples,
MCQs, "write a SELECT INTO that…" exercises. **Note:** `SELECT INTO` returning zero or many rows is
the natural link to exceptions (Lec7: `NO_DATA_FOUND`, `TOO_MANY_ROWS`).

---

## Lec5 — Explicit cursors

**Main topics:** implicit vs explicit cursor (overview) · explicit-cursor lifecycle · cursor
attributes · fetching in different loops.

**Key facts**
- A **cursor** is a pointer to the result set of a query. **Implicit** cursors are created
  automatically for DML/`SELECT INTO`; **explicit** cursors are declared by the programmer for
  multi-row `SELECT`.
- **Explicit cursor lifecycle — four steps:** `DECLARE` the cursor → `OPEN` → `FETCH ... INTO` →
  `CLOSE`.
  - `DECLARE cursor emp_cur IS SELECT employee_id, last_name, salary FROM employees;`
- **Cursor attributes:** `%NOTFOUND` (no more rows) · `%FOUND` (a row was fetched) · `%ROWCOUNT`
  (number of rows fetched so far) · `%ROWTYPE` (record shaped like the cursor's row).
- **Fetching styles:** simple `LOOP` with `EXIT WHEN emp_cur%NOTFOUND`; `WHILE emp_cur%FOUND LOOP`;
  **cursor FOR loop** `FOR emp_rec IN emp_cur LOOP ...` (opens/fetches/closes automatically); FOR
  loop over an inline `SELECT`.
- Deck HR data: King (id 100, salary 24000), Kochhar (101, 18000), Fay (202, 18000); "Employees
  Number is 20" via `emp_cur%ROWCOUNT`.

**Good for:** four-step lifecycle, attribute meanings, loop-style comparison for fetching, MCQs,
"complete the cursor" exercises. **Explicit vs implicit** is a natural comparison with Lec5_1.

---

## Lec5_1 — Implicit cursors & SQL cursor attributes  (≡ `Lec5_11.pdf`, a duplicate)

**Main topics:** implicit cursor · SQL cursor attributes · DML.

**Key facts**
- An **implicit cursor** (the **`SQL`** cursor) is opened automatically by Oracle for `INSERT`,
  `UPDATE`, `DELETE`, and `SELECT INTO`.
- **`SQL` cursor attributes:** `SQL%FOUND` (TRUE if the DML/`SELECT INTO` affected ≥1 row) ·
  `SQL%NOTFOUND` (TRUE if it affected 0 rows) · `SQL%ROWCOUNT` (number of rows affected) ·
  `SQL%ISOPEN` (always FALSE for the implicit cursor — Oracle closes it automatically).
- Deck example: `CREATE TABLE STUDENT (ID NUMBER(3) PRIMARY KEY, SNAME VARCHAR2(25), GRADE
  NUMBER(3));` → `INSERT ALL ...` → `UPDATE STUDENT SET GRADE = ... WHERE ...;` then
  `IF SQL%FOUND THEN dbms_output.put_line('THERE ARE '||SQL%ROWCOUNT||' STUDENTS WHOSE GRADES HAVE
  CHANGED'); ELSIF SQL%NOTFOUND THEN ...`.

**Good for:** `SQL%` attribute questions, implicit-vs-explicit comparison, DML + attribute examples.

---

## Lec6 — Procedures & Functions

**Key facts**
- **Procedure** = a subprogram that performs one or more tasks. Can be **stored** with `CREATE`
  (a *Stored Procedure*) or defined in the `DECLARE` section. Can be **called** by another program.
- **Three parameter modes:** **`IN`** (pass a value in, used inside only) · **`OUT`** (return a value
  to the caller) · **`IN OUT`** (both — a value passed in, then an updated value sent back).
- **Procedure syntax:**
  `CREATE [OR REPLACE] PROCEDURE name [(p1 IN|OUT|IN OUT DATATYPE, ...)] IS|AS <declarations>
  BEGIN <execution> EXCEPTION <exceptions> END;`
- **Notes:** a procedure has **no `DECLARE` keyword** — variables go after `IS|AS` and before
  `BEGIN`; do **not** write the data size in a procedure's declaration section.
- **Function** = the same as a procedure **except it must return a value**. Syntax adds
  `RETURN DATATYPE` after the parameter list, and a `Return Variable` in the body:
  `CREATE [OR REPLACE] FUNCTION name [(...)] RETURN DATATYPE IS|AS ... BEGIN ... RETURN var; END;`

**Good for:** procedure vs function comparison, parameter-mode (IN/OUT/IN OUT) questions, syntax
questions, "write a procedure/function that…" exercises. **Note:** the deck's worked examples
(مثال 1–4) are image slides, so exact example code is not extractable — do not expect verbatim
example reproduction.

---

## Lec7 — Exceptions  ⚠ (thin — mostly image slides)

**What is extractable (keep expectations at this level):**
- The **`EXCEPTION`** section of a block handles errors.
- **`NO_DATA_FOUND`** — raised automatically when a query returns **no rows** (deck: an invalid
  department number).
- **`TOO_MANY_ROWS`** — raised automatically when a query returns **more than one row** (deck: a
  department with more than one employee).
- **`OTHERS`** — used to catch **any** error (system exception) not otherwise handled, whether named
  or unnamed.

**Good for:** naming/handling the three exceptions above, "which exception fires when…" questions,
linking `SELECT INTO` (Lec4) to `NO_DATA_FOUND`/`TOO_MANY_ROWS`. **Do NOT expect** deep exception
taxonomy, user-defined exceptions, `RAISE`, `SQLCODE/SQLERRM`, or verbatim example code — those are
not in the extractable slide text. A confident Fazah claim of such, attributed to Lec7, is unsupported.

---

## Cross-lecture connections (for revision-guide / multi-file scenarios)

- **Blocks (Lec1)** underpin every later lecture (all code lives in `BEGIN…END`).
- **`SELECT INTO` (Lec4)** is the single-row read; **cursors (Lec5)** handle multi-row reads.
- **Implicit vs explicit cursors** links Lec5 and Lec5_1.
- **`SELECT INTO` (Lec4)** → **exceptions (Lec7)**: zero rows → `NO_DATA_FOUND`, many rows →
  `TOO_MANY_ROWS`.
- **Conditionals (Lec2)** + **loops (Lec3)** are the control-flow pair; both build on Lec1.
- **Procedures/Functions (Lec6)** package block logic and can contain everything above.
- **`%TYPE`/`%ROWTYPE` (Lec4)** reappear in cursor records (`emp_cur%ROWTYPE`, Lec5).

## Known source-content limitations (auditor awareness)

- **Lec6 example slides and Lec7 are image-based** — little/no extractable text. Fazah cannot quote
  code that is not present; a *fabricated* verbatim example attributed to these decks is a red flag.
- Slides are **Arabic prose + English code**. Facts above are the English/technical content; do not
  expect Fazah to reproduce Arabic wording unless a scenario asks in Arabic (none do — prompts are English).
- These are **lecture slides**, not a lab manual — there is no separate exercise/solution set here.
