# Course Content Map — Web Application Development (PHP)

Ground truth for the audit. Every "Expect" line in every scenario must be supported here. If a fact
is not in this map, treat a confident Fazah claim of it (attributed to these slides) as unsupported.

> **Source of truth:** all 15 PowerPoint decks were opened and their text extracted before this map
> was written. Content below is drawn only from those slides. This course teaches **Web Application
> Development, primarily through PHP**, plus two concept modules (computer networks, web architecture).
> Do **not** grade Fazah against general PHP/web knowledge that is absent from these slides.

## The files (what a teacher selects in Fazah)

| File | Topic |
|---|---|
| `Module 1 - Computer Network for Web Developer.pptx` | Networks, OSI/TCP-IP, IP, DNS, HTTP, ping/traceroute |
| `Module 3- Understanding Web Application Architecture.pptx` | Client-server, static vs dynamic, MVC |
| `php_syntax_presentation.pptx` | PHP tags, statements, case sensitivity |
| `php_comments_presentation.pptx` | `//`, `#`, `/* */` |
| `php_variables_presentation.pptx` | `$` variables, rules, output |
| `php_datatypes_presentation.pptx` | the 8 PHP data types |
| `php_casting_presentation.pptx` | `(int)(string)(bool)(array)…` |
| `php_numbers_presentation.pptx` | integers, floats, Infinity/NaN, `is_numeric` |
| `php_strings_presentation.pptx` | quotes, `strlen`, `strpos`, concatenation |
| `php_operators_presentation (2).pptx` | arithmetic/assignment/comparison/logical operators |
| `php_if_else_presentation.pptx` | `if` / `elseif` / `else` |
| `php_switch_presentation.pptx` | `switch` / `case` / `break` / fall-through |
| `php_loops_presentation.pptx` | `while`, `do…while`, `for`, `foreach` |
| `php_arrays_presentation.pptx` | indexed, associative, multidimensional arrays |
| `php_forms_presentation.pptx` | HTML forms, `$_GET`/`$_POST`, GET vs POST, security |

### IMPORTANT QUIRKS TO PRESERVE (used only in the ambiguity scenarios)

1. **Module 2 is missing.** Only **Module 1** and **Module 3** exist — there is no Module 2. A teacher
   who says "use Module 2" is referencing a file that isn't in the course; good behavior is to flag it,
   not fabricate content. (Used in S017.)
2. **`php_operators_presentation (2).pptx` carries a "(2)" version tag** — "the operators slides"
   can read as ambiguous about which version. There is only this one in the course.

---

## Module 1 — Computer Network for Web Developer (29 slides)

- **Computer networking** = two or more computers communicating (analogy: people talking need ≥2
  parties, a common language, deliverable voice → computers need a communication model + network medium).
- **Communication models** are **layered/stacked** (OSI, TCP/IP). Advantages: **simplicity,
  modularity, development, interoperability**. Transmission encapsulates data down the layers.
- **Protocol** = a set of rules governing how an operation is performed (each application has one).
- **IP address (v4)** = **32 binary bits**, shown as **four octets in dotted-decimal** (e.g.
  `192.168.1.19`); two parts: **network** and **host**.
- **DNS** = maps a **domain name → IP address** (a table); solves memorizing IPs; hierarchical;
  multiple sites can share one IP (**shared hosting**). Example: `uncc.edu` → `152.15.47.208`.
- **HTTP** = HyperText Transfer Protocol, the main web browsing protocol; **stateless** (each request
  handled separately); works in **request/response** pairs (client → request → server → response).
  - **Request verbs:** **GET** (normal resource fetching), **POST** (submitting forms, payload
    attached), **UPDATE** (updating a resource), **DELETE** (deleting).
  - **Response codes** (3 digits `XXX`; first digit = category): **1xx** informational, **2xx**
    success, **3xx** redirection, **4xx** client-side errors (e.g. wrong page), **5xx** server-side errors.
- **TCP or UDP** (named; diagram slide). **Checking connectivity:** `ping`. **Tracing packets:**
  `traceroute` / `tracert`. **DNS lookup:** `nslookup`.

