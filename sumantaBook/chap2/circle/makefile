CC=g++
INCLUDE=-I../../../glad/include
CFLAGS=-c -Wall -std=c++11 $(INCLUDE) 
LDFLAGS=-L../../../glfw3/glfw/build/src -lglfw3 -lGL -lGLX -ldl -lpthread -lglut -lGLEW
CSOURCES=../../../glad/src/glad.c
CPPSOURCES=circle.cpp
OBJECTS=$(CPPSOURCES:.cpp=.o) $(CSOURCES:.c=.o)
EXECUTABLE=circle

all: $(CSOURCES) $(CPPSOURCES) $(EXECUTABLE)
    
$(EXECUTABLE): $(OBJECTS) 
	$(CC) $(OBJECTS) $(LDFLAGS) -o $@

.cpp.o:
	$(CC) $(CFLAGS) $< -o $@
clean:
	rm -rf *.o ${EXECUTABLE}	
