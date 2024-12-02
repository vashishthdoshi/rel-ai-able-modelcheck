![image](https://github.com/user-attachments/assets/772095dd-08f9-40ca-a51d-fc78de642139)

# rel-AI-able-modelcheck

This repository contains benchmark models that test your code. These tests generate JSON reports that can be uploaded to our website for reliability reports on hallucinations, robustness, accuracy, and other principles of Responsible AI.

---

## README

This readme explains the purpose and use of this repository as a framework to ensure that an AI model is technically aligned with US AI regulations and best practice requirements, as well as the process of building this repository further.

---

## About the Project

This project was created by Heinz College students at Carnegie Mellon University as a product for a client under the Policy Innovation Lab course. Contact information for the students can be found at the end of this document.

---

## Larger Interface

This GitHub repository is part of a larger interface available [here](<figma>). The general purpose of the interface is to tie together the knowledge base in AI Risk Mitigation, the regulations and frameworks already in place for AI in the US like `<framework 01>`, `<framework 02>`, `<framework 03>`, and mapping technical benchmarks to those regulations. The interface allows developers to:

- Test AI solutions locally during development.
- Access a guidebook for AI Red-Teaming and risk mitigation for whatever stage of the AI lifecycle your product may be in.
- Map technical benchmarks to U.S. AI regulations and frameworks.

The idea is to solve for the developer's need to test their model locally against technical benchmarks which 'meet the regulations'. This local test's results then can be uploaded to the interface for an evaluation to be generated. 

The use of this evaluation report is for developers to understand which metric their model doesn't align with and why. The entire framework's purpose is to make the sometimes vague, and other times complicated requirements that regulations establish accessible to developers. The benchmark models are the developments of academic research based on the regulations, and this mapping is available in the respective benchmarks metadata. When policy is established, academic research finds the appropriate technical interpretation. This technical interpretation or 'benchmark model' can act as a standard relative to which your model is locally evaluated.

1. **Local Testing**: Developers test their models locally against technical benchmarks that align with regulations.
2. **Upload Results**: JSON reports generated by the local tests can be uploaded to the interface for evaluation.
3. **Evaluation Report**: Developers receive a detailed report highlighting metrics where the model may not align with regulatory requirements and why.

---

## Design Inspiration and Philosophy

This framework was inspired by [COMPL-AI.org](https://compl-ai.org), which our user research identified as an accessible solution for enabling small-scale models to comply with governance standards and regulations. We consider this as 'derived work' under their licensing.

---

## Current State and Future Vision

This repository is currently a shadow repository of a [technical skeleton](<technical skeleton figma>) of our imagined solution. It demonstrates the framework's functionality with the potential for future expansion into a more comprehensive evaluation tool.

```
rel-AI-able-modelcheck/main/
    - benchmarks/models                    # Evaluation tools for compliance testing
        - fairness/
            - fairness_benchmark.py  # Fairness evaluation script
            - test_cases.json        # Test cases for fairness assessments
        - robustness/
            - adversarial_tests.py   # Scripts for adversarial robustness
            - perturbation_metrics.py
        - privacy/
            - data_leakage_check.py  # Privacy evaluation scripts
            - memorization_tests.py

    - requirements/
        - us_ai_regulations.md       # Summary of U.S. AI regulatory landscape
        - nist_guidelines.md         # Key principles of NIST AI Risk Framework

    - tools/                         # Utility scripts for running evaluations
        - evaluation_runner.py       # Main script for running evaluations

    - tests/                         # Automated testing for codebase
        - unit/
            - test_benchmark_functions.py
        - integration/
            - test_full_pipeline.py

    - .github/
        - workflows/
            - ci.yml                 # Continuous Integration (CI) pipeline
            - codeql-analysis.yml    # Security analysis

    - LICENSE                        # Repository licensing information
    - setup.py                       # Setup script for the repository
    - requirements.txt               # Python dependencies
    - README.md                      # Overview and setup instructions
    - CONTRIBUTING.md                # Guide for contributors
    - API.md                         # API documentation for benchmarks
    - US_AI_Regulations.md           # Details on the regulations addressed
```
## Contact
  Christian A Borrero candino@andrew.cmu.edu | Lisa Menda lmenda@andrew.cmu.edu | Grace Sam gsam@andrew.cmu.edu | Zachary Zwijacz zzwijacz@andrew.cmu.edu | Vashishth Doshi vbd@andrew.cmu.edu

## Citations
    Guldimann, P., Spiridonov, A., Staab, R., Jovanović, N., Vero, M., Vechev, V., Gueorguieva, A., Balunović, M., Konstantinov, N., Bielik, P., Tsankov, P., & Vechev, M. (2024). COMPL-AI Framework: A Technical Interpretation and LLM Benchmarking Suite for the EU Artificial Intelligence Act. arXiv. https://arxiv.org/abs/2410.07959
        
    (2024). [GitHub Repository Purpose, Content and Design]. https://docs.google.com/document/d/1rGoSqr3MN4ac5GHFD1ERGHKpxcrk6SoM/edit?usp=sharing&ouid=114720471682987242471&rtpof=true&sd=true
