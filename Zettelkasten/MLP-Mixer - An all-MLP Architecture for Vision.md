---
tags:
  - paper
  - rate-no
---
URL: 
Review: https://openreview.net/forum?id=EI2KOXKdnP
Review average (1-5): 3
Conf: NeurIPS 2021

---

Basically computer vision only with MLP (no CNN involved)

Moreover, this claim is equally true for both Vision Transformer and MLP-Mixer: compared to CNNs, both models require more data (or more aggressive augmentation techniques) to achieve the same performance. Recent works [Touvron et al., 2020, Steiner et al., 2021] have shown that additional regularization and tricks can be used instead of data for Vision Transformers; we believe similar advances will be worth exploring for MLP-Mixer also.

---

Initially, the paper received scores 7, 7, 6, and 5. All reviewers consider the idea is very interesting, experiments are comprehensive, the paper is well-written, and results are strong given the simplicity of the model. At the same time, multiple concerns were raised, specifically pointing out limitations of the model ( e.g., inability to handle multiple resolutions and tasks such as detection/segmentation; the model is data-hungry, parameter-inefficient, and tailored to specialized hardware/TPUs). During the discussion phase, two reviewers were disappointed by the author response, which did not address well questions such as reporting ImageNet results from other architectures, adopting the same training procedure as in DeiT, and over claimed significance of results. They downgraded their rating from 7 to 6, still recommending borderline acceptance. While the concerns raised by the reviewers are all legitimate, the AC considers that the strengths of the paper outweighs its weaknesses, and agrees with the majority that it passes the acceptance bar of NeurIPS. In particular, the proposed architecture has the potential to make an impact and inspire further research in the field, as it is conceptually simple yet achieves strong results. The authors should include in the camera-ready the discussion based on reviewer’s comments, properly convey the limitations of the architecture, and also address the two ethical concerns pointed out in the ethics review.