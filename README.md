# Home

[GitHub Repository](https://github.com/DynaHug-Detector/dynahug.github.io)

# DynaHug: Learning to Detect Malicious Pre-trained Models via Dynamic Analysis

A Machine Learning based dynamic analysis approach to detecting malicious Pre-trained models.

## Overview

Pre-trained machine learning models (PTMs) are
commonly provided via Model Hubs (e.g., Hugging Face) in
standard formats like Pickles to facilitate accessibility and
reuse. However, this ML supply chain setting is susceptible
to malicious attacks that are capable of executing arbitrary
code on trusted user environments, e.g., during model load-
ing. To detect malicious PTMs, state-of-the-art detectors (e.g.,
PickleScan) rely on rules, heuristics, or static analysis, but ig-
nore runtime model behaviors. Consequently, they either miss
malicious models due to under-approximation (blacklisting)
or miscategorize benign models due to over-approximation
(static analysis or whitelisting). To address this challenge,
we propose a novel technique (DYNAHUG) which detects
malicious PTMs by learning the behavior of benign PTMs
using dynamic analysis and machine learning (ML). DYNAHUG
trains an ML classifier (one-class SVM (OCSVM)) on the
runtime behaviours of task-specific benign models. We evaluate
DYNAHUG using over 18,000 benign and malicious PTMs from
different sources including Hugging Face and MALHUG. We
also compare DYNAHUG to several state-of-the-art detectors
including static, dynamic and LLM-based detectors. Results
show that DYNAHUG is up to 44% more effective than existing
baselines. Our ablation study demonstrates that our design
decisions (dynamic analysis, OCSVM, clustering) contribute
positively to DYNAHUG’s effectiveness. This work motivates
the need for dynamic analysis in malicious PTM detection.

