# OpenwrtPackages
OpenWRT Makefiles for my projects

This isn't exactly OpenWRT standard package management, but it's quick and dirty:

From your openwrt BSP directory, navigate to your package directory:

cd package

  Make a directory for embedcreativity
  
    mkdir embedcreativity
    
  Clone this repo
  
    git clone https://github.com/embedCreativity/OpenwrtPackages.git

Now navigate back to the root BSP directory and update your OpenWRT config by doing a 'make menuconfig'.
From here, you should be able to see the new embedCreativity section and you can select packages from there.
