malwareDetector
===============

* Source code: https://github.com/louiskyee/malwareDetector.git
* Wiki: https://github.com/louiskyee/malwareDetector/wiki
* PyPI: https://pypi.org/project/malwareDetector/

Description
-----------

This is a malware detector specification for NTUST isLab.
The `malwareDetector` is a base class designed for malicious software detection. It enables straightforward utilization of Python's inheritance feature. By inheriting from `malwareDetector` and implementing the required functions, you can achieve your specific goals. Additionally, it offers convenient configuration management. For more detailed instructions, please refer to the [GitHub Wiki](https://github.com/louiskyee/malwareDetector/wiki).

Requirements
------------
Tool | Version |Source |
|---|---|---|
| Python | `>= 3.10` | https://www.python.org/downloads |

Installation
------------

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install `malwareDetector`.
* Example: `pip install malwareDetector`

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
from typing import Any
import numpy as np

class subDetector(detector):
    def __init__(self) -> None:
        super().__init__()

    def extractFeature(self) -> Any:
        return 'This is the implementation of the extractFeature function from the derived class.'

    def vectorize(self) -> np.array:
        return 'This is the implementation of the vectorize function from the derived class.'

    def model(self) -> Any:
        return 'This is the implementation of the model function from the derived class.'

    def predict(self) -> np.array:
        return 'This is the implementation of the predict function from the derived class.'
```