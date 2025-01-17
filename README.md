
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/src/assets/logo_Scat_README_white.svg" height="190">
  <source media="(prefers-color-scheme: light)" srcset="docs/src/assets/logo_Scat_README.svg" height="190">
  <img alt="" src="" height="190">
</picture>

[![Stable](https://img.shields.io/badge/docs-stable-blue.svg)](https://hobezwe.github.io/SphericalScattering.jl/dev/)
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/HoBeZwe/SphericalScattering.jl/blob/master/LICENSE)
[![CI](https://github.com/HoBeZwe/SphericalScattering.jl/actions/workflows/CI.yml/badge.svg?branch=master)](https://github.com/HoBeZwe/SphericalScattering.jl/actions/workflows/CI.yml)
[![codecov](https://codecov.io/gh/HoBeZwe/SphericalScattering.jl/branch/master/graph/badge.svg?token=4F9NUNRC1K)](https://codecov.io/gh/HoBeZwe/SphericalScattering.jl)
[![DOI](https://zenodo.org/badge/375493054.svg)](https://zenodo.org/badge/latestdoi/375493054)

## Introduction

This package provides semi-analytical solutions to the scattering of time harmonic and static electromagnetic fields from spherical objects (amongst others known as Mie solutions or Mie scattering). 
To this end, series expansions are evaluated. Special care is taken to obtain accurate solutions down to the static limit.

The following aspects are implemented (✔) and planned (⌛):

##### Available incident fields:
- ✔ Plane wave
- ✔ Field of electric/magnetic ring current
- ✔ Field of electric/magnetic dipole
- ✔ TE/TM spherical vector waves
- ✔ Uniform static electric field
- ⌛ Static charge(s)

##### Available scattering objects:
- ✔ PEC sphere
- ⌛ PMC sphere
- ⌛ Dielectric sphere                          (✔ for uniform static field & plane-wave)
- ⌛ Multilayer dielectric sphere               (✔ for uniform static field)
- ⌛ Multilayer dielectric sphere with PEC core (✔ for uniform static field)
- ✔ Dielectric sphere with thin impedance layer

##### Available quantities (where applicable):
- ✔ Far-fields
- ✔ Near-fields (electric & magnetic)
- ⌛ Radar cross section (RCS)
- ⌛ Surface currents
- ✔ Scalar potentials 
- ✔ Displacement fields 
- ✔ Scalar potential jump 



## Citation

Please cite this package following the information on [Zenodo](https://zenodo.org/badge/latestdoi/375493054).



## Documentation

Here you can find the [documentation](https://hobezwe.github.io/SphericalScattering.jl/dev/).