# Cmake-tools-import-errors
A minimal project to show an intelligence include error.

## Reproduction
Open the project with clang 12.0 configuration on MacOS.
## Accelerate Import error
There will be a squiggle under `#import <Accelerate/Accelerate.h>`
The error message should say: `cannot open source file "cblas.h" (dependency of "Accelerate.framework/Headers/Accelerate.h")C/C++(1696)`
## No stdlib because of precompiled header
Squiggle underneath `#include <stdlib.h>`. You can get rid of this squiggle by deactivating precompiled headers in the CMakeLists.txt (which of course is not desireable in a real project)
