## ADDRESS CRAN REMOVAL NOTE

```
Check Details
Version: 0.0.1
Check: whether package can be installed
Result: WARN 
  Found the following significant warnings:
    Warning: namespace ‘fio’ is not available and has been replaced
Flavors: r-devel-linux-x86_64-debian-clang, r-devel-linux-x86_64-debian-gcc, r-patched-linux-x86_64, r-release-linux-x86_64

Version: 0.0.1
Check: installed package size
Result: NOTE 
    installed size is  6.9Mb
    sub-directories of 1Mb or more:
      data      2.7Mb
      extdata   4.1Mb
Flavors: r-oldrel-macos-arm64, r-oldrel-macos-x86_64, r-oldrel-windows-x86_64
```

* fio moved from Suggests to Imports.
* Added `@import fio` in the datasets documentation.