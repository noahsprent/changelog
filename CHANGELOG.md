# Changelog

## [1.1.0] - 2022-06-14
Our GFP part has now been used over 1000 times! There are 1002 publicly-viewable experiments online that link back to the URI for GFP in our package. Thanks to this, we can now confirm that the Coefficient of Variation for MEFL when the part is used to-spec is <2%! 🎉 Check out our [blog post]() explaining how we automate this.

### Added

- Following lots of work over the last few months, all the proteins in this package are now specced as stable up to 55C! Thanks to User 1 for predicting mutations that enhance thermostability and User 2 for testing all of the proteins in vivo.
- We’re now using the BioRegression system for testing any changes that we make to the parts in this package. Every time a change is made, BioCloudLabs Inc. will synthesize, express, and test the new part against the specifications of the package to ensure they still hold.
- We used the mutations outlined in Example et al. (2022) to increase the brightness of the RFP by approximately 40%

### Deprecated
- In response to the recent paper outlining the off-target cutting of the restriction enzyme we're using for some parts, we will no longer be supporting the use of this enzyme when assembling our parts.

### Fixed

- Changed bases 103-107 in the RBS used in Device 30 to avoid BsaI-HFv2 cut site (Addressing Issue #105 - Part not compatible with MoClo Assembly)
- The sequence for RFP in *Pichia pastoris* had been codon-optimised for *Saccharomyces cerevisiae* (Issue #68), and has now been replaced with a sequence that is properly optimised, reducing burden on the host cell by ~10%

### Security
- We have added the BioSecure script to our regression testing, which will look for potentially nefarious sequences
