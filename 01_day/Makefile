helloos.o: helloos.asm
	nasm -o helloos.o helloos.asm

build: helloos.o
	dd if=helloos.o of=boot.img

clean:
	rm -rf ./helloos.o
	rm -rf ./boot.img

run:
	qemu-system-x86_64 -fda boot.img -boot a