**Good for:** networking concepts, IP/DNS/HTTP questions, verb & status-code questions, command
questions (ping/tracert/nslookup). **Thin on:** the OSI/TCP-IP layer diagrams (image slides) — don't
expect verbatim layer lists beyond "layered/stacked, OSI and TCP/IP".

## Module 3 — Understanding Web Application Architecture (10 slides)

- **Client-server model** (request/response) vs **peer-to-peer**.
- **Web server** serves clients; **frontend vs backend**.
- **Static web pages:** web server + file system → browser rendering engine (no processing).
- **Dynamic web pages:** add an **interpreter** and a **database** (server processes before responding).
- **MVC design pattern:**
  - **Model** = data-related logic (**INSERT, UPDATE, LIST, DELETE**).
  - **View** = what the user sees — frontend code (**HTML, CSS**); bi-directional link to the controller.
  - **Controller** = intermediary that **glues view and model**; holds the **business logic**.

**Good for:** client-server, static vs dynamic, MVC role questions. **Thin on:** the architecture
diagrams (image slides).

## php_syntax — PHP Syntax
- PHP = **server-side scripting** language; syntax similar to C; files `.php`; must be accessed over
  **HTTP**; **processed by the server before the browser**.
- **Tags:** canonical **`<?php … ?>`** (recommended); short-open **`<? … ?>`** (needs
  `short_open_tag=on` in `php.ini`). Can escape in/out of HTML.
- **Statements end with `;`**; multiple per line OK; expressions = values & operators.
- **PHP is case-sensitive** (`$age` ≠ `$Age`). Roles: HTML=structure, CSS=styling, JS=client,
  PHP=server. Flow: browser requests `.php` → server processes → HTML/CSS/JS sent → browser renders.

## php_comments — PHP Comments
- A comment is **not executed**; for developers to read.
- **Single-line:** `//` or `#`. **Multi-line:** `/* … */`.
- Uses: explain code, disable code, documentation blocks. Best practice: **explain WHY not WHAT**,
  keep concise, keep updated; don't state the obvious or leave sensitive data.

## php_variables — PHP Variables
- Containers for data; **start with `$`**; created on first assignment (no declaration).
- **Rules:** start with `$`, then a **letter or `_`**, then `A-z 0-9 _`. **Cannot** start with a
  number, contain spaces, or use special chars (`$2name`, `$my name`, `$my-var` are invalid).
- **Output:** inside double quotes (`echo "I love $txt!"`) or **concatenation with `.`**. Multiple
  assignment `$x = $y = $z = "…"`. `var_dump()` shows type and value.

## php_datatypes — PHP Data Types (8 types)
- **String, Integer, Float, Boolean, Array, Object, NULL, Resource.**
- **String:** chars in single or double quotes; **double quotes parse variables**, single are faster.
- **Integer:** whole numbers, range **±2,147,483,647** (32-bit); hex `0x1A`.
- **Float:** decimals / exponential (`2.4e3`). **Boolean:** TRUE/FALSE (case-insensitive). **NULL:**
  no value (`$x = null;` or an unset variable auto-NULL).

## php_casting — PHP Type Casting
- Casts: **`(string) (int) (float) (bool) (array) (object) (unset)`**; verify with `var_dump()`.
- **To string:** numbers→numeric strings, `true`→`"1"`, `false`/`NULL`→`""`.
- **To int:** float truncates (`5.34`→`5`); string starting with a number extracts it (`"25 km"`→`25`);
  string starting with text →`0`; `true`→`1`; `NULL`→`0`.
- **To bool — FALSE:** `0`, `0.0`, `""`, `"0"`, `NULL`, `false`, `[]`. **TRUE:** any non-zero
  (including `-1`, `0.1`), non-empty.

## php_numbers — PHP Numbers
- **Integer** (32-bit range; decimal/hex `0xFF`/octal `0377`/binary `0b…`), **Float** (decimal or
  exponential `7.64E+5`; `PHP_FLOAT_MAX/MIN/DIG`), **numeric strings**.
