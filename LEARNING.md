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
