CC = riscv64-unknown-elf-gcc
OBJCOPY = riscv64-unknown-elf-objcopy

CFLAGS = -nostdlib -O0 -march=rv64g
OBJCOPYFLAGS = -O binary

all: test.bin

test.bin: test.elf
	$(OBJCOPY) $(OBJCOPYFLAGS) $< $@

test.elf: test.S
	$(CC) $< -o $@ $(CFLAGS)

clean:
	-@rm test.elf test.bin

.PHONY: all clean