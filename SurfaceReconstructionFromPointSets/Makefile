CGALINCLUDEDIR=~/.homebrew/include
LIBDIR=/Users/noshita/.homebrew/lib
# CGALLIBS=$(LIBDIR)/libCGAL.dylib,$(LIBDIR)/libCGAL_Core.dylib,$(LIBDIR)/libCGAL_ImageIO.dylib,$(LIBDIR)/libboost_thread-mt.dylib,$(LIBDIR)/libgmp.dylib,$(LIBDIR)/libmpfr.dylib
CGALLIBS=$(LIBDIR)/libCGAL.dylib,$(LIBDIR)/libCGAL_Core.dylib,$(LIBDIR)/libCGAL_ImageIO.dylib,$(LIBDIR)/libboost_thread-mt.dylib,$(LIBDIR)/libboost_system-mt.dylib,$(LIBDIR)/libgmp.dylib,$(LIBDIR)/libmpfr.dylib
#必要に応じてstdlib=$(STDLIB)をつける．
# STDLIB=libstdc++
STDLIB=libc++

poisson_reconstruction_example.o: poisson_reconstruction_example.cpp
	clang++ -std=c++11 -I $(CGALINCLUDEDIR) -I $(CGALINCLUDEDIR)/eigen3 -o poisson_reconstruction_example.o -c poisson_reconstruction_example.cpp

poisson_reconstruction_example: poisson_reconstruction_example.o
	clang++ -std=c++11 -Wl,$(CGALLIBS) -frounding-math -o poisson_reconstruction_example poisson_reconstruction_example.o -v

clean:
	rm poisson_reconstruction_example.o
	rm poisson_reconstruction_example