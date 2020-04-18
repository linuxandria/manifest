mupload.nl/index/?ref=eyrqdcs' border='0' target='_blank'><img src='https://www.mupload.nl/img/eyrqdcs.jpg' border='0'></a>




Xtended-Mutate:
====================
This is a ROM based on MSM-Xtended. We thank the founders of this project for making this possible.
Our goal is to tailor this project to the oneplus devices, with our insights to get the most out of the oneplus and to provide it with extra mods, etc.


To initialize your local repository, use this command:
-----------------------------------------------------

    repo init -u https://github.com/Xtended-Mutate/manifest.git -b xq

To sync the repository, use this command:
-----------------------------------------

    repo sync -c --force-sync --no-tags --no-clone-bundle 

For using the right trees for hotdogb (Oneplus 7T) you can add in .repo a local_manifest and put these lines into it:
---------------------------------------------------------------------------------------------------------------------

<?xml version="1.0" encoding="UTF-8"?>
<manifest>
    <remote fetch="https://github.com/Xtended-Mutate/" name="Xtended-Mutate"  />
    <remote name="gitlab" fetch="https://gitlab.com" />
    <remote fetch="https://gitlab.com/jacks84/platform_vendor_pixelgapps" name="platform_vendor_pixelgapps" />

   
   <!-- devices -->
  <project name="Xtended-Mutate/device_oneplus_hotdogb" path="device/oneplus/hotdogb" remote="github" revision="xq" />

   <!-- common repos -->
  <project name="Xtended-Mutate/device_oneplus_sm8150-common" path="device/oneplus/sm8150-common" remote="github" revision="xq" />
  <project name="Xtended-Mutate/android_device_oneplus_common" path="device/oneplus/common" remote="github" revision="xq" />


   <!--kernel -->
  <project name="Xtended-Mutate/kernel_oneplus_sm8150" path="kernel/oneplus/sm8150" remote="github" revision="xq" />

   <!-- vendors -->
  <project name="Xtended-Mutate/vendor_oneplus" path="vendor/oneplus" remote="github" revision="xq" />

  <!-- gapps included -->
  <project path="vendor/pixelgapps" name="jacks84/platform_vendor_pixelgapps" remote="gitlab" revision="ten" />
   
</manifest>



Or download the map: 

https://sourceforge.net/projects/local-manifest-mutate/files/mutate.xml/download




To Build, use following commands:
---------------------------------
    
    . build/envsetup.sh
    lunch xtended_device-userdebug
    make xtended

