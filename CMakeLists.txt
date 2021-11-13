cmake_minimum_required(VERSION 3.12)
project(WOLF3DEXTRACT)

file(GLOB WOLF3DEXTRACT_SRC
"./Source/wolf3dextract.c"
"./Source/globals.c"
"./Source/audio_extract/*.c"
"./Source/compression/*.c"
"./Source/map_extract/*.c"
"./Source/palette/*.c"
"./Source/pic_extract/*.c"
"./Source/sprite_extract/*.c")

add_executable(wolf3dextract)
set_property(TARGET wolf3dextract PROPERTY C_STANDARD 99)
target_sources(wolf3dextract PRIVATE ${WOLF3DEXTRACT_SRC})


add_executable(snd2wav)
set_property(TARGET snd2wav PROPERTY C_STANDARD 99)
target_sources(snd2wav PRIVATE "./Source/snd2wav.c")

add_executable(snd2wlf)
set_property(TARGET snd2wlf PROPERTY C_STANDARD 99)
target_sources(snd2wlf PRIVATE "./Source/snd2wlf.c")

add_executable(vga2ppm)
set_property(TARGET vga2ppm PROPERTY C_STANDARD 99)
target_sources(vga2ppm PRIVATE "./Source/vga2ppm.c")