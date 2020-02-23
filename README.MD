## Fix External Monitor Color Problem with MacBookPro
Based on https://embdev.net/topic/284710#3027030
# Instructions
```
-   Download patch.rb and run ./patch.rb 

-   Take a look at the generated file and remember its path (mine was ~/Desktop/DisplayVendorID-10ac/DisplayProductID-4080 ).

-   Reboot into recovery mode (⌘-R at boot).

-   Mount your main disk (enter Disk Utility, select the gray Macintosh HD, click Mount, provide your password, close Disk Utility).

-   Open up a terminal (Utilities -> Terminal), backup the overrides directory, copy in your new override file, and reboot:

```
````
$ cd /Volumes/Macintosh\ HD/System/Library/Displays/Contents/Resources
$ cp -R Overrides Overrides.bak
$ cp -R /Volumes/Macintosh\ HD/Users/jrr/Desktop/DisplayVendorID-10ac Overrides/
$ reboot
````

