CXX = cl
CXXFLAGS = /EHsc /nologo
MAIN_EXECUTABLE = main.exe 

all: $(MAIN_EXECUTABLE) 
.PHONY: all

$(MAIN_EXECUTABLE):main.obj sort.obj
	link /nologo $^ /OUT:$@
	
main.obj: main.cpp
	$(CXX) $(CXXFLAGS) /c $<	
	
%.obj: %.cpp %.h
	$(CXX) $(CXXFLAGS) /c $<	
	
clean:
	del *.obj

distclean: clean 
	del $(MAIN_EXECUTABLE) 
.PHONY: clean distclean