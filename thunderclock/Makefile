all: thunderclock.bin

	md5sum --ignore-missing --check md5sums.txt

thunderclock.o: thunderclock.s
	ca65 --target apple2 -l "$@.list" -o "$@" "$<"

thunderclock.bin: thunderclock.o
	ld65 --config apple2-asm.cfg -o "$@" "$<"

clean:
	rm -f *.bin *.o
