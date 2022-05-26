# Info

Thes recipe allows you to downalod and install 1Password latest version eg. 1Password 8

# Usage
You will need to canche DOWNLOAD_URL and supported_architectures in your munki override.

DOWNLOAD_URL for Intel based: https://downloads.1password.com/mac/1Password-latest.zip  
DOWNLOAD_URL for Apple silicon: https://downloads.1password.com/mac/1Password-latest-aarch64.zip  

supported_architectures for Intel based: x86_64  
supported_architectures for Apple silicon: arm64

Our best practice is to make 2 sepereatet munki override
Intel based:
```
autopkg make-override 1PasswordLatest.munki -n 1PasswordLatest-x86.munki
```

Apple Silicon:
```
autopkg make-override 1PasswordLatest.munki -n 1PasswordLatest-arm.munki
```
