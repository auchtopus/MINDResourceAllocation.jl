## Sigmoidal Resource Allocation on MIND

This is a simulation/experiment of using sigmoidal programming for resource allocation optimization on MIND

This solves the problem on a single resource (cache), assuming that `throughput = f(cache)` can be modelled as a sigmoidal function, thus permitting simulation as a sigmoidal programming problem. A more complete writeup can be found in the pdf, but the gist is that we use `SigmoidalProgramming.jl` to solve problems of the form:

```math
\begin{align*}
\max \sum_{i=1}^n f_i(c_i)  \\
\text{subject to } \sum_{i=1}^n c_i = C
\end{align*}
```
where $f_i$ is sigmoidal.

The simulation is currently running on simple sigmoids, not a differnece of sigmoids of of a sigmoid minus convex function. 

### Usage
The simulation is found in `src/MIND_sigmoidal_programming.ipynb` and needs a julia installation to run. The current version `1.6` will suffice, and can be run as any other julia notebook. Instructiosn can be found here: https://julialang.github.io/IJulia.jl/stable/manual/running/
