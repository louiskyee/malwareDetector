malwareDetector
===================

[GitHub](https://github.com/louiskyee/malwareDetector.git)

Description
-----------

This is a malware detector specification for NTUST isLab.

Installation
------------

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install `malwareDetector`.

Usage
-----

### import
* import class `detector` from `malwareDetector.detector`
```python=
from malwareDetector.detector import detector
```

### Examples:
```python=
from malwareDetector.detector import detector
import numpy as np

class subDetector(detector):
    def extractFeature(self) -> list:
        return 'This is the implementation of the extractFeature function from the derived class.'

    def vectorize(self) -> np.array:
        return 'This is the implementation of the vectorize function from the derived class.'

    def model(self):
        return 'This is the implementation of the model function from the derived class.'

    def predict(self):
        return 'This is the implementation of the predict function from the derived class.'
```