# malwareDetector

* Source code: https://github.com/louiskyee/malwareDetector.git
* Wiki: https://github.com/louiskyee/malwareDetector/wiki
* PyPI: https://pypi.org/project/malwareDetector/

## Description

This is a malware detector specification for NTUST isLab.
The `malwareDetector` is a base class designed for malicious software detection. It enables straightforward utilization of Python's inheritance feature. By inheriting from `malwareDetector` and implementing the required functions, you can achieve your specific goals. Additionally, it offers convenient configuration management. For more detailed instructions, please refer to the [GitHub Wiki](https://github.com/louiskyee/malwareDetector/wiki).

## Requirements

Tool | Version | Source
-----|---------|-------
Python | `>= 3.10` | https://www.python.org/downloads

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install `malwareDetector`.
* Example: `pip install malwareDetector`

## Usage

### Import
* Import class `detector` from `malwareDetector.detector`
    ```python
    from malwareDetector.detector import detector
    ```

### Example:
```python
import numpy as np
from typing import Any
from malwareDetector.detector import detector

class subDetector(detector):
    def __init__(self, config_path=None) -> None:
        super().__init__(config_path)

    def extractFeature(self) -> Any:
        return 'This is the implementation of the extractFeature function from the derived class.'

    def vectorize(self) -> np.array:
        return 'This is the implementation of the vectorize function from the derived class.'

    def model(self, training: bool = True) -> Any:
        return 'This is the implementation of the model function from the derived class.'

    def predict(self) -> np.array:
        return 'This is the implementation of the predict function from the derived class.'
```

## Configuration

The `malwareDetector` uses a configuration system that can be customized through a JSON file or command-line arguments. The default configuration file is `config.json` in the current directory, but you can specify a custom path when initializing the detector.

### Key Configuration Classes:

- `Config`: Stores all external settings for the detector.
- `PathConfig`: Manages input and output file paths.
- `FolderConfig`: Handles folder configurations for data storage.
- `ModelConfig`: Stores model-specific parameters and hyperparameters.

For detailed information on configuration options and usage, please refer to the [GitHub Wiki](https://github.com/louiskyee/malwareDetector/wiki).