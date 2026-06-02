# belieffit

`belieffit` is a Stata command for estimating posterior mean log beliefs and correcting parametrically for bias from posterior variance using fixed-point iteration.

## Installation

Install the package directly from GitHub with:

```stata
net install belieffit, from("https://raw.githubusercontent.com/martin-andresen/belieffit/main") replace
```

The command depends on the user-written packages `reghdfe` and `ppmlhdfe`. Install these first if they are not already available:

```stata
ssc install reghdfe, replace
ssc install ppmlhdfe, replace
```

After installation, open the help file in Stata with:

```stata
help belieffit
```

## Basic usage

```stata
belieffit logbelief, absorb(person job) reps(500) vce(person job)
belieffit logbelief, absorb(person job) reps(500) vce(person job) aux(name(mean) regress {mean} gender {W})
```

See the Stata help file for full syntax and options:

```stata
help belieffit
```

## Citation

If you use `belieffit`, please cite:

Martin Eckhoff Andresen, Manudeep Bhuller, and Alfred Løvgren. [*Pay Beliefs and the Amenity-Pay Tradeoff*](https://arxiv.org/pdf/2606.02503).

## License

This project is licensed under the MIT License. See `LICENSE` for details.
