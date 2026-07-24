# Course Content Map — AI623: Deep Vision Language Models (LUMS, Spring 2026)

Instructor: Muhammad Tahir · MS-level elective · 1×180-min lecture/week · open-book final.
Fazah course name: **AI623 — Deep Vision Language Models** (13 files: 12 text-ready + 1
deliberately handwritten/scanned edge-case file).

Every scenario in this suite grounds against the facts below. When a scenario says "matching the
notes", the auditor checks against this map and, when needed, the original file in
[`course-files/`](./course-files/).

## Files and what they contain

| # | Fazah filename | Source | Key content (grounding anchors) |
|---|---|---|---|
| 0 | `AI623_course_outline.pdf` | Official LUMS outline | Course description (multimodal deep models, diffusion focus); prerequisites (MS AI standing or CS331/EE315); grading: attendance 5%, PAs 40%, final exam 20%, group project 35%; final exam open-book/open-notes, 3 h, no midterm; CLO1–CLO3 |
| 1 | `01_dvlm_introduction.pptx` | Intro deck | Definitions: **LLM** (language-only), **VLM** (LLM + vision encoder, understands language+images, generates text), **MLLM** (processes/understands/generates text, images, video, audio); what the course will NOT cover (CNNs, RNNs, LSTMs, transformer training); reference book: Holderrieth & Erives, *An Introduction to Flow Matching and Diffusion Models* (arXiv:2506.02070); grading repeated |
| 2 | `04_vae_denoising_autoencoders_notes.pdf` | VAE cheat sheet | DAE forward corruption x̃ = x + ε, ε∼N(0, σ²I); DAE reconstruction MSE loss; **Tweedie's formula** E[x\|x̃] = x̃ + σ²∇log P(x̃); **reparameterization trick** z = μ_φ(x) + σ_φ(x)⊙ε; ELBO = reconstruction − KL; closed-form KL for Gaussians |
| 3 | `05_ncsn_score_based_models_notes.pdf` | NCSN cheat sheet | Forward x̃ = x + σε; **true score of Gaussian** S_true(x̃\|x) = −ε/σ (= (x−x̃)/σ²); unweighted NCSN loss; λ(σ)=σ² weighting; **annealed Langevin dynamics** update x ← x + (α/2)s_θ(x,σ) + √α·z |
| 4 | `06_diffusion_ddpm_ddim_notes.pdf` | Diffusion cheat sheet | α_t = 1−β_t; ᾱ_t = ∏α_i; **SNR_t = ᾱ_t/(1−ᾱ_t)**; iterative forward step; **closed-form jump** x_t = √ᾱ_t·x_0 + √(1−ᾱ_t)·ε; x_0 isolation; true posterior mean/variance; DDPM sampling step; **DDIM step with η blending (η=0 deterministic, η=1 ≈ DDPM)** |
| 5 | `07_flow_matching_notes.pdf` | Flow-matching cheat sheet | **VE-SDE** (NCSN, f=0) vs **VP-SDE** (DDPM, f=−½β(t)x_t); reverse SDE; **Euler–Maruyama predictor** + Langevin corrector (predictor-corrector); probability-flow ODE; **linear interpolant** x_t = (1−t)x_0 + t·x_1 with target velocity v = x_1 − x_0; flow-matching loss |
| 6 | `08_diffusion_score_flow_worked_problems.md` | Worked problems | 10+ fully worked numeric problems on DDPM forward/posterior, DDIM steps, score↔noise conversion, Euler–Maruyama, flow-matching interpolants — with final boxed answers (used to check Fazah's arithmetic) |
| 7 | `09_ar_alignment_rlhf_notes.pdf` | AR + alignment cheat sheet | Autoregressive chain rule P_θ(x)=∏P_θ(x_t\|x_<t); softmax with temperature; token cross-entropy; perplexity; top-k / top-p (nucleus); beam search; **RLHF objective with KL penalty**; **Bradley–Terry reward model loss**; **DPO loss**; **GRPO group-normalized advantage** |
| 8 | `10_ar_alignment_worked_problems.md` | Worked problems | Numeric problems: temperature softmax (z=(2,1,0), T=0.5 → p≈(0.867, 0.117, 0.016)); top-k/top-p + beam-search step; perplexity; DPO gradient sign; GRPO advantages — with boxed answers |
| 9 | `11_ppo_dpo_grpo_alignment.pptx` | PA2 deck (6 slides) | Alignment = helpful/harmless/honest; pipeline: base model → preference data → reward model → policy optimization, KL constrains drift; **PPO**: needs policy + reference + reward + critic (most complex); **DPO**: pairwise preferences, no separate reward model; **GRPO**: no critic, group sampling, group-normalized rewards; all three keep a reference model for KL control |
| 10 | `12_vlm_vit_clip_reasoning.md` | VLM notes + problems | **ViT patch tokenization**: N = HW/P² (224×224, P=16 → 196 patches + [CLS] = 197 tokens); patch-embedding parameter count; **CLIP contrastive loss** (symmetric InfoNCE, temperature); cross/multimodal attention shapes; VLM token budgets; visual-reasoning grounding checks |
| 11 | `13_exam_master_cheatsheet.md` | Master cheat sheet | Cross-topic quick reference: numeric tables (ln, e^x, σ(x)), all core formulas from files 2–10, solution recipes, sanity checks, common pitfalls — the "whole-course" file for revision scenarios |
| 12 | `14_handwritten_class_notes_L2.pdf` | Handwritten class notes | **Deliberate edge case**: scanned handwriting, zero extractable text (Fazah shows it as needs-review). Used by scenarios that test how Fazah behaves when a selected source has no usable text |

## Topic → file quick map

| Topic | Primary file(s) |
|---|---|
| Course logistics, grading, prerequisites | outline (0), intro (1) |
| LLM / VLM / MLLM definitions | intro (1) |
| DAE, Tweedie, VAE, reparameterization, ELBO | 04 (2) |
| Score matching, NCSN, Langevin | 05 (3) |
| DDPM / DDIM, schedules, SNR, posterior | 06 (4), 08 (6) |
| SDEs, predictor-corrector, flow matching | 07 (5), 08 (6) |
| AR generation, sampling, perplexity | 09 (7), 10 (8) |
| RLHF / PPO / DPO / GRPO | 09 (7), 10 (8), 11 (9) |
| ViT, CLIP, multimodal attention, VLM reasoning | 12 (10) |
| Whole-course revision | 13 (11) |
| Unreadable/handwritten source behavior | 14 (12) |

## High-value grounding facts (for quick pass/fail checks)

1. VLM = an LLM **with a vision encoder**; understands language + images, **generates text** (intro).
2. Tweedie's formula: E[x|x̃] = x̃ + σ²∇log P(x̃) (VAE notes).
3. True Gaussian score: −ε/σ, equivalently (x−x̃)/σ² (NCSN notes).
4. Closed-form DDPM jump: x_t = √ᾱ_t·x_0 + √(1−ᾱ_t)·ε; SNR_t = ᾱ_t/(1−ᾱ_t) (diffusion notes).
5. DDIM η: η=0 deterministic, η blends toward DDPM (diffusion notes).
6. VE-SDE has zero drift (f=0); VP-SDE drift −½β(t)x_t (flow-matching notes).
7. Flow-matching linear interpolant target velocity: v = x_1 − x_0 (flow-matching notes).
8. Temperature softmax worked answer: z=(2,1,0), T=0.5 → p≈(0.867, 0.117, 0.016) (worked problems).
9. PPO needs 4 models (policy, reference, reward, critic); DPO drops the reward model; GRPO drops the critic; **all three keep the reference model for KL** (PA2 deck).
10. ViT 224×224, P=16 → 196 patches, 197 tokens with [CLS] (VLM notes).
11. Grading: 5% attendance / 40% PAs / 20% final / 35% project; open-book final, no midterm (outline).
12. File 14 (handwritten) has **no extractable text** — an honest system must say so, not hallucinate content.
