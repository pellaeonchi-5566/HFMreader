# Third-party notices and runtime provenance

This candidate uses **Astral python-build-standalone 20261013, CPython 3.12.15, Windows x86_64 MSVC PGO**. The complete upstream archive was downloaded from its official GitHub Release and its SHA-256 matched the published digest:

`7780bf6a29f93e6d0e3b5bdbe8cf799b3e2a0638bdec921be5b0c3ca81e67313`

[Upstream release](https://github.com/astral-sh/python-build-standalone/releases/tag/20261013). Exact shipped native-file hashes and their paths within that archive are in RUNTIME_PROVENANCE.json. Application packaging uses PyInstaller 6.22.1. Build tools, Python source files, research documents and unused upstream build objects are not shipped.

| Component actually used | Version / origin | Included notice |
| --- | --- | --- |
| CPython and standard library | 3.12.15, official Astral archive | licenses-runtime/LICENSE.cpython.txt; Python-Windows-LICENSE.txt; Python-additional-notices.rst |
| Tcl/Tk | 8.6.15, archive runtime; upstream CPython binary-deps revision c807be2b19bafc06767b2ed8afec4d5f9a9553b2 | LICENSE.tcl.txt and Tk-LICENSE.txt |
| OpenSSL | 3.5.9, queried from runtime | LICENSE.openssl-3.txt (Apache-2.0) |
| Expat | 2.8.5, queried from pyexpat; vendored CPython dependency | LICENSE.expat.txt (MIT) |
| libffi | 3.4.2, Windows build pins CPython source-deps 16fad4855b3d8c03b5910e405ff3a04395b39a98 | LICENSE.libffi.txt (MIT) |
| liblzma / XZ | 5.8.4, Windows build's pinned XZ source | LICENSE.liblzma.txt (0BSD) |
| zlib | 1.3.2 in Python; 1.3.1 in Tcl/Tk zlib1.dll (both queried) | LICENSE.zlib.txt (Zlib) |
| libmpdec | 2.5.1, queried from decimal; vendored CPython dependency | LICENSE.mpdecimal.txt and Python-additional-notices.rst |
| bzip2 | 1.0.8, Windows build source | LICENSE.bzip2.txt |
| Microsoft VC runtime | VCRUNTIME140.dll and VCRUNTIME140_1.dll from the same verified archive | Python-Windows-LICENSE.txt and FREE_USE_TERMS.md |
| PyInstaller | 6.22.1 bootloader and runtime hooks | PyInstaller-COPYING.txt (GPL with bundled-application distribution exception) |

Unless expanded above, notice filenames are under licenses-runtime/. Tix, SQLite, pip and unrelated tool-runtime DLLs are not included. Windows 10/11 supplies the system UCRT; **ucrtbase.dll and API-set shims are not redistributed in this ZIP**. No Microsoft system DLL was copied out of an unrelated application directory.

The manifest's generic OpenSSL linkage labels are not used as filenames for this audit: the shipped libcrypto-3-x64.dll/libssl-3-x64.dll and their hashes are checked directly. Likewise, the generic dependency download list is not substituted for Windows' pinned libffi source or CPython's vendored Expat/libmpdec versions.

All third-party components retain their own copyrights, license grants and warranty disclaimers. HFMreader's resale restrictions do not override those independent rights. The original waveform icon and connection drawing were created for HFMreader. The screenshot shows the application's own simulated session. The rc3 Windows ZIP includes no HFMscan Hfm.dat, HHT executable, seller photograph or third-party research document. The repository hardware guide separately includes two original product reference photos supplied by Pellaeon Chi. These are not claimed as original HFMreader artwork or covered by its original-material copyright notice.

Original HFMreader material: Copyright (c) 2026 Pellaeon Chi. This attribution does not replace any third-party copyright or license notice.
