# Files for Rebuttal of ICML 2025 Submission 7638

In this repository, we release files as requested by reviewers. These files demonstrate that our method is easy to use, and that the comparison made in the paper was fair.

As requested by all Reviewers, we release the original hinted images and masks we used for Section 3.1. The images can be found in the folder `ChainReaction`. All hints and masks are **casually drawn**, yet the editing results are of high quality. This supports our claims that our method is robust, and that the burden on the user is extremely low.
- `*.jpg` is the hint.
- `*-mask.jpg` is the mask.
- `*-result.jpg` is the editing result.

As requested by Reviewer S8do, we use FLUX.1 Dev Fill ("flux inpainting") as an additional baseline. The results can be found in the folder `Flux.1-Fill-dev`. We use the same masks as for our workflow. While FLUX.1 Dev Fill is a strong baseline, it falls short in the following aspects:
- Background editing ability is weak. The images in `bg_change` are mostly failures.
- Global color outside the editing region can sometimes be altered. The 9th image in `obj_remo` is an obvious example, where the color of the grass has shifted. The global color change is also [reported by the model developers](https://huggingface.co/black-forest-labs/FLUX.1-Fill-dev#limitations), a limitation that makes FLUX.1 Dev Fill unsuitable for iterative editing.
-  FLUX.1 Dev Fill has a tendency to replicate objects. The 9th image in `obj_addi`, 11th image in `obj_addi`, and 11th image in `obj_remo` are obvious examples. Our method is designed to resolve this issue by color hints.

As requested by Reviewer S8do, we try to use MGIE as another baseline. Partial results can be found in the folder `MGIE`. We used the [official demo of MGIE](https://huggingface.co/spaces/tsujuifu/ml-mgie). We only provide partial results here due to time constraints, but we will include a larger-scale qualitative comparison in the final version of the paper.

Finally, the folder `EditEval` contains the original images and editing instructions in the benchmark. The official link is [here](https://github.com/SiatMMLab/Awesome-Diffusion-Model-Based-Image-Editing-Methods?tab=readme-ov-file#benchmark-editeval_v2).

If you have any remaining questions or requests for other files, please feel free to ask on OpenReview. We are happy to respond.