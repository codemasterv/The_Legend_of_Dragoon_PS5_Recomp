The Legend of Dragoon (PSXRecomp) - PS5 native title PPSA77067
============================================================
Unofficial PS5 build of a PSXRecomp static recompilation.

INSTALL
  1. Copy this PPSA folder to /data/homebrew/ (FTP) and let
     ShadowMountPlus register it.
  2. Copy your disc image(s) to /data/lod/disc/ and rename them:
        disc1.bin   (Disc 1; single-track .bin)
        disc2.bin   (Disc 2; single-track .bin)
        disc3.bin   (Disc 3; single-track .bin)
        disc4.bin   (Disc 4; single-track .bin)
     The .cue files and game.toml are written there on the first launch;
     you only supply the .bin files. (Multi-track dump? Put your own .cue
     there as discN.cue with FILE "discN.bin" instead.)
  3. Launch "The Legend of Dragoon" from the home screen.

CONTROLS (DualSense)
  PS1 controller: Cross/Circle/Square/Triangle, L1/R1/L2/R2, D-pad,
  Options = Start. Left stick = D-pad in digital games, sticks in
  analog games. Select = touchpad click + Options (the PS5 keeps
  the Create button for itself).
  Touchpad click + L1 / R1   previous / next disc
  Touchpad click + Square    save state
  Touchpad click + Triangle  load state
  Touchpad click + L3        FPS readout on/off
  Widescreen: set widescreen = on in ps5_controls.ini (restart the game).
  16:9 where this game supports it; other scenes, FMVs and menus stay 4:3.
  (the shortcut button can be changed: shortcut_button in ps5_controls.ini)
  Settings: /data/lod/ps5_controls.ini

FILES IN /data/lod
  game.toml      game configuration (delete it to get the default back)
  disc/          disc .cue (auto) + your .bin files
  saves/         memory cards and save states
  psx_ps5.log    log of the last run - send this with any bug report
