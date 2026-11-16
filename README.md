
# Analysis of the Creep Behaviour of Metallic Materials using Machine Learning and Numerical Simulation
 
LaTeX source of my M.Sc. thesis in Embedded Systems Engineering (AI specialization) at the University of Freiburg, written at Fraunhofer IWM within the EU project AID4GREENEST.
 
| | |
|---|---|
| **Author** | Arjun Gopalakrishnan |
| **Type** | Master's Thesis |
| **Institute** | IMTEK, Department of Microsystems Engineering, University of Freiburg |
| **Chair** | Laboratory for Micro and Materials Mechanics |
| **First examiner** | Prof. Dr. Christoph Eberl (University of Freiburg) |
| **Second examiner** | Prof. Dr. Anne Marie Habraken (ULiège) |
| **Supervisor** | Dr. Lukas Morand (Fraunhofer IWM, Machine Learning for Manufacturing Processes) |
| **Editing time** | November 1, 2024 to May 26, 2025 |
| **Submitted** | May 26, 2025 |
 
**Read the thesis:** [Thesis PDF](https://github.com/arjungkk/master-thesis/blob/main/main.pdf)
 
## Summary
 
Creep tests on metallic materials can run for thousands of hours. This thesis explores whether machine learning and finite element simulation can predict long-term creep behaviour from much shorter, accelerated tests.
 
- **Data generation:** 3,376 synthetic creep curves were produced with Morch's damage model, evaluated via finite element simulation in LAGAMINE, with parameters sampled by Latin hypercube sampling (LHS).
- **Curve representations:** theta projection, a three-parameter model, PCA and kernel PCA were compared as compact descriptions of creep curves.
- **Parameter recovery:** random forest, gradient boosting, stacking and voting regressors were trained to map curves back to material parameters. For most parameters this inverse problem turned out to be ill-posed.
- **Active learning:** a loop combining query-by-committee (MLP learner), an Isolation Forest region filter and a differential evolution optimizer, with FEA as the oracle, was evaluated against LHS for covering the data space more evenly. Results were mixed: fewer very early ruptures and more balanced flat curves, but fewer ruptured curves overall.
- **Outlook:** microstructure-based prediction and validation with real experiments.
## Skills demonstrated
 
Python, scientific machine learning (scikit-learn style regression, dimensionality reduction, active learning), finite element simulation workflows, experiment design and sampling strategies, and scientific writing in LaTeX.
 
## Repository structure
 
```
.
├── main.tex            # Entry point: metadata, front matter, chapter includes
├── settings+/          # Template settings (document class, language, covers, lists)
└── chapters/
    ├── abstract.tex
    ├── introduction.tex
    ├── theory.tex
    ├── methodology.tex
    ├── results.tex
    ├── discussion.tex
    ├── summary.tex
    ├── acknowledgments.tex
    └── appendix.tex
```
 
The bibliography is handled with BibLaTeX. Figures and bibliography files are stored alongside the chapters.
 
## Template
 
Built on the [EMES LaTeX template](https://github.com/imtekalex/emes_template) from the Laboratory for Electrical Instrumentation and Embedded Systems, University of Freiburg (Alexander Richter, Till Steinmann, Andreas Reichenbach).
 
## Related
 
- Code and experiments: [not public]
## Contact
 
Arjun Gopalakrishnan, [[LinkedIn](https://www.linkedin.com/in/arjungopalakrishnan/) / arjungcodes@gmail.com]
 