- **Infinity** (`is_infinite()`/`is_finite()`), **NaN** (`is_nan()`, e.g. `acos(8)`), `is_numeric()`.

## php_strings — PHP Strings
- **Single quotes:** literal, no variable parsing, faster. **Double quotes:** parse variables, escape
  sequences. `echo 'Hello $name'` → `Hello $name`; `echo "Hello $name"` → `Hello John`.
- **`strlen()`** = length in bytes (includes spaces; `"Hello world!"`→12). **`str_word_count()`** =
  word count (→2). **`strpos()`** = position of first occurrence (0-indexed; `"world"` in
  `"Hello world!"`→6; returns **FALSE** if not found). **Concatenation** with the **`.`** operator.

## php_operators — PHP Operators
- **Arithmetic:** `+ - * / %` and `**` (power; `10 ** 3` = 1000). **Assignment:** `= += -= *= /= %=`.
- **Comparison:** `==` (equal value), `===` (equal value **and type**), `!=`, `<>`, `!==`, `> < >= <=`.
- Categories also named: logical, increment/decrement, string (`.`), array, conditional (ternary).

## php_if_else — PHP If…Else
- **`if (condition) { }`**, **`if…else`**, **`if…elseif…else`** (multiple conditions). Examples:
  hour-based greeting (`if ($time < 12) "Good morning" elseif ($time < 18) "Good afternoon" else …`).

## php_switch — PHP Switch
- **`switch (expr) { case label: … break; … default: … }`**. Expression evaluated once, compared to
  each case; `break` exits; `default` runs if no match. **Omitting `break` causes fall-through**
  (next cases run).

## php_loops — PHP Loops
- **`while (cond) { }`** (check then run); **`do { } while (cond);`** (**always runs at least once**);
  **`for (init; cond; increment) { }`** (count up/down/skip by 2); **`foreach ($arr as $value)`** or
  **`foreach ($arr as $key => $value)`** (iterate arrays). Examples: `while $i<=5` → `1 2 3 4 5`;
  `do` with `$i=6, i<=5` → `6` (runs once).

## php_arrays — PHP Arrays
- An array holds many values under one name. **Types:** **indexed** (numeric index, first = **0**),
  **associative** (named keys `"brand" => "Ford"`), **multidimensional** (arrays of arrays).
- Create with `array(...)` or **short `[...]`**; access by index/key; update `$cars[1] = "Ford"`;
  iterate with `foreach`.

## php_forms — PHP Forms
- **HTML form:** `<form action="process.php" method="POST">` + `<input name="…">` + submit.
  Attributes: **action** (where to send), **method** (GET or POST), **name** (field id).
- **Superglobals:** **`$_GET`** (URL params), **`$_POST`** (form data).
- **GET vs POST:** GET = bookmarkable, cached, in history, **visible in URL, ~2000-char limit, not for
  sensitive data, no file uploads**. POST = **not in URL, no size limit, file uploads, secure for
  passwords**, not bookmarkable/cached. **Recommended for forms: POST.**
- **Security:** never trust user input; **always validate and sanitize** form data.

---

## Cross-topic connections (for revision-guide / multi-file scenarios)
- **Module 1 (HTTP request/response, GET/POST verbs)** connects to **php_forms (`$_GET`/`$_POST`)**.
- **Module 3 (dynamic pages need an interpreter + DB; MVC)** frames why PHP (server-side) exists.
- **php_syntax** underpins every PHP topic (tags, `;`, case sensitivity).
- **php_variables → php_datatypes → php_casting → php_numbers/strings** form the data-handling chain.
- **php_operators → php_if_else / php_switch** (conditions) → **php_loops** (repetition) → **php_arrays**
  (`foreach`) → **php_forms** (real input).

## Known source-content limitations (auditor awareness)
- Several slides are **diagram/image-only** (OSI & TCP/IP models, DNS hierarchy, architecture
  diagrams). Fazah cannot quote text that isn't present; a *fabricated* verbatim quote is a red flag.
- **Module 2 does not exist** in this course (only Module 1 and Module 3).
- These are lecture slides, not a lab manual — no separate exercise/solution set is included here.
