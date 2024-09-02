# How to build flatpak

This assumes you have the flatpak tools installed already and the required version of freedesktop.Platform and freedesktop.Sdk specified in the manifest. Copy the manifest and patch files in this directory to a suitable build location and run:

	flatpak-builder build-dir io.github.gcc_ia16.Gcc_ia16.20240218_2208.json

build-dir can be replaced by any other name, but it's the name that is used for examples in the flatpak documentation so might as well use it. On subsequent builds you will need to delete build-dir or use the --force-clean option.

After a lot of downloading and compiling the result will be in build-dir. You can test it by:

	flatpak-builder --run build-dir io.github.gcc_ia16.Gcc_ia16.20240218_2208.json ia16-elf-gcc --help

Finishing the flatpak and exporting it is outside the scope of this short document. Please consult the flatpak documentation.
