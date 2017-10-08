CXXFLAGS := -Wall -Werror -Wno-unused-function -fPIC -fno-rtti -I/usr/include/x86_64-linux-gnu/qt5 -I.
CPPFILES := qt_binding.cpp
OBJFILES := $(CPPFILES:.cpp=.o)

CC ?= g++
AR ?= ar
RM ?= rm

all: binding.a

clean:
	$(RM) -f $(OBJFILES)
	$(RM) -f binding.a

binding.a: $(OBJFILES)
	$(AR) rcs $@ $^

%.o: %.cpp
	$(CC) -c -o $@ $< $(CXXFLAGS)

.PHONY: clean
