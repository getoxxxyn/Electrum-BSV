
# Electrum-BSV - Lightweight Bitcoin SV Client

Electrum-BSV is a fast and secure Bitcoin SV (BSV) wallet designed for high performance and flexibility. It is based on ElectrumSV, which itself is a Python-based fork of the Electrum Core client, specifically built for BSV.

## :memo: License & Contributors
- **License:** MIT License
- **Maintainers:** Neil Booth, Roger Taylor, AustEcon
- **Project Lead:** Roger Taylor
- **Language:** Python (requires Python 3.9.13 or later)
- **Website:** [electrumsv.io](https://electrumsv.io)

## :rocket: Getting Started on Linux / macOS

Electrum-BSV is a lightweight Bitcoin SV client based on ElectrumSV. To get started, ensure you are using the **latest stable release branch** (`releases/1.3`) for production use. The `develop` branch may include experimental changes and features that are not guaranteed to be stable.

### :exclamation: Prerequisites
Before you begin, make sure your system meets the following requirements:

- **Python Version**: 3.9.13 or higher (Python 3.10 and 3.11 are not supported)
- **SQLite Version**: 3.31.1 or higher
- **Dependencies**: Refer to the instructions below based on your operating system.

### :wrench: Installing Dependencies

#### For macOS:
```bash
brew install pyqt5
pip3 install --user -r contrib/deterministic-build/macos-py3.9-requirements-electrumsv.txt
```

#### For Linux (Ubuntu/Debian):
```bash
sudo apt-get install python3-pyqt5
pip3 install wheel
pip3 install cython==0.29.36
pip3 install --user -r contrib/deterministic-build/linux-py3.9-requirements-electrumsv.txt
```

### :floppy_disk: Running Electrum-BSV

After installing dependencies, run Electrum-BSV with:
```bash
python3 electrum-sv
```

To install Electrum-BSV system-wide (without dependencies), use:
```bash
pip3 install . --no-dependencies
```

## :book: Troubleshooting

If you encounter issues, here are some common solutions:

### :gear: Errors with "wheels"
If you see errors related to **wheels**, ensure the `wheel` package is installed:
```bash
pip3 install --user wheel
```

### :warning: Issues with "libusb"
Install the necessary development libraries:
```bash
sudo apt-get install libusb-1.0.0-dev libudev-dev
```

### :bug: Problems with "Python.h"
If you get errors related to `Python.h`, check your Python version and install the necessary development headers:
```bash
sudo apt install python3.9-dev
```

### :camera: Enabling QR Code Scanning
For QR code scanning functionality, install `zbar-tools`:
```bash
sudo apt-get install zbar-tools
```

## :computer: Getting Started on Windows

The simplest way to run Electrum-BSV on Windows is to use the pre-built executable for the latest release from the official website. To verify the download’s integrity, compare the SHA-256 hash with the one provided in the `build-hashes.txt` file.

Alternatively, you can run it directly from the source repository for customizations or contributions.

### :floppy_disk: Installing Dependencies for Windows
First, install the required dependencies:
```bash
py -3.9 -m pip install --user -r contrib/deterministic-build/win64-py3.9-requirements-electrumsv.txt
```

To run Electrum-BSV:
```bash
py -3.9 electrum-sv
```

### :package: Installing System-Wide (Windows)
To install the package without dependencies:
```bash
pip3 install . --no-dependencies
```

## :bar_chart: Development & Contributions

Electrum-BSV is built automatically via Azure Pipelines CI services for each commit. If you want to create your own builds, you can fork the project and link it to Azure Pipelines for automatic builds.

### :memo: Running Unit Tests
To run the unit tests with `pytest`, use:
```bash
pytest electrumsv/tests
```

### :package: Running Pylint
To run **Pylint** for code quality checks:
```bash
pylint --rcfile=.pylintrc electrum-sv electrumsv
```

### :sunglasses: Running MyPy (Static Typing)
For static type checking, use **MyPy**:
```bash
mypy --config-file mypy.ini --python-version 3.9
```

## :package: Builds & Distribution

### :floppy_disk: Source Archives
To create the source archives, run:
```bash
./contrib/make_source_archives.py
```

### :apple: macOS Build Instructions
See the `contrib/osx/` directory for detailed build instructions.

### :windows: Windows Build Instructions
For Windows builds, refer to `contrib/build-wine/`.

## :star: Additional Notes

We welcome contributions to the Electrum-BSV project. If you wish to improve the software, please fork the repository and submit a pull request.

