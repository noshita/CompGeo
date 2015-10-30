CGALINCLUDEDIR=/Users/noshita/.homebrew/include
LIBDIR=/Users/noshita/.homebrew/lib
# CGALLIBS=$(LIBDIR)/libCGAL.dylib,$(LIBDIR)/libCGAL_Core.dylib,$(LIBDIR)/libCGAL_ImageIO.dylib,$(LIBDIR)/libboost_thread-mt.dylib,$(LIBDIR)/libgmp.dylib,$(LIBDIR)/libmpfr.dylib
CGALLIBS=$(LIBDIR)/libCGAL.dylib,$(LIBDIR)/libgmp.dylib
#必要に応じてstdlib=$(STDLIB)をつける．
STDLIB=libc++

HelloCGAL.o: HelloCGAL.cpp
	clang++ -I $(CGALINCLUDEDIR) -o HelloCGAL.o -c HelloCGAL.cpp

HelloCGAL: HelloCGAL.o
	clang++ -std=c++11 -Wl,$(CGALLIBS) -frounding-math -o HelloCGAL HelloCGAL.o

clean:
	rm HelloCGAL.o
	rm HelloCGAL