# My AI Engineering Path
<!-- Managed by the ai-engineering-from-scratch learning skills.
     Repo: https://github.com/rohitg00/ai-engineering-from-scratch -->

## Mission
"I think all": shipping an AI product, a possible career change, understanding the AI tools I use every day, and research.
Build goal: not sure yet. I'll decide along the way.

## Placement
- Date: 2026-10-17
- Score: self-selected
- Entry point: Phase 0: Setup & Tooling
- Pace: ~2 h/week

## Path
| Phase | Name | Status | Est. hours |
|-------|------|--------|------------|
| 0 | Setup & Tooling | Do | 16 |
| 1 | Math Foundations | Do | 23 |
| 2 | ML Fundamentals | Do | 26 |
| 3 | Deep Learning Core | Do | 15 |
| 4 | Computer Vision | Do | 27 |
| 5 | NLP — Foundations to Advanced | Do | 30 |
| 6 | Speech & Audio | Do | 18 |
| 7 | Transformers Deep Dive | Do | 14 |
| 8 | Generative AI | Do | 14 |
| 9 | Reinforcement Learning | Do | 13 |
| 10 | LLMs from Scratch | Do | 26 |
| 11 | LLM Engineering | Do | 19 |
| 12 | Multimodal AI | Do | 65 |
| 13 | Tools & Protocols | Do | 43 |
| 14 | Agent Engineering | Do | 55 |
| 15 | Autonomous Systems | Do | 20 |
| 16 | Multi-Agent & Swarms | Do | 28 |
| 17 | Infrastructure & Production | Do | 34 |
| 18 | Ethics, Safety & Alignment | Do | 31 |
| 19 | Capstone Projects | Do | 620 |
| | **Total** | | **1137** |

## Progress log
| Date | Lesson | Quiz | Note |
|------|--------|------|------|
| 2026-10-17 | 00/01-dev-environment | 3/3 | Intel Mac (i7-8850H, macOS 15.5): Homebrew has no bottles and CLT is too old, so uv came from the astral installer. torch capped at 2.2.2 with numpy<2. MPS True via Radeon Pro 560X (learner predicted False). git is still 2.18.0 (old). |
| 2026-10-18 | 00/02-git-and-collaboration | 3/3 | Fixed SSH from scratch: ed25519 key, Keychain agent, origin switched to SSH, pushed `my-progress` to fork with -u. Explained key auth as signature check. Learned `!` can't answer interactive prompts (passphrase). |
| 2026-10-18 | 00/03-gpu-setup-and-cloud | 2/3 | No CUDA; MPS benchmark on Radeon Pro 560X (4 GB): GPU loses at 10-500, ~3x at 2000-4000. Predicted overhead for small matmuls; unsure on sync until no-sync timing (~0.2 ms) shown. Needed a walkthrough for VRAM/2 rule, then got 8 GB -> 4B. Missed nvidia-smi (picked torch.cuda.list_devices). |

## Review queue
- 00/03-gpu-setup-and-cloud: `nvidia-smi` (NVIDIA GPU status CLI; driver, CUDA version, VRAM, processes). Practise on Colab T4.

## Resume notes
_Last updated 2026-10-18. Read this first when resuming._

**Next lesson:** 00/04-apis-and-keys (`phases/00-setup-and-tooling/04-apis-and-keys/`, code: `first_api_call.py`, `first_api_call.ts`). Warm-up from 00/03 quiz (pre questions not yet asked: why GPUs are faster, what VRAM is). Revisit the review item `nvidia-smi` when Colab comes up.
**Heads-up for 00/04:** needs an LLM API key. Keep it in an env var or a gitignored `.env`, never in a commit (the fork `shaffi/ai-engineering-from-scratch` is public on GitHub).

**Machine**
- Intel MacBook Pro, i7-8850H (6 cores), macOS 15.5. GPUs: Radeon Pro 560X (4 GB VRAM) + Intel UHD 630.
- No CUDA. PyTorch MPS works (built + available). Device pick: cuda -> mps -> cpu.
- Python venv at repo root `.venv` (made with uv from the astral installer; Homebrew has no bottles here). torch 2.2.2, numpy<2. Run lesson code as `.venv/bin/python ...` from the repo root.
- MPS matmul benchmark (00/03): GPU slower at 10x10 and 500x500, ~3x faster at 2000-4000. Heavy phases (4+) should use Colab T4.

**Git**
- Apple git 2.39.5. Branch `my-progress` tracks `origin/my-progress` (`-u` set), so plain `git push` works.
- `origin` = git@github.com:shaffi/ai-engineering-from-scratch.git (SSH), `upstream` = rohitg00 repo (HTTPS).
- SSH key `~/.ssh/id_ed25519` is on GitHub and stored in the macOS Keychain; `ssh -T git@github.com` says "Hi shaffi".
- Routine after each lesson: `git commit -am "chore: log 00/NN"` then `git push`.

**How the learner learns best**
- Short replies ("C", "not sure", "I dont know"). When unsure, break it into small numbered steps with concrete numbers, then give a quick check question. That worked for the VRAM rule.
- Gets intuition right (predicted GPU overhead on small matrices). Running a real experiment on their own machine helped the most (no-sync timing).
- `!` commands in Claude Code cannot answer interactive prompts (passwords, passphrases). Use a separate Terminal.app window for those.
