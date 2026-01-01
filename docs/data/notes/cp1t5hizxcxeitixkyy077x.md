
- https://leodemoura.github.io/files/elaboration.pdf

## Abstract

We describe the elaboration algorithm that is used in [[prdct.lean]], a new interactive theorem prover based on dependent type theory. To be practical, interactive theorem provers must provide mechanisms to resolve ambiguities and infer implicit information, thereby supporting convenient input of expressions and proofs. Lean’s elaborator supports higher-order unification, ad-hoc overloading, insertion of coercions, type class inference, the use of tactics, and the computational reduction of terms. The interactions between these components are subtle and com- plex, and Lean’s elaborator has been carefully designed to balance effi- ciency and usability.