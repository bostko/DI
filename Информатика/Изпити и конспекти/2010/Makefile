CXX=g++
BIN_PATH=./bin
CXXFLAGS=-I. -g -O0 -Wall -Wextra

dllist.o:
	$(CXX) -c dllist.cpp -o $(BIN_PATH)/dllist.o $(CXXFLAGS)

test: dllist.o
	$(CXX) -o $(BIN_PATH)/dllist_test $(BIN_PATH)/dllist.o dllist_test.cpp

dllist_bin: dllist.o
	$(CXX) -o $(BIN_PATH)/dllist.bin $(BIN_PATH)/dllist.o dllist_bin.cpp $(CXXFLAGS)

## hpp cannot be compiled
#dllist_templ.o:
#	$(CXX) -c dllist_templ.hpp -o $(BIN_PATH)/dllist_templ.o $(CXXFLAGS)

dllist_templ_test:
	$(CXX) -o $(BIN_PATH)/dllist_templ.bin dllist_templ_test.cpp $(CXXFLAGS)


debug: CXXFLAGS += -g -O0 -Wall -Wextra
debug: dllist_bin

all: dllist_bin

clean:
	rm -f $(BIN_PATH)/dllist*
