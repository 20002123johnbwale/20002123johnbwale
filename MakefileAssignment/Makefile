# Makefile for MakefileAssignment

# Compiler
CC = gcc

# Compiler flags
CFLAGS = -Wall

# Directories
SRC_DIR = src
BIN_DIR = bin

# Files
SRC_FILES = $(wildcard $(SRC_DIR)/*.c)
OBJ_FILES = $(patsubst $(SRC_DIR)/%.c, $(BIN_DIR)/%.o, $(SRC_FILES))
EXECUTABLE = $(BIN_DIR)/myprogram

# Rules
all: $(EXECUTABLE)

$(EXECUTABLE): $(OBJ_FILES)
	$(CC) $(CFLAGS) -o $@ $^

$(BIN_DIR)/%.o: $(SRC_DIR)/%.c
	$(CC) $(CFLAGS) -c -o $@ $<

clean:
	rm -f $(BIN_DIR)/*.o $(EXECUTABLE)
