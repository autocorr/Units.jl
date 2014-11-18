Getting Started
===============
`Units.jl` defines a great deal of symbols for units, so to not pollute the
namespace I prefer:

    julia> import Units; u = Units

However, in this documentation for the sake of clarity, `using Units` is used.


Unit Types
----------
Units are defined as types with capital letters (`Meter`) to let Julia keep track of their relationships within the type hierarchy. Here are some branches of the type tree as an example:

    Parsec <: Length <: Unit
    Year <: Time <: Unit

These generally follow a pattern of:

    Concrete Unit <: Unit Dimension <: Unit Top

One advantage of this system is that units can be differentiated even when they
have the same base representation in MKS or CGS unit systems, e.g. luminous
flux and luminous intensity.


Concrete Units
--------------
Concrete units are actual instances of unit types and are uncapitalized
(`meter`).  These are the primary interface to manipulate physical units with
`Units.jl`. Creating a composite unit is as simple as applying the normal
operations to the unit instances:

    julia> c = 2 * meter^(1//2) / second
    2.0 Meter^¹/₂ Second^-1

Equivalently, composite units can be parsed from strings directly by Julia:

    julia> c = Composite("2 * meter^(1//2) / second")
    2.0 Meter^¹/₂ Second^-1

The namespace is from within the module, so the namespace `Units.meter` or
`u.meter` can be omitted. Currently supported operations are:

    +, -, *, /, \, ^, ==, !=, >, <, <=, >=

where the comparison operators reduce two units to the same dimensions in the
base unit system (i.e. MKS) and then compare their numeric values. The next
section covers dimensions.


Dimensions
----------

