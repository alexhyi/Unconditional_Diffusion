# Diffusion_and_Flow_Matching
An artifact to my self study of Diffusion Models and Flow Matching for Generative Models

## Goal

I've already mapped the conceptual landscape of visual generative AI (autoencoders → VAEs → U-Nets → DDPMs → transformers → DiTs → video). This repo is about going from *"I followed the paper"* to *"I can re-derive it from a blank page and make it converge in code"*, focusing at load-bearing points decribed below.  

My real interest: **controllable, human-in-the-loop generation** — keeping the artist's intent while the model does the laborious work.

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
*(Update as I go)*

## Key resources

- Calvin Luo — [Understanding Diffusion Models: A Unified Perspective](https://arxiv.org/abs/2208.11970)
- [Ho et al. — DDPM](https://arxiv.org/abs/2006.11239) · [Song et al. — Score-based SDEs](https://arxiv.org/abs/2011.13456) · [Yang Song's blog](https://yang-song.net/blog/2021/score/)
- [Lipman et al. — Flow Matching](https://arxiv.org/abs/2210.02747) · [Flow Matching Guide & Code](https://arxiv.org/abs/2412.06264)
- [Peebles & Xie — DiT](https://arxiv.org/abs/2212.09748)
