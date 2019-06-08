<!-- TITLE: Md -->
<!-- SUBTITLE: A quick summary of Md -->

# Molecular Dynamics is the basic framework behind most of what we do
Recommend Andrew Leach's book: Molecular Modeling Principles and Applications

And this paper will have th foundations of Molecular Dynamics:
Braun, E., Gilmer, J., Science, H. M. M., 2018. (n.d.). Best Practices for Foundations in Molecular Simulations [Article v1. 0]. Livecomsjournal.org
.

# 1. Force fields:
     a. What is a force field?

             i. Bonded and non-bonded terms.

            ii. How do we calculate partial charges on atoms?

           iii. Which interactions are long-range and which are short range?

     b. What does transferability mean when applied to force fields?

     c. Differences and similarities between fixed charged and polarizable force fields.

     d. Solvent models:

             i. Implicit: Generalized Born (GB), GB-neck2

            ii. Explicit: SPC, TIP3P

           iii. Vacuum

     e.  What does "combination rules" mean in the context of force fields?

     f. Differences between United, all atom, coarse-grained force fields.

     g. Periodic Boundary Conditions, Particle Mesh Ewald, Cutoff methods.

# 2. Sampling complex energy surfaces
    a. Minimization

             i. Steepest descent.

            ii. Conjugate Gradient.

     b. Molecular Dynamics

             i. Barostats.

            ii. Termostats.

           iii. Time-step, multiple time-step, hydrogen mass repartitioning.

           iv.  Equilibration vs Production.

           v.  Ensembles: NPT, NVT, NVE, ...