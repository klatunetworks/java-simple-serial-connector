CXX=$(CROSS_COMPILE)g++
CPPFLAGS=-fPIC -Os
CPPFLAGS+=-I$(JDK_HOME)/include
CPPFLAGS+=-I$(JDK_HOME)/include/linux

all: jssc_x86

clean:
	rm -f *.o

jssc_x86: jssc.o
	$(CXX) -shared -o libjSSC-2.8_x86.so jssc.o

jssc_x86_64: jssc.o
	$(CXX) -shared -o libjSSC-2.8_x86_64.so jssc.o

jssc_armhf: jssc.o
	$(CXX) -shared -o libjSSC-2.8_armhf.so jssc.o

jssc_armsf: jssc.o
	$(CXX) -shared -o libjSSC-2.8_armsf.so jssc.o

jssc.o: jssc.cpp ../jssc_SerialNativeInterface.h
	$(CXX) $(CPPOPTS) $(CPPFLAGS) -c jssc.cpp
