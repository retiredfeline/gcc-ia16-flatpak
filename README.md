# Flatpak configurations to build gcc-ia16

Each subdirectory contains the manifest, patches and other material to build a flatpak for the [gcc-ia16 GNU C compiler for the 16-bit x86 architecture](https://github.com/tkchia/gcc-ia16).

## Example

After installation, compile the standard hello world program to a DOS COM executable:

	flatpak run io.github.gcc_ia16.Gcc_ia16 ia16-elf-gcc -o hello.com hello.c
	dosbox hello.com

See the generated assembler:

	flatpak run io.github.gcc_ia16.Gcc_ia16 ia16-elf-gcc -S -O hello.c
	# assembler output is in hello.s

Shell scripts or aliases will help reduce typing.

## Notes

Remember that a flatpak runs in a sandbox and file access is allowed to only parts of the filesystem. Files under /home should work fine.

The license of this code is [GPL3](gplv3.md).
