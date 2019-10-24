Modified version of Christopher O'Neill's NumericalSemigroup Sage class, updated for use as a Python package.

# numsgps-sage

Provides a Python class `NumericalSemigroup` for use with the computer algebra system [Sage](http://sagemath.org/) that adds functionality for working with numerical semigroups. Internally, it uses the [GAP](http://www.gap-system.org/) package [numericalsgps](http://www.gap-system.org/Packages/numericalsgps.html), and is intended to help ease the interface between Sage and the GAP package.

- All types returned are true Sage types, not just wrappers around GAP types.
- Autocomplete is supported in the Sage web interface. See the sample code below.
- Most factorization invariants supported by GAP are implemented, and more functionality will continue to be added. In fact, feature requests are encouraged, just send me an email!

You can find action shots in the `images` folder.

Please note that this is an _alpha version_ and subject to change without notice.

## License

numsgps-sage is released under the terms of the [MIT license](https://tldrlegal.com/license/mit-license). The MIT License is simple and easy to understand and it places almost no restrictions on what you can do with this software.

## Usage

To set up your machine to use numsgpssage, do the following.

- First, install Sage on your machine. Instructions for doing so can be found [here](http://sagemath.org/).
- Next, install the GAP package numericalsgps into your Sage installation. Instructions for installing GAP packages in Sage can be found [here](http://wiki.sagemath.org/InstallingGapPackages), and the numericalsgps package can be found [here](https://www.gap-system.org/Packages/numericalsgps.html).
- Finally, download `numerical_semigroup.py` and place it in your project directory.

The following code fragment gives an overview of how to use the `NumericalSemigroup` class from within Sage, and more complete documentation will be added in the near future.

    from numerical_semigroup import *
    McNuggets = NumericalSemigroup([6,9,20])
    print McNuggets.FrobeniusNumber()
    print McNuggets.LengthSet(400)
    print McNuggets.DeltaSet(400)
    print McNuggets.OmegaPrimality(400)
    print McNuggets.CatenaryDegree(400)
