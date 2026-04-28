# Photonic Reservoir Computing for Hypersonic Guidance, Navigation, and Control

A technical brief arguing that photonic reservoir computing (PRC) is a credible candidate for a specific role within hypersonic GNC: a fast surrogate dynamical model embedded within a Predictive Safety-Stability Filter (PS2F) architecture, where classical model predictive control retains certified authority and the photonic reservoir provides the high-bandwidth, low-latency dynamical surrogate that makes inner-loop MPC tractable on hypersonic timescales.

## Scope

The brief argues for the architectural class — PRC as MPC surrogate within PS2F-architected hybrid control — with multiple candidate substrates warranting parallel investigation. It is not an advocacy document for any specific photonic device. It does not propose photonic RC as a replacement for classical flight computers. It does not claim the technology is ready for near-term deployment, and it does not claim the certification problem is solved.

The proposed role is restricted authority within a partitioned architecture, on a 5–10 year horizon for flight-relevant demonstration, with significant engineering work remaining at every milestone.

## Audience

Technically literate readers in the defense-aerospace research and acquisition community: engineers, program managers, and research staff with the background to evaluate the argument on its technical merits. The brief assumes familiarity with model predictive control, reservoir computing, and the basics of aerospace system certification. Acronyms are defined on first use.

## How to read

Twelve sections plus acknowledgments and references. For readers short on time, sections 2 (PS2F framing), 4 (stability and certification), 10 (open research questions), and 11 (scope) carry the central argument. The rest provides supporting detail.

The brief is approximately 6,800 words. Reading time is roughly 25–30 minutes.

## Repository contents

- `paper.md` — the v4 brief
- `index.html` — rendered HTML version for browser viewing
- `changelog.md` — version history and the role of adversarial review in shaping the argument
- `LICENSE` — Creative Commons Attribution 4.0
- `CITATION.cff` — formal citation metadata

## Method note

This brief was developed using iterated multi-AI adversarial review (Perplexity, GPT, Gemini, DeepSeek) across four drafts, each round producing structural critique that reshaped the work. This method is being used in lieu of conventional peer review because the work is unsponsored, conducted independently outside institutional affiliation, and not yet at a stage suitable for journal submission. AI-assisted adversarial review is offered as a partial — not equivalent — substitute for human domain expert review. A reader evaluating the brief should weigh this provenance accordingly.

The acknowledgments section of the brief itself documents what each review contributed.

## Related work

The Betsy architecture, named in section 7 as one candidate photonic RC design point, is developed separately in the [betsy-photonic-reservoir](https://github.com/bluebflatminor/betsy-photonic-reservoir) repository. That work is a speculative cavity-based architecture currently at TRL 2; this brief argues for the broader class of approach, with Betsy as one instantiation among candidates.

## Status

Version 4, April 2026. Technically defensible after four rounds of adversarial review and a verification pass on all primary references. Critique and correction from human domain experts are explicitly welcomed via repository issues or pull requests.

## License and citation

Released under Creative Commons Attribution 4.0 International (CC BY 4.0). Use, share, and adapt with attribution. Formal citation metadata is in `CITATION.cff`.
