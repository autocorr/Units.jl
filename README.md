Units.jl
========
Manipulate units and physical quantities in Julia. Future functionality aims to include `mks` and `cgs` units, constants, and dimensional analysis.


Installing
----------
As this package is in an immature state, it is not currently available in the Julia package archive. To install and try it:

```julia
julia> Pkg.update()
julia> Pkg.clone("git://github.com/autocorr/Units.jl.git")
```

Usage
-----

```julia
julia> import Units; u = Units;
julia> x = u.Quantity(2, u.Meter)
Quantity(2,Meter,1,Length)
julia> 2x^2
Quantity(16.0,Meter,2,Length)
```

Info
----

Author  | Brian Svoboda
:-------|:--------------------------------------|
Email   | svobodb@email.arizona.edu             |
Source  | https://github.com/autocorr/Units.jl  |
Docs    | https://unitsjl.readthedocs/en/latest |
Version | alpha                                 |
