# compiling/installing virtual display driver (itsmikethetech/Virtual-Display-Driver)

1. install visual studio 2022
2. install [Windows SDK 10.0.26100.1](https://learn.microsoft.com/en-us/windows-hardware/drivers/download-the-wdk#download-icon-for-sdk-step-2-install-sdk)
3. install [WindowsUserModeDriver10.0](https://learn.microsoft.com/en-us/windows-hardware/drivers/download-the-wdk#download-icon-for-wdk-step-3-install-wdk)
4. download master branch from [itsmikethetech/Virtual-Display-Driver](https://github.com/itsmikethetech/Virtual-Display-Driver)
5. open solution in `Virtual Display Driver (Non-HDR)`
6. might require you to download some dependencies
7. click Project => Properties => C/C++ => Code Generation => Spectre Mitigation => Disable
8. set build to release
9. build solution
10. copy folder `Virtual Display Driver (Non-HDR)\x64\Release\IddSampleDriver` to `c:\`
11. copy file `Virtual Display Driver (Non-HDR)\x64\Release\IddSampleDriver.cer` to `c:\IddSampleDriver`
12. edit `options.txt`, add entry for resolutions/mhz eg `2560, 1440, 60`
13. copy provided `installCert.bat` to `c:\IddSampleDriver` and run as administrator
14. go `device manager` => `display adapters` => `action` (from top menu) => `add legacy hardware` => `install hardware` => `display adapters` => `have disk` => `c:\IddSampleDriver`
