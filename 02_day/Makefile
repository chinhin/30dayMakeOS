
ipl.bin: ipl.asm Makefile
	nasm -o ipl.bin ipl.asm

build: ipl.bin Makefile
	cp ../bootimg/boot.img helloos.img
	dd if=ipl.bin of=helloos.img conv=notrunc

clean:
	rm -rf ./ipl.bin
	rm -rf ./helloos.img

run:
	qemu-system-x86_64 -fda helloos.img -boot a
