GXX = g++
OUTPUT = program

SRC = $(wildcard *.cpp)
OBS = $(SRC:.cpp=.o)
DEP = $(SRC:.cpp = .d) 

DEP_FLAGS = -MMD
DEP_FLAGS+= -MP

all: $(OUTPUT)

program: $(OBS)
	$(GXX) $^ -o $@

$(OBS): $(SRC)
	$(GXX) -c $*.cpp -o $@
	
run: 
	./$(OUTPUT)

clean:
	rm *.o $(OUTPUT)



.PHONY: clean all run

	-include $(DEP)
