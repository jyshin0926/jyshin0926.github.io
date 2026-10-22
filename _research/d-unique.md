---
title: "D-UNIQE: Descriptive Unified Speech Quality and Emotion Assessment for Emotional TTS"
excerpt: "A speech LLM that jointly assesses naturalness, audio quality, and emotion with perceptual explanations.<br/><img src='/images/duniqe-framework.png' alt='D-UNIQE framework figure from the paper'>"
collection: research
---

D-UNIQE is a unified evaluator for naturalness, audio quality, and emotional fidelity in emotional TTS. Frozen Whisper, BEATs, and AVD encoders provide semantic, acoustic, and affective speech features. A windowed Q-Former and task-routed projection mixture-of-experts map these features to a LoRA-adapted Vicuna-7B model, which generates scores and perceptual explanations. GRPO-QTR trains score accuracy and score-explanation consistency for the two score-based quality tasks.

On held-out evaluations, D-UNIQE reports naturalness SRCC 0.726 and PCC 0.727, and audio-quality MSE 0.336, SRCC 0.808, and PCC 0.824. It achieves emotion accuracy 0.658, with CCC 0.606 and PCC 0.624 for dimensional affect. In a matched naturalness analysis, soft task routing raises score-description correlation to 0.890 and reduces observed high-score/negative-description contradictions to 0%.

<figure>
	<img src="/images/duniqe-framework.png" alt="D-UNIQE framework from the paper">
	<figcaption>Overview of D-UNIQE: multi-encoder speech representations feed a task-routed projection module and language model, with supervised and GRPO-QTR training stages.</figcaption>
</figure>

The paper is under review at ICASSP 2027.

- [Open the listening demo](https://jyshin0926.github.io/DUNIQE/)
- [View the source on GitHub](https://github.com/jyshin0926/DUNIQE)