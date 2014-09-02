LIBS = -lopencv_core -lopencv_imgproc -lopencv_highgui
CXX = g++
CXXFLAGS = -Wall `pkg-config --cflags opencv`
LDFLAGS = $(LIBS)

all: libmeanshift.so meanshift_demo

meanshift_demo: main.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) -Wl,-rpath,. -L . -lmeanshift -o $@ $?
main.o: main.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

libmeanshift.so: MeanShift.o
	$(CXX) $(CXXFLAGS) -shared -o $@ $?
MeanShift.o: MeanShift.cpp MeanShift.h
	$(CC) $(CXXFLAGS) -fPIC -c $< -o $@

.PHONY: clean
clean:
	rm *.o meanshift_demo libmeanshift.so
