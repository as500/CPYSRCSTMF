# cpysrcstmf

Tool to convert source members to streamfiles.

### Installation

1. `git clone` this repository
2. Run `gmake` (available from yum)

### Usage instructions

1. `ADDLIBLE cpysrcstmf` (or whatever library you built into)
2. `cpysrcstmf` has three parameters.
   1. `LIBRARY` is the library with the source members
   2. `SOURCEPF` is the source physical file with the source members
   3. `OUTDIR` is the directory files will be created in. Parameter must not end with a `/` (forward slash). For example, **`/mydir` is valid** but `/mydir/` is not.

A new directory will be created in your specified output directory with the name of the source physical file, which will then contain the copied source members.

### Examples

```
cpysrcstmf LIBRARY(TESTPROJ) SOURCEPF(QRPGLESRC) OUTDIR('/mydir')
cpysrcstmf LIBRARY(DEVLIB) SOURCEPF(QRPGLESRC) OUTDIR('/myrepo')
cpysrcstmf LIBRARY(TESTPROJ) SOURCEPF(QRPGLESRC) OUTDIR('/myrepo')
```
