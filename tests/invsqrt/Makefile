####################################################
# This file is distributed under the               #
# University of Illinois/NCSA Open Source License. #
# See LICENSE file in top directory for details.   #
#                                                  #
# Copyright (c) 2016 FIGSiM developers             #
####################################################

# Makefile

# compile tests

PREFIX=../../

include $(PREFIX)Makefile.choices
include $(PREFIX)Makefile.check


# Program name
PROG_NAME=invsqrt

# Define object code files
OBJS = ScalarMat.o VecMat.o

# Compile executable and link
all: $(OBJS)
	$(CPP) $(CPPFLAGS) $(ALL_INCLUDES) -o $(PROG_NAME) $(PROG_NAME).cpp $(LIB_OPENCL) $(OBJS)

# Compile object code files without linking
%.o:$(PREFIX)%.cpp
	$(CPP) $(CPPFLAGS) $(ALL_INCLUDES) -c $< -o $@

clean:
	rm -f *.o $(PROG_NAME)

test: all
	./$(PROG_NAME)
