# Certifiability of Deep Learning models in security critical industries such as automotive

**Problem**: Certification/Regulation aspects of Machine Learning are still unclear: no industry standards, no traceability between the algorithm implementation and its requirements, mostly no determinism in training, neural networks pose attack vectors.

**Notes**:
* DL/ML algorithms make mistakes and are never perfect - at the same time, they can't be interpreted ("black box nature"). This makes it to for them to obey legal guidelines society imposes. However, if they perform much better *on average*, possibly these guidelines need to be softened.
* Being hard to validate in real-world scenarios, deployment of neural networks poses certficiation challenges such as: **Is the dataset appropriate and free of undesirable bias?**, **Are learning process errors mitigated?**, **Does the model generalize to real-world scenarios and is it robust against adversarial examples?**, **Are there means for investigation of errors?**
* Most tenable approach for neural networks in particular: a priori training and validation, in-situ runtime monitoring.
* Current industry approaches for validation of algorithms are two-fold: via simulation (e.g. Waymo, "CarCraft" toolset) or fleet (Tesla).
* key enablers for certifiable deep learning algorithms: robust AI systems (to cyber- and adversarial attacks), provision of explainability, finding of holistic test suites for data (e.g. regularly spaced test grid), models and infrastructure (see a [recent post of mine](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/The%20ML%20Test%20Score:%20A%20Rubric%20for%20ML%20Production%20Readiness%20and%20Technical%20Debt%20Reduction.md)) 
* The US has taken a pioneering role with the [self drive act](https://www.congress.gov/bill/115th-congress/house-bill/3388), while the EU is still [lagging behind](https://oeil.secure.europarl.europa.eu/oeil/popups/ficheprocedure.do?lang=&reference=2018/2089(INI)), even though the importance has been acknowledged.
