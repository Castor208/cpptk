COMPILER = g++ -std=c++17 -Wno-parentheses
OPTIONS = -Wall -Wno-long-long -pedantic
INCLUDES = -I.. -I/usr/include/tcl8.6 -I/usr/include/tk8.6
INCLUDES = -I.. -I/System/Library/Frameworks/Tcl.framework/Headers -I/System/Library/Frameworks/Tk.framework/Headers -I$(BOOST_ROOT)
LIBDIRS =
LIBS = -ltcl8.6 -ltk8.6
LIBS = -ltcl8.5 -ltk8.5

ALL_OPTIONS = ${OPTIONS} ${INCLUDES} ${LIBDIRS} ${LIBS}


ALL_OUTS = example0 example1 example2 example3 example4 example5 example6

all : ${ALL_OUTS}

example0 : example0.cc cpptk.o cpptkbase.o
	${COMPILER} example0.cc cpptk.o cpptkbase.o -o $@ ${ALL_OPTIONS}

example1 : example1.cc cpptk.o cpptkbase.o
	${COMPILER} example1.cc cpptk.o cpptkbase.o -o $@ ${ALL_OPTIONS}

example2 : example2.cc cpptk.o cpptkbase.o
	${COMPILER} example2.cc cpptk.o cpptkbase.o -o $@ ${ALL_OPTIONS}

example3 : example3.cc cpptk.o cpptkbase.o
	${COMPILER} example3.cc cpptk.o cpptkbase.o -o $@ ${ALL_OPTIONS}

example4 : example4.cc cpptk.o cpptkbase.o
	${COMPILER} example4.cc cpptk.o cpptkbase.o -o $@ ${ALL_OPTIONS}

example5 : example5.cc cpptk.o cpptkbase.o
	${COMPILER} example5.cc cpptk.o cpptkbase.o -o $@ ${ALL_OPTIONS}

example6 : example6.cc cpptk.o cpptkbase.o
	${COMPILER} example6.cc cpptk.o cpptkbase.o -o $@ ${ALL_OPTIONS}

cpptk.o : ../cpptk.cc
	${COMPILER} $? -o $@ -c ${OPTIONS} ${INCLUDES}

cpptkbase.o : ../base/cpptkbase.cc
	${COMPILER} $? -o $@ -c ${OPTIONS} ${INCLUDES}


clean :
	rm -f ${ALL_OUTS} cpptk.o cpptkbase.o
