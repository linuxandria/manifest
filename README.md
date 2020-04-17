


Xtended-Mutant:
====================
This is a ROM based on MSM-Xtended. We thank the founders of this project for making this possible.
Our goal is to tailor this project to the oneplus devices, with our insights to get the most out of the oneplus and to provide it with extra mods, etc.


To initialize your local repository, use this command:
-----------------------------------------------------

    repo init -u https://github.com/Xtended-Mutate/manifest.git -b xq

To sync the repository, use this command:
-----------------------------------------

    repo sync -c --force-sync --no-tags --no-clone-bundle 

To Build, use following commands:
---------------------------------
    
    . build/envsetup.sh
    lunch xtended_device-userdebug
    make xtended

