# PrimeQA
The prime repository for Question Answering research and development.


[![Build Status](https://travis.ibm.com/ai-foundation/PrimeQA.svg?token=XcbF7zxMKHD12hqZiBwc&branch=master)](https://travis.ibm.com/ai-foundation/PrimeQA)


## Getting Started

## Installation

```shell
# cd to project root

# If you want to run on GPU make sure to install torch appropriately

# E.g. for torch 1.11 + CUDA 11.3:
pip install 'torch~=1.11.0' --extra-index-url https://download.pytorch.org/whl/cu113

# Install as editable (-e) or non-editable using pip, with extras (e.g. tests) as desired
# Example installation commands:

# Minimal install (non-editable)
pip install .

# Full install (editable)
pip install -e .[all]
```

Please note that dependencies (specified in [setup.py](./setup.py)) are pinned to provide a stable experience.
When installing from source these can be modified, however this is not officially supported.

## JAVA requirements
Java 11 is required for BM25 retrieval. 

Download Java 11 package from https://jdk.java.net/archive/ and uncompress

Set JAVA_HOME:
```shell
export JAVA_HOME=<jdk-dir>
export PATH=$JAVA_HOME/bin:$PATH
```

## Unit Tests

To run the unit tests you first need to [install PrimeQA](#Installation).
Make sure to install with the `[tests]` or `[all]` extras from pip.

From there you can run the tests via pytest, for example:
```shell
pytest --cov PrimeQA --cov-config .coveragerc tests/
```

For more information, see:
- Our [tox.ini](./tox.ini)
- The [pytest](https://docs.pytest.org) and [tox](https://tox.wiki/en/latest/) documentation

