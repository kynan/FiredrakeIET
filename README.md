# Solving partial differential equations using the finite element method efficiently and productively with Firedrake and PyOP2

## http://firedrakeproject.org

### **Florian Rathgeber**<sup>0</sup>, Lawrence Mitchell<sup>1</sup>, David Ham<sup>1,2</sup>, Michael Lange<sup>3</sup>, Andrew McRae<sup>2</sup>, Fabio Luporini<sup>1</sup>, Gheorghe-teodor Bercea<sup>1</sup>, Paul Kelly<sup>1</sup>

<sup>0</sup> Data Handling Team, Development Section, Forecast Department, ECMWF  
<sup>1</sup> Department of Computing, Imperial College London  
<sup>2</sup> Department of Mathematics, Imperial College London  
<sup>3</sup> Department of Earth Science & Engineering, Imperial College London

Slides from an [invited seminar](http://cmg.soton.ac.uk/events/event-794/) at
the [Computational Modelling Group](http://cmg.soton.ac.uk/) led by [Prof. Hans
Fangohr](http://cmg.soton.ac.uk/people/fangohr/) at the University of
Southampton on November 27th:
http://kynan.github.io/FiredrakeSeminarSoton

Hans [blogged] about the seminar.

[blogged]: http://ngcm.soton.ac.uk/blog/2014-11-27/seminar-by-florian-rathgeber-on-solving-pdes-using-firedrake.html

### Abstract

In this talk I will give an overview of my PhD research in computational
science at Imperial College London before joining ECMWF, which involved
designing and implementing a two-layer domain-specific framework for the
efficient solution of partial differential equations from a high-level problem
specification. I will present Firedrake, a high-level framework for solving
partial differential equations using the finite element method, built on top of
PyOP2, a domain-specific language embedded in Python for parallel mesh-based
computations. I am going to highlight characteristic features that
differentiate this tool chain from existing solutions, reflect on the process
of designing and implementing the framework and discuss some lessons learnt in
running an academic open source software project.

Firedrake allows scientists to describe variational forms and discretisations
for linear and non-linear finite element problems symbolically, in a notation
very close to their mathematical models. PyOP2 abstracts the
performance-portable parallel execution of local computations over the mesh on
a range of hardware architectures, targeting multi-core CPUs, GPUs and
accelerators. Thereby, a separation of concerns is achieved, in which Firedrake
encapsulates domain knowledge about the finite element method separately from
its efficient parallel execution in PyOP2, which in turn is completely agnostic
to the higher abstraction layer.

As a consequence of the composability of those abstractions, optimised
implementations for different hardware architectures can be automatically
generated without any changes to a single high-level source. Performance
matches or exceeds what is realistically attainable by hand-written code.
Firedrake and PyOP2 are combined to form a tool chain that is demonstrated to
be competitive with or faster than available alternatives on a wide range of
different finite element problems.

### Resources

  * **PyOP2** https://github.com/OP2/PyOP2
    * *[PyOP2: A High-Level Framework for Performance-Portable Simulations on Unstructured Meshes](http://dx.doi.org/10.1109/SC.Companion.2012.134)*  
      Florian Rathgeber, Graham R. Markall, Lawrence Mitchell, Nicholas Loriant, David A. Ham, Carlo Bertolli, Paul H.J. Kelly,
      WOLFHPC 2012
    * *[Performance-Portable Finite Element Assembly Using PyOP2 and FEniCS](http://link.springer.com/chapter/10.1007/978-3-642-38750-0_21)*  
       Graham R. Markall, Florian Rathgeber, Lawrence Mitchell, Nicolas Loriant, Carlo Bertolli, David A. Ham, Paul H. J. Kelly ,
       ISC 2013
  * **Firedrake** https://github.com/firedrakeproject/firedrake
    * *[Productive and Efficient Computational Science Through Domain-specific Abstractions](https://wwwhomes.doc.ic.ac.uk/~fr710/Rathgeber-F-2014-PhD-Thesis.pdf)*  
      Florian Rathgeber, PhD thesis, October 2014
    * *[Cross-Loop Optimization of Arithmetic Intensity for Finite Element Local Assembly](http://arxiv.org/abs/1407.0904)*
      Fabio Luporini, Ana Lucia Varbanescu, Florian Rathgeber, Gheorghe-Teodor Bercea, J. Ramanujam, David A. Ham, Paul H. J. Kelly
  * **UFL** https://bitbucket.org/mapdes/ufl
  * **FFC** https://bitbucket.org/mapdes/ffc
