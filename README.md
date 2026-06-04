# Diffusion_and_Flow_Matching
An artifact to my self study of Diffusion Models and Flow Matching for Generative Models

## Goal

I've already mapped the conceptual landscape of visual generative AI (autoencoders → VAEs → U-Nets → DDPMs → transformers → DiTs → video). This repo is about going from *"I followed the paper"* to *"I can re-derive it from a blank page and make it converge in code."*

The focus is depth at the load-bearing points, working toward my real interest: **controllable, human-in-the-loop generation** — keeping the artist's intent while the model does the laborious work.

**Keystone idea:** noise-prediction (ε), score (∇ log p), clean-data (x₀), and velocity (v) prediction are the same model under reparameterization. Owning that equivalence is owning DDPM.

## How I'm working

Two modes for every topic:
- **Derive** — work it out by hand in a derivations notebook. No "it can be shown."
- **Build** — implement the smallest version that proves it works.

The loop: intuition → derive → code → read the original paper. One concept at a time. Math lets you fool yourself; code doesn't.

## Roadmap

| Phase | Focus | Key build |
|-------|-------|-----------|
| 0 | Math prerequisites (Gaussians, KL, ELBO, ODE/SDE literacy) | — |
| 1 | DDPM foundations + the ε / score / x₀ / v equivalence | DDPM from scratch on MNIST/CIFAR-10 |
| 1.5 | Guidance & samplers (DDIM, classifier-free guidance) | DDIM + CFG on my model |
| 2 | Continuous time & flow matching (SDEs, prob-flow ODE, rectified flow) | Flow matching on a 2D toy (vector-field plot) |
| 3 | DiT + my niche (controllable / stylized conditioning) | Latent DiT; a controllable conditioning experiment |

## Planned repo layout

```
notebooks/      # derivations + experiments, phase by phase
src/            # reusable model / training / sampling code
notes/          # short write-ups (e.g. "Diffusion vs Flow Matching")
roadmap.md      # the full plan with gates
```

## Progress

- [ ] Phase 0 — prerequisites
- [ ] Phase 1 — DDPM from scratch
- [ ] Phase 1.5 — guidance & samplers
- [ ] Phase 2 — flow matching
- [ ] Phase 3 — DiT & controllable generation

*(Updated as I go.)*

## Key resources

- Calvin Luo — [Understanding Diffusion Models: A Unified Perspective](https://arxiv.org/abs/2208.11970)
- [Ho et al. — DDPM](https://arxiv.org/abs/2006.11239) · [Song et al. — Score-based SDEs](https://arxiv.org/abs/2011.13456) · [Yang Song's blog](https://yang-song.net/blog/2021/score/)
- [Lipman et al. — Flow Matching](https://arxiv.org/abs/2210.02747) · [Flow Matching Guide & Code](https://arxiv.org/abs/2412.06264)
- [Peebles & Xie — DiT](https://arxiv.org/abs/2212.09748)
