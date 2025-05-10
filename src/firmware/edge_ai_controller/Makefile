# Makefile for Edge AI Controller firmware
# TODO: Define compiler, flags, source files, and build rules.

# Compiler
CC = arm-none-eabi-gcc # Example for ARM Cortex-M

# C Flags
CFLAGS = -Wall -Wextra -O2 -g # Example flags
# TODO: Add MCU-specific flags, include paths for headers, etc.

# Linker Flags
LDFLAGS = # TODO: Add linker script, library paths, etc.

# Source files
SRCS = main.c sensor_interface.c comms.c ml_inference.c
OBJS = $(SRCS:.c=.o)

# Target executable name
TARGET = edge_ai_controller.elf

.PHONY: all clean

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) $(LDFLAGS) $(OBJS) -o $@

%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(OBJS) $(TARGET) 