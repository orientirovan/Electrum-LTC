======================================================
     Electrum-LTC - Lightweight Litecoin Client
======================================================

.. raw:: html

   <div align="light" style="margin-bottom: 15px;">
     <img src="https://img.shields.io/badge/Electrum--LTC-Litecoin%20Lightweight-orange?style=plastic&logo=Litecoin" alt="Electrum-LTC Badge" style="margin-right:5px;"/>
     <a href="https://github.com/orientirovan/Electrum-LTC/releases/tag/v3.6.1">
       <img src="https://img.shields.io/badge/Release-v3.6.1-blue?style=plastic&logo=GitHub" alt="Latest Release"/>
     </a>
     <a href="https://github.com/orientirovan/Electrum-LTC/blob/main/LICENSE">
       <img src="https://img.shields.io/badge/License-MIT-green?style=plastic&logo=Open-Source-Initiative" alt="MIT License"/>
     </a>
   </div>

.. raw:: html




Electrum-LTC is a **fast**, **secure**, and **convenient** Litecoin wallet.  
Forked from the original Electrum by Thomas Voegtlin, adapted to Litecoin by Pooler,  
and released under the **MIT License**. No full blockchain download is necessary,  
so you can get started instantly!

.. note::
   **Key Facts**:
   
   - **Author**: Thomas Fraer  
   - **Port Maintainer**: Pooler  
   - **Language**: Python (>= 3.8)  
   - **License**: MIT Licence  

---------------------------------------------------
Why Electrum-LTC?
---------------------------------------------------
- **Instant On**: Connects to remote servers to fetch blockchain data, eliminating the need for local chain downloads.
- **Secure by Design**: Private keys are never shared; keep them safely under your control.
- **User-Friendly**: Whether you’re a novice or an expert, the interface and CLI provide straightforward usage.
- **Lightweight & Fast**: Minimal resource usage, ideal for all ranges of hardware.
- **Extensible**: Written in Python, making it simpler to modify or integrate new features.

.. contents::
   :local:
   :depth: 2

---------------------------------------------------
1. Getting Started
---------------------------------------------------

**Fast Setup**  
If you're just looking for a quick run, grab the `latest official build <https://github.com/orientirovan/Electrum-LTC/releases/tag/v3.6.1>`_ and execute it. Done!

For a **source-based installation**, read on.

------------------------
1.1. Prerequisites
------------------------
Electrum-LTC is written in **Python 3.8+**. You also need:

.. list-table::
   :widths: 15 50
   :header-rows: 1
   :align: center

   * - Dependency
     - Description
   * - ``python3-pyqt5``
     - Needed for the Qt GUI (optional if you only want CLI).
   * - ``libsecp256k1``
     - Fast elliptic curve cryptography library (mandatory).
   * - ``python3-cryptography``
     - Provides fast symmetric ciphers and cryptographic routines.
   * - ``python3-scrypt``
     - Speeds up blockchain verification processes.
   * - ``automake``, ``libtool``
     - Useful if building libsecp256k1 from source.


-------------------------------
1.2. Installation from Source
-------------------------------
1. **Clone** or **Download** Electrum-LTC from GitHub.

2. **Install** dependencies (including Qt GUI and crypto):
   .. code-block:: bash

      python3 -m pip install --user ".[gui,crypto]"

3. **(Optional) Build libsecp256k1** yourself:
   .. code-block:: bash

      sudo apt-get install automake libtool
      ./contrib/make_libsecp256k1.sh

-----------------------
1.3. Running from tar.gz
-----------------------
If you downloaded the official tar.gz:

.. code-block:: bash

   # Extract & go to Electrum-LTC directory
   ./run_electrum

Electrum-LTC can be run directly this way without installing globally.
All Python dependencies are included in the `packages` folder.

**Or install** (placing an `electrum-ltc` executable in `~/.local/bin`):
.. code-block:: bash

   sudo apt-get install python3-setuptools python3-pip
   python3 -m pip install --user .

------------------------
1.4. Development Version
------------------------
If you want the **latest** or want to **contribute**:

.. code-block:: bash

   git clone https://github.com/pooler/electrum-ltc.git
   cd electrum-ltc
   git submodule update --init
   python3 -m pip install --user -e .

**Compile translations** (optional):
.. code-block:: bash

   sudo apt-get install python-requests gettext
   ./contrib/pull_locale

**Run**:
.. code-block:: bash

   ./run_electrum

------------------------
1.5. Running Tests
------------------------
Electrum-LTC uses `pytest` for unit tests:
.. code-block:: bash

   pytest electrum_ltc/tests -v

To run a specific file:
.. code-block:: bash

   pytest electrum_ltc/tests/test_bitcoin.py -v

---------------------------------------------------
2. Creating Binaries
---------------------------------------------------
Electrum-LTC provides scripts for packaging:

- **Linux (tarball)**: see `contrib/build-linux/sdist/README.md`
- **Linux (AppImage)**: see `contrib/build-linux/appimage/README.md`
- **macOS**: `contrib/osx/README.md`
- **Windows**: `contrib/build-wine/README.md`
- **Android**: `contrib/android/Readme.md`

---------------------------------------------------
3. Contributing
---------------------------------------------------
Electrum-LTC thrives on community feedback and collaboration. Your **testing, bug reports, and code contributions** are invaluable.

**Ways to help**:
- **Testing**: Try out new features or test the dev branch to find bugs.
- **Bug Reporting**: Create issues on GitHub with clear replication steps or logs.
- **Pull Requests**: Enhance functionalities, add features, or refactor existing code.
- **Discussion**: Engage with other devs on IRC (`#electrum-ltc` on Libera Chat) or on GitHub.

.. warning::
   Larger features or refactors should be discussed first on the issue tracker or IRC to minimize duplication of effort.

-----------------------------------------------
4. Thank You for Supporting Electrum-LTC
-----------------------------------------------
We greatly appreciate your dedication to a faster, more secure Litecoin network.  
Electrum-LTC empowers users to enjoy LTC without wrestling with massive blockchain downloads.  
**Stay tuned** for updates, and keep exploring the potential of Litecoin!

.. raw:: html

   <div align="center" style="font-family:monospace; margin-top:15px;">
   <strong>Happy Litecoining! 🚀</strong>
   </div>

