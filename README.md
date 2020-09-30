## Updating

1. Find the latest released version: https://github.com/qupath/qupath/releases

2. Update version number in **libvips.nuspec**:
        
        <version>0.2.3</version>

3. Download installer and get its hash in PowerShell:

        PS> Get-FileHash -Algorithm SHA256 -Path ".\Downloads\QuPath-0.2.3-Windows.zip"
        Hash: 6F53A32E168B0DC61451DBEC9BC4577EDA52E7069372EE8EB402120D7775DD26

   Paste this hash into the "checksum" field in chocolateyinstall.ps1

4. Rebuild and install the package:
   
        choco pack
        choco upgrade qupath -dv -s .