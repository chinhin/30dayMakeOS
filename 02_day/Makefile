
ipl.bin: ipl.asm Makefile
	nasm -o ipl.bin ipl.asm

build: ipl.bin Makefile
	dd if=ipl.bin of=helloos.img

clean:
	rm -rf ./ipl.bin
	rm -rf ./helloos.img

run:
	qemu-system-x86_64 -fda helloos.img -boot a
