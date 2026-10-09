TOP=../..

include $(TOP)/configure/CONFIG

LIBRARY_IOC += HidenRGA

DBD += HidenRGA.dbd

# Source files
HidenRGA_DBD += measValue.dbd
HidenRGA_SRCS += measValue.c

# Build SNL programs when SNCSEQ is defined
ifneq ($(SNCSEQ),)
    HidenRGA_SNCFLAGS += +d
    HidenRGA_DBD += sncHidenRGA.dbd
    HidenRGA_SRCS += sncDegas.stt
    HidenRGA_LIBS += seq pv
endif

#=============================

include $(TOP)/configure/RULES

#----------------------------------------
#  ADD RULES AFTER THIS LINE
