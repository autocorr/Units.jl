Units.jl
========
Manipulate units and physical quantities in Julia. Future functionality aims to
include `mks` and `cgs` units, constants, and dimensional analysis.


Installing
----------
As this package is still in a state of active development, it is not currently
available in the Julia package archive. To install and try it:

```julia
julia> Pkg.update()
julia> Pkg.clone("git://github.com/autocorr/Units.jl.git")
```

Usage
-----

```julia
julia> import Units; u = Units;
julia> q = u.Quantity(2, u.Meter)
Quantity(2,Meter,1,Length)
julia> 2 * u.Meter
Quantity(2,Meter,1,Length)
julia> 2q^2
Quantity(8,Meter,2,Length)
```

Info
----

Author  | Brian Svoboda
:-------|:--------------------------------------|
Email   | svobodb@email.arizona.edu             |
Source  | https://github.com/autocorr/Units.jl  |
Docs    | https://unitsjl.readthedocs.org       |
Version | alpha                                 |
Build   | [![Build Status](https://api.travis-ci.org/autocorr/Units.jl.svg?branch=master)](https://travis-ci.org/autocorr/Units.jl) |
