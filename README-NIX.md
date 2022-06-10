# Building Zephyr™ Mechanical Keyboard (ZMK) Firmware with Nix

This extension is added by Chris Andreae for MoErgo.

Nix makes setup significantly easier. With this approach West is not needed. You can however still choose to use the ZMK's sanctioned West if you wish.

# To build a target 
In ZMK root directory,

    nix-build -A *target*
	
An example is 
    nix-build -A glove80_left
	

# Adding new targets
Edit default.nix and add an target based on zmk

An example is:

    glove80_left = zmk.override {
        board = "glove80_lh";
     };