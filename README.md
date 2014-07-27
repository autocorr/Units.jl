Units.jl
========
Algebraically manipulate units and physical quantities in Julia. `Units.jl`
uses the type system for logical unit system hierarchies, unit conversion, and
flexible user-defined units. Future functionality aims to include `mks` and
`cgs` units, constants, dimensional analysis, and electromagnetic units in
different `cgs` sub-systems. I started this project to explore Julia.  Other
active projects that support unit analysis in Julia include
[Physical.jl](https://github.com/ggggggggg/Physical.jl) and
[SIUnits.jl](https://github.com/Keno/SIUnits.jl). The API is modelled after
Python's [Pint](https://github.com/hgrecco/pint) and the
[Astropy](https://github.com/astropy/astropy) `units` sub-module.


Installing
----------
As this package is still in a state of active development, it is not currently
available in the Julia package archive. To install and try it:

```julia
julia> Pkg.update()
julia> Pkg.clone("git://github.com/autocorr/Units.jl.git")
julia> import Units; u = Units;
```


Example Usage
-------------
Detailed documentation will be made available on the
[ReadTheDocs](https://unitsjl.readthedocs.org) page once all core functionality
has been implemented. Example usage of `Units.jl` includes:

```julia
julia> import Units; u = Units;
julia> c = 2 * u.meter^(1//2) / u.second
2 Meter^¹/₂ Second^-1
julia> c.<tab>
base dim   mag   ord   unit
julia> (c.base, q.unit)
(Length,Meter)
julia> c.dim
Dimension(d=1//2, m=0, t=-1,  i=0, θ=0, n=0, j=0)
```


License
-------
`Units.jl` is released under the MIT license.


Info
----

Author  | Brian Svoboda
:-------|:--------------------------------------|
Email   | svobodb@email.arizona.edu             |
Source  | https://github.com/autocorr/Units.jl  |
Docs    | https://unitsjl.readthedocs.org       |
Version | alpha                                 |
Build   | [![Build Status](https://api.travis-ci.org/autocorr/Units.jl.svg?branch=master)](https://travis-ci.org/autocorr/Units.jl) |
