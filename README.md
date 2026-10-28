"# The_Legend_of_Dragoon_PS5_Recomp" 
The files in this repository are just structure, you need to go to the releases to get a working image with an eboot.bin.

This is NOT emulation
An emulator like DuckStation runs the game by pretending to be a PS1 CPU. It reads the game's MIPS machine code one instruction at a time and works out what each one would have done, for the entire session.

This doesn't do that. It's built with PSXRecomp, a static recompiler:

Translate: the game's original MIPS R3000 code is read off the disc ahead of time and translated into C source code. That covers the main executable plus the modules the game loads for battles, fields, menus and the world map.
Compile: that C is compiled with Clang/LLVM straight into native x86-64 code for the PS5's Zen 2 CPU.
Ship: the result is a signed PS5 executable (eboot.bin).
So when you play, the PS5's CPU runs Dragoon's own game logic directly, as native code. No instruction-by-instruction interpreter.

Features
Vulkan on the PS5 GPU Vulkan is the modern low-level graphics API PC and Linux games use to talk directly to the graphics card. The PS5 doesn't officially support it, so this port links in RADV, Mesa's open-source Vulkan driver for AMD GPUs, as ported to the PS5 by mihawk-99. Graphics are drawn on the actual PS5 GPU, so high-res rendering runs at a locked 60 fps.

4x internal resolution, 4K output Rendered at 4x PS1 resolution and output at 3840x2160. Sharp polygons, characters and effects.

True 16:9 widescreen (not a stretch) - Battles and the world map render more of the world at the sides. - Fields and towns use pre-rendered 4:3 backgrounds, so the wider view slides within each room's art. Rooms narrower than the screen get side bars. - FMVs and menus stay 4:3 so nothing's distorted.

HD texture pack support Loads DuckStation-format texture packs. Tested with the Vierock HD Retro Dragoon pack: about 8,400 upscaled textures across all four discs, loaded in the background while you play.

Perspective-correct textures Fixes the PS1's classic texture wobble and warping.

Quality of life - Quick save and load anywhere - Disc swapping across all 4 discs - On-screen notices for saves and disc swaps - Full DualSense support, including the touchpad - Everything configured in one simple text file

Stable 50+ minute sessions at 4K with HD textures, a locked 60 fps and flat memory use.

Credits
PSXRecomp: the static recompiler and runtime
mihawk-99: the PS5 Vulkan (RADV/Mesa) port
The Mesa project: the RADV driver
Vierock HD Retro: the HD texture pack
