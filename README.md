About instaseis
===============

Home: http://instaseis.net

Package license: LGPL-3.0 (for non-commercial/academic use)

Feedstock license: BSD 3-Clause

Summary: Instant Global Broadband Seismograms Based on a Waveform Database

Instaseis calculates broadband seismograms from Green's function databases
generated with AxiSEM and allows for near instantaneous (on the order of
milliseconds) extraction of seismograms. Using the 2.5D axisymmetric
spectral element method, the generation of these databases, based on
reciprocity of the Green's functions, is very efficient and is approximately
half as expensive as a single AxiSEM forward run. Thus this enables the
computation of full databases at half the cost of the computation of
seismograms for a single source in the previous scheme and hence allows to
compute databases at the highest frequencies globally observed. By storing
the basis coefficients of the numerical scheme (Lagrange polynomials),
the Green's functions are 4th order accurate in space and the spatial
discretization respects discontinuities in the velocity model exactly. On
top, AxiSEM allows to include 2D structure in the source receiver plane and
readily includes other planets such as Mars.


Installing instaseis
====================

Installing instaseis from the conda-forge channel can be achieved by adding conda-forge to your channels with:

```
conda config --add channels conda-forge
```

Once the conda-forge channel has been enabled, instaseis can be installed with:

```
conda install instaseis
```

It is possible to list all of the versions of instaseis available on your platform with:

```
conda search instaseis --channel conda-forge
```


About conda-forge
=================

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](http://www.appveyor.com/)
and [TravisCI](https://travis-ci.org/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](http://docs.anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](http://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to regenerate all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy regenerate``.


Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)

Current build status
====================

Linux: [![Circle CI](https://circleci.com/gh/conda-forge/instaseis-feedstock.svg?style=shield)](https://circleci.com/gh/conda-forge/instaseis-feedstock)
OSX: [![TravisCI](https://travis-ci.org/conda-forge/instaseis-feedstock.svg?branch=master)](https://travis-ci.org/conda-forge/instaseis-feedstock)
Windows: ![](https://cdn.rawgit.com/conda-forge/conda-smithy/90845bba35bec53edac7a16638aa4d77217a3713/conda_smithy/static/disabled.svg)

Current release info
====================
Version: [![Anaconda-Server Badge](https://anaconda.org/conda-forge/instaseis/badges/version.svg)](https://anaconda.org/conda-forge/instaseis)
Downloads: [![Anaconda-Server Badge](https://anaconda.org/conda-forge/instaseis/badges/downloads.svg)](https://anaconda.org/conda-forge/instaseis)


Updating instaseis-feedstock
============================

If you would like to improve the instaseis recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/instaseis-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string)
   back to 0.
