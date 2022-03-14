# mrc_hero_bringup

This package is a stripped down version of hero_bringup to be used in the course Mobile Robot Control (mrc) It is used to launch only the basic hardware.

# HERO mrc installation instructions

This guide assumes the robot is in working order and installed using the instructions in [hero_bringup](<https://github.com/tue-robotics/hero_bringup#re-install-hero>)

- create a new user.
`sudo adduser mrc` 
- switch to this new user. `su mrc`
- install the mrc environment
`wget https://raw.githubusercontent.com/tue-robotics/emc-env/master/install.bash` followed by
`source install.bash`
