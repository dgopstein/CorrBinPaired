# clust.bin.pair

Statistical tools for analyzing clustered binary matched-pair data in R.

### Clustered Binary Matched-Pair

The tests and tools included in this package work primarily on clustered binary matched-pair data. In order for data to be a good fit for analysis with these tools it needs to have the following three properties:

- **Clustered** (aka *correlated*, *non-independent*): Multiple samples drawn from the same distribution. 
  - e.g. Measurements of multiple teeth from each of several dental patients. The teeth of one patient are more likely to be similar than the teeth of different patients.
- **Binary** (aka *dichotomous*): Results that can have only two discrete values.
  - e.g. Values like true/false, yes/no, success/failure, missing/present, etc.
- **Matched-pair**: Data points that come in pairs. Often from successive trials in a repeated measures experiment or from measuring two different, but related, sources.
  - e.g. Eyes measured before and after surgery or the opinions of a doctor and her patient on the patient's progress.

### Tests
This package contains 5 statistical tests suitable for analyzing clustered binary matched-pair data in various contexts. Four of the tests are designed specifically for this type of data. The fifth test, McNemar's test is the conceptual predecessor to each of the other tests, and is included for comparison. In practice, McNemar's test is specifically noted to be unsuitable for clustered data. The tests are listed below, along with the articles which introduce them:

- **McNemar**:
[McNemar, Quinn. 1947. "Note on the sampling error of the difference between correlated proportions or percentages." *Psychometrika*.](https://dx.doi.org/10.1007/BF02295996)
- **Eliasziw**:
[Eliasziw, Michael, and Allan Donner. 1991. "Application of the McNemar test to non‐independent matched pair data." *Statistics in medicine*.](https://dx.doi.org/10.1002/sim.4780101211)
- **Obuchowski**:
[Obuchowski, Nancy A. 1998. "On the comparison of correlated proportions for clustered data." *Statistics in medicine*.](https://dx.doi.org/10.1002/(SICI)1097-0258(19980715)17:13%3C1495::AID-SIM863%3E3.0.CO;2-I)
- **Durkalski**:
[Durkalski, Valerie L., Yuko Y. Palesch, Stuart R. Lipsitz, and Philip F. Rust. 2003. "Analysis of clustered matched‐pair data." *Statistics in medicine*.](https://dx.doi.org/10.1002/sim.1438)
- **Yang**:
[Yang, Zhao, Xuezheng Sun, and James W. Hardin. 2010. "A note on the tests for clustered matched‐pair binary data." *Biometrical journal*.](https://dx.doi.org/10.1002/bimj.201000035)

### Datasets

Included is sample data from real world experiments of the form that can benefit from the application of these tests:

- **Obfuscation**: Programmers were asked to hand-evaluate pairs of obfuscated and deobfuscated snippets of C source code. The data is tested to see whether or not programmers trace deobfuscated code any differently than obfuscated code.
- **Psychiatry**: Psychiatrists and their patients were asked to evaluate the applicability of various concerns and treatments to the patient. The data is tested to see how well patient and doctor perception aligns.
- **Thyroids**: Hyperparathyroidism patients were scanned using both PET and SPECT tests. The data is tested to evaluate the sensitivity and specificity of the two tomogoraphy tests.

## Documentation

Description of functions as well as usage examples are available in the [reference manual](https://cran.r-project.org/package=clust.bin.pair/clust.bin.pair.pdf).

## Installation and Use

You can install the latest release from CRAN:

    install.packages("clust.bin.pair")

To use, load as follows:

    library(clust.bin.pair)
