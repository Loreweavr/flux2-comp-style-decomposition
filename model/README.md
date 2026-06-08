# orph_light — style_8k (value-painting LoRA)

The deliverable from the composition-vs-style decomposition. See [`../splitting-a-flux2-lora.md`](../splitting-a-flux2-lora.md) for the full story.

- **Download:** [huggingface.co/loreweavr/orph_light_style_8k](https://huggingface.co/loreweavr/orph_light_style_8k) (file `FLUX2_orph_light_style_v1.0_000008000.safetensors`, ~1.56 GB).
- **Base model:** FLUX.2-dev
- **Trigger word:** `orph_light`
- **Recommended strength:** 1.0 (full). Drop to 0.6–0.8 on faces and on subjects far from the training set.
- **Checkpoint:** step 8000, the locked midpoint. Past ~10k the style LoRA overcooks into prompt-agnostic memorization, so cap there.
- **What it does:** paints a scene in dynamic black-and-white value structure, with crisp light and dark masses doing the work, and lands composition most of the time on its own. It is the project's actual product: value-painting turned out to live in the style branch, not the composition one.
- **Tested with:** dpmpp_2s_ancestral / sgm_uniform, 20 steps, guidance 2.5.

## License
Derived from **FLUX.2-dev**, which ships under Black Forest Labs' non-commercial license. This LoRA inherits those terms. Treat it as non-commercial and review the FLUX.2-dev license before any redistribution or commercial use.
