# Fock Basis

```@example
using QuantumOptics # hide
N = 10
b = FockBasis(N)
alpha = 0.4
psi = coherentstate(b, alpha)
a = destroy(b)
nothing # hide
```

A fock space describes the situation of variable particle number. I.e. the system can have zero particles, one particle, two particles and so on.

To create a basis of a Fock space **QuantumOptics.jl** provides the [`FockBasis`](@ref) class which has to be supplied with an integer specifying the maximum number of photons. It is defined as:

```julia
type FockBasis <: Basis
    shape::Vector{Int}
    N::Int
end
```

## States

* [`fockstate`](@ref)
* [`coherentstate`](@ref)


## Operators

* [`number`](@ref)
* [`destroy`](@ref)
* [`create`](@ref)


## Additional functions

* [`qfunc`](@ref)


## Examples

* [Example: Pumped cavity](@ref)
* [Example: Jaynes-Cummings](@ref)
* [Example: Correlation spectrum](@ref)