CC		:=	g++
CXX		:=	g++
CPPFLAGS:=	
LDFLAGS	:=	
LDLIBS	:=

EXE		:=	a
SRCS	:=	$(EXE).cc b.cc
OBJS	:=	$(subst .cc,.o,$(SRCS))

all:	$(EXE)

$(EXE):	$(OBJS)

clean:
	$(RM)	$(EXE) $(OBJS)

distclean:	clean
	$(RM)	*~ .depend

# A depend target and rule that compute source dependencies
depend:	.depend

.depend:	$(SRCS)
	$(RM)	./depend
	$(CXX)	$(CPPFLAGS) -MM $^ >> ./.depend;

# Append at the end of the Makefile all dependencies
include	.depend
