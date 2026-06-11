all: mouse.bin

	md5sum --ignore-missing --check md5sums.txt

mouse.o: mouse.s
	ca65 --target apple2 -l "$@.list" -o "$@" "$<"

mouse.bin: mouse.o
	ld65 --config apple2-asm.cfg -o "$@" "$<"

clean:
	rm -f *.bin *.o
