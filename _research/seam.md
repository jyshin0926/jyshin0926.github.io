---
title: "SEAM: Speech Emotion-Aligned Controllable Music Generation"
excerpt: "Speech affect guides music mood while text independently controls instrumentation.<br/><img src='/images/seam-framework.png' alt='SEAM speech-conditioned music generation framework'>"
collection: research
---

SEAM transfers the affect of expressive speech to newly generated instrumental music while an emotion-free text prompt specifies the musical content. A lightweight conditioner for frozen Stable Audio 3 maps speech into separate valence and arousal tokens, injected through mood cross-attention while preserving the text-conditioning pathway. At inference, baseline-relative steering in speech-emotion representation space controls affect intensity without adding emotion words or VA values to the prompt.

Evaluation uses IEMOCAP and ESD speech paired with Jamendo music. On held-out IEMOCAP Session 5, SEAM reaches a valence-arousal distance of 0.81, compared with 0.92 for numeric-VA prompts and 0.96 for lexical prompts. On held-out ESD speakers, emotion-prototype accuracy is 0.88 versus 0.33 for lexical prompting. In a 43-person listening study, SEAM receives the highest emotion-alignment ratings for happy, sad, and angry conditions; its intensity-control trajectories move toward the target affect, though not perfectly monotonically.

<figure>
	<img src="/images/seam-framework.png" alt="SEAM training and inference architecture">
	<figcaption>SEAM separates text-based music prompting from speech-derived affect, then injects factorized valence and arousal tokens into a frozen Stable Audio 3 backbone.</figcaption>
</figure>

<figure>
	<img src="/images/seam-intensity.png" alt="Valence and arousal trajectories across speech-residual steering intensity">
	<figcaption>Automatic valence and arousal estimates across five steering strengths for happy and sad speech, comparing speech-residual steering with lexical blending.</figcaption>
</figure>

The paper is under review at ICASSP 2027.

- [Open the listening demo](https://jyshin0926.github.io/SEAM/)
- [View the source on GitHub](https://github.com/jyshin0926/SEAM)