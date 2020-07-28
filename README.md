## Updating

1. Find the latest released version: https://github.com/qupath/qupath/releases

2. Update version number in **libvips.nuspec**:
        
        <version>0.2.2</version>

3. Download installer and get its hash in PowerShell:

        PS> Get-FileHash -Algorithm SHA256 -Path ".\Downloads\QuPath-0.2.2-Windows.zip"
        Hash: 668DBDF6840833B3D8C6577FDAF7C2E3759DC27DABF37D19741E56ECFD925DCA

   Paste this hash into the "checksum" field in chocolateyinstall.ps1

4. Rebuild and install the package:
   
        choco pack
        choco upgrade qupath -dv -s .