
# Sphere Dimensions

!!! note
    In all of the following setups the sphere is embedded in a homogeneous background medium with permeability ``\mu`` and permittivity ``\varepsilon`` defined by [`Medium(ε, μ)`](@ref). The values [`μ0`](@ref) and [`ε0`](@ref)  are provided containing the free space values.


---
## PEC/PMC Sphere

The perfectly electrically conducting (PEC) or perfectly magnetically conducting (PMC) sphere has radius ``r`` and is assumed to be located in the origin. It is defined by [`PECSphere`](@ref).
```@raw html
<div align="center">
<img src="../assets/PECsphere.svg" width="300"/>
</div>
<br/>
```

#### [API](@id pecAPI)

```@docs
PECSphere
```


---
## Dielectric Sphere

The dielectric sphere has radius ``r`` and is assumed to be located in the origin. It is defined by [`DielectricSphere`](@ref). In addition to the embedding [`Medium(ε, μ)`](@ref) a filling [`Medium(εᵢ, μᵢ)`](@ref) with permeability ``\mu_\mathrm{i}`` and permittivity ``\varepsilon_\mathrm{i}`` has to be defined. 
```@raw html
<div align="center">
<img src="../assets/DielectricSphere.svg" width="300"/>
</div>
<br/>
```

#### [API](@id dielecAPI)

```@docs
DielectricSphere
```
Here `radius` is a Float and `filling` of type [`Medium(εᵢ, μᵢ)`](@ref).


---
## Layered Dielectric Sphere

The layered dielectric sphere has radii ``[r_1, r_2, \dots, r_N]`` and is assumed to be located in the origin. It is defined by [`LayeredSphere`](@ref). In addition to the embedding [`Medium(ε, μ)`](@ref) a vector of fillings [[`Medium(ε₁, μ₁)`](@ref), [`Medium(ε₂, μ₂)`](@ref), ..., [`Medium(εN, μN)`](@ref)] with permeability ``\mu_n`` and permittivity ``\varepsilon_n`` has to be defined.
```@raw html
<div align="center">
<img src="../assets/LayeredSphere.svg" width="300"/>
</div>
<br/>
```

#### [API](@id mlDielecAPI)

```@docs
LayeredSphere
```
with, e.g., `radii = SVector(1.0, 0.5, 0.25)` and `radii = SVector(Medium(ε1, μ1), Medium(ε2, μ2), Medium(ε3, μ3))`.

!!! warning
    The order of the radii does not yet match the image!


---
## Layered Dielectric Sphere with PEC Core

The layered dielectric sphere has radii ``[r_1, r_2, \dots, r_{N+1}]`` and is assumed to be located in the origin. It is defined by [`LayeredSpherePEC`](@ref). In addition to the embedding [`Medium(ε, μ)`](@ref) a vector of fillings [[`Medium(ε₁, μ₁)`](@ref), [`Medium(ε₂, μ₂)`](@ref), ..., [`Medium(εN, μN)`](@ref)] with permeability ``\mu_n`` and permittivity ``\varepsilon_n`` has to be defined.
```@raw html
<div align="center">
<img src="../assets/LayeredSpherePEC.svg" width="300"/>
</div>
```

#### [API](@id mlDielecPecAPI)

```@docs
LayeredSpherePEC
```
with, e.g., `radii = SVector(1.0, 0.5, 0.25)` and `radii = SVector(Medium(ε1, μ1), Medium(ε2, μ2))`.

!!! warning
    The order of the radii does not yet match the image!


---
## [Dielectric Sphere with Thin Impedance Layer](@id dielecimped)

The dielectric sphere with a thin impedance layer of thickness ``t`` has radius ``r`` and is assumed to be located in the origin. It is defined by [`DielectricSphereThinImpedanceLayer`](@ref). Unlike the LayeredSphere model, the solution is obtained by using an approximation: it is assumed that the impedance is so high that the displacement field is purely radial (see [[6, pp. 230ff]](@ref refs)). This leads to a potential drop across the thin layer, while the displacement field is constant in radial direction. In addition to the embedding [`Medium(ε, μ)`](@ref) and  filling [`Medium(εᵢ, μᵢ)`](@ref), the impedance layer must be specified, both the [`Medium(εₜ, μₜ)`](@ref) and its `thickness`.  
```@raw html
<div align="center">
<img src="../assets/ImpedanceLayer.svg" width="300"/>
</div>
<br/>
```

!!! note
    This configuration is (at least so far) only intended for the [uniform static field](@ref uniformEx) excitation.

#### [API](@id dielecimpedAPI)

```@docs
DielectricSphereThinImpedanceLayer
```
Here `radius` and `thickness` are a Floats, `embedding`, `filling` and `thinlayer` are of type [`Medium`](@ref).
