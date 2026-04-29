# Changelog

This document records the version history of the brief, including the role of adversarial review at each stage.

## v4.0 — April 2026

Self-administered red-team pass on v3 followed by a tightening pass. Substantive technical changes:

- Latency analysis softened to acknowledge that real MPC solvers exploit problem structure (Jacobian reuse, sequential quadratic programming) rather than performing naive forward simulations at every iteration. Naive arithmetic from v3 would not have survived scrutiny by anyone who has implemented hypersonic MPC.
- Substrate thermal coefficient discussion qualified to acknowledge that low thermo-optic coefficient is necessary but not sufficient for cavity-based thermal stability; resonator Q and operating-point margins must be jointly optimized.
- Section 1 environmental hostility claim corrected to refer to vehicle skin and forward-mounted optical sensors rather than avionics interior, which is thermally managed.
- Certification framing softened from "maps cleanly" to "offers a plausible path." No precedent exists yet for the specific PS2F architecture in primary flight authority.
- Orthogonal test signal failure detection method qualified: out-of-band probing is necessary but not sufficient; periodic in-band probing is also required, accepting the small disturbance cost.
- Russian literature gap acknowledged honestly without undercutting the central argument.
- Removed unverified "Beca 2025" reference.
- Reconciled Aadhi et al. publication date inconsistency to Nature Communications 17, 1225 (2026).
- Yan et al. given institutional context (UCL, Southeast University, Loughborough University) on first detailed mention.

Tightening:
- Abstract split into two paragraphs, redundancy removed.
- Verbal signal-flow walkthrough removed (duplicated existing Section 2 content).
- Various opener phrases trimmed to direct statement.
- Section 7 Betsy introduction tightened.
- Acknowledgments leaned further into the AI-adversarial-review methodology, explaining its use as a partial substitute for conventional peer review and explicitly inviting human domain expert critique.

Final length: approximately 6,800 words.

## v3.0 — April 2026

Incorporated structural review from DeepSeek (received after v2 reference verification pass). Substantive additions:

- Quantified latency analysis with concrete MPC horizon and iteration numbers (later softened in v4 after self-administered red-team review).
- Substrate thermal coefficient comparison with specific values (silicon: 1.8 × 10⁻⁴ K⁻¹, diamond approximately an order of magnitude smaller).
- Concrete failure detection method: pseudo-random orthogonal test signal injection above the control bandwidth, cross-correlation against baseline impulse response.
- Training pipeline specifics: CFD bulk training with domain randomization, Bayesian transfer learning to wind-tunnel data, sub-scale flight refinement.
- Readout bottleneck paragraph in Section 6: hybrid optical-electronic ADC latency can be 10× to 100× the optical core's evaluation time.
- Comparison to non-photonic alternatives in Section 6: memristor crossbars, FPGA-accelerated ESNs, analog neuromorphic chips.
- New Section 10 with six concrete open research questions structured around the milestone framework.

Length grew from approximately 5,500 words (v2) to approximately 6,800 words (v3). Self-administered red-team identified that the latency analysis would not survive scrutiny and that several other framing choices needed tightening, leading to v4.

Acknowledgment: DeepSeek also suggested several changes that were deliberately not incorporated, including a counter-argument-and-rebuttal section (sales-document pattern), a risk register with probability columns (false precision on un-estimable outcomes), and an explanatory footnote for the Betsy name (placeholder is fine as placeholder).

## v2.0 — April 2026

Comprehensive rewrite incorporating convergent adversarial review from Perplexity, GPT, and Gemini. Key structural changes:

- Repositioning of the central argument from "photonic RC as alternative computational primitive" to "photonic RC as fast surrogate dynamical model within Predictive Safety-Stability Filter (PS2F) architecture."
- Introduction of the PS2F framework (Yan et al. 2026) as the certification-amenable architectural template.
- Addition of explicit stability and certification analysis (new Section 4).
- Explicit failure mode taxonomy with detection and response strategies.
- Training pipeline and sim-to-real discussion (new Section 5).
- International research landscape section (new Section 8) following the surfacing of Ma et al. 2026 (deep photonic reservoir computer integrated with UAV control). The presence of this work materially changed the brief from "this should be done" to "this is being done; here is the hypersonic-specific extension."
- Bibliographic verification pass on all primary citations following a Perplexity-flagged check. The verification confirmed the cited arXiv identifiers and caught one real attribution error: the 200 TOPS silicon photonic RC paper is by Wang, D., Nie, Y., Hu, G., Tsang, H. K., and Huang, C. (Chinese University of Hong Kong, Nature Communications 15, 10841, 2024), not "Tang et al." as initially attributed. Corrected throughout.

The convergent adversarial review identified a structural weakness in v1 that all three AI reviewers flagged independently: v1 made a computational-alignment argument when the field requires a certifiability argument. This insight reshaped the entire framing.

## v1.0 — April 2026

Initial draft. Argued for photonic reservoir computing as an alternative computational primitive for hypersonic GNC inner loops, with audience framed as a "deep-tech-aware former program executive" archetype. Adversarial review by Perplexity, GPT, and Gemini identified structural problems that drove the v2 rewrite.

---

## Methodological note

This brief was developed using iterated multi-AI adversarial review (Perplexity, GPT, Gemini, DeepSeek) across four drafts. The method is offered as a partial — not equivalent — substitute for conventional peer review, given that the work is unsponsored and conducted independently outside institutional affiliation. AI-assisted critique catches a meaningful subset of the issues that human domain experts would catch, but cannot substitute for the specific technical judgment that comes from having implemented hypersonic GNC, designed photonic devices, or led aerospace certification campaigns. Critique from human domain experts is explicitly welcomed via repository issues or pull requests.