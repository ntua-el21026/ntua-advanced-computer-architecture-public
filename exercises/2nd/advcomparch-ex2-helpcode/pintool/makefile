ifndef PIN_ROOT
$(error Set PIN_ROOT to the installed Intel Pin kit)
endif
CONFIG_ROOT := $(PIN_ROOT)/source/tools/Config
include $(CONFIG_ROOT)/makefile.config
include makefile.rules
include $(TOOLS_ROOT)/Config/makefile.default.rules
override export PIN_WRAPPER_GCC := /usr/bin/gcc
