## Updating

1. Find the latest released version: https://github.com/qupath/qupath/releases

2. Update version number in **libvips.nuspec**:
        
        <version>0.2.1</version>

3. Rebuild and install the package:
   
        choco pack
        choco upgrade qupath -dv -s .