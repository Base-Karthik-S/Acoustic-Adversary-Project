# Acoustic-Adversary-Project
This research project investigates the adversarial robustness of deep audio classification models by implementing and comparing two gradient-based attack methods: the Fast Gradient Sign Method (FGSM) and Projected Gradient Descent (PGD).

Using Google’s YAMNet, a pre-trained EfficientNet-based model trained on AudioSet, we assessed the model’s classification performance under adversarial perturbations. A LibriSpeech audio sample served as the input waveform for the experiment.

Both FGSM and PGD attacks were executed across varying perturbation strengths (Ɛ) in incremental batch tests to examine the relationship between attack intensity and classification confidence. Key findings revealed that:

FGSM led to moderate confidence degradation but rarely caused misclassification.

PGD consistently induced label flipping, even under high signal-to-noise ratios (SNR > 17 dB).

These results underscore the vulnerability of deep auditory models to iterative gradient-based attacks and emphasize the critical need for robust defense mechanisms in safety-critical audio recognition systems, such as speech and sound monitoring applications.

Technical implementation was carried out in a TensorFlow-based Jupyter Notebook, including waveform processing, baseline classification, adversarial attack execution, and evaluation using metrics such as Top-1 confidence, SNR, and Attack Success Rate (ASR).

This work contributes to the emerging field of audio adversarial machine learning, bridging a gap between widely studied image-domain attacks and the less-explored audio modality, with implications for secure and reliable AI-powered sound recognition.
