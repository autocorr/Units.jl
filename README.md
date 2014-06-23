Units.jl
========
Manipulate units and physical quantities in Julia.


Installing
----------

    julia> Pkg.update()
    julia> Pkg.add("Units.jl")


Usage
-----

    julia> import Units; u = Units;
    julia> x = u.Quantity(2, u.Meter)


Author  | Brian Svoboda
--------|---------------------------------------|
Email   | svobodb@email.arizona.edu             |
Source  | https://github.com/autocorr/Units.jl  |
Docs    | https://unitsjl.readthedocs/en/latest |
Version | alpha                                 |
