# Emscripten

## Build

```
mkdir build
cd build
emcmake cmake ..
emmake make
```

## Link

```
em++ -O3 -flto -fno-rtti -fno-exceptions *.o -o index.html -sUSE_SDL=2 -sASYNCIFY -sASYNCIFY_IGNORE_INDIRECT -sASYNCIFY_ONLY=@../../../funcs.txt -sENVIRONMENT=web -sINITIAL_MEMORY=192mb --preload-file Setup.dat --preload-file Rock_hod.lvl --preload-file Rock_hod.mst --preload-file Rock_hod.sss --preload-file hod_demo.paf --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate']
```
