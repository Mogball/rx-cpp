# Rx library
# OPT=-g
OPT=-O2

CFLAGS=-std=c99 -c $(OPT) -Wall
CXXFLAGS=-std=c++0x -c $(OPT) -Wall
LUA_STR=lua-str.o
ifdef NO_POSIX
  CXXFLAGS+=-DNO_POSIX
endif
ifdef NO_LUA
  LUA_STR=
  CXXFLAGS+=-DNO_LUA
endif

librx.a: rx.o $(LUA_STR)
	ar rcu librx.a rx.o $(LUA_STR) && ranlib librx.a

clean:
	rm *.a *.o   