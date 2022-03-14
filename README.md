# mrc_hero_bringup

This package is a stripped down version of hero_bringup to be used in the course Mobile Robot Control (mrc) It is used to launch only the basic hardware.

# HERO mrc installation instructions

This guide assumes the robot is in working order and installed using the instructions in [hero_bringup](<https://github.com/tue-robotics/hero_bringup#re-install-hero>)

- create a new user.
`sudo adduser mrc` 
- Add this user to the sudoers file (! Take care to remove it later)
  `sudo usermod -aG sudo mrc`
- switch to this new user. `su mrc`
- add an environment variable to .bashrc
  `echo -e "\n# This is the actual robot\nexport ROBOT_REAL=true" >> ~/.bashrc`
- install the mrc environment
`wget https://raw.githubusercontent.com/tue-robotics/emc-env/master/install.bash` followed by
`source install.bash`
- test the installation by running `hero-start`
- remove root priviliges from the mrc user `sudo deluser mrc sudo`
- reboot

Note: since the mrc user does not have root priviliges, it cannot do an update of the emc-system anymore. If such an update is required one should add the user to the sudoers file, perform the update and remove the user again.
