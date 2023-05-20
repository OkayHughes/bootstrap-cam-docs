# Bootstrapping CAM "documentation" using `doxygen`
The `doxygen` library can generate automatic documentation from a codebase, which can infer call signatures for subroutines,
inter-module dependencies, and caller/callee trees for Fortran code. It tends to be even more useful for C/C++ code.
Much like the statistical bootstrap, `doxygen` can blow the head off of the problem of generating documentation,
but only if the developer is willing to deal with the resulting mess. This is my first attempt at trying to make sense of this mess.
In my personal work on the CAM dynamical cores, I find that the auto-generated caller/callee graphs are
invaluable for ensuring that changes that I change every last invocation of a subroutine when I change what it does or how it is called.
Furthermore, I find that the graphical call trees are quite helpful for determining where in the top-level CAM physics/dynamics sequence a
subroutine (potentially buried deep within a parameterization) is invoked. 
