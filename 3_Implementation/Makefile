PROJ_NAME = calender
SRC = main.c project.c 

ifdef OS
	RM = del/q
	Fixpath = $(subst /,\,$1)
	EXEC = exe 
else
	ifeq ($(shell uname),Linux)
		RM = rm -rf
		Fixpath = $1
		EXEC = out
	endif
endif

Build:
	gcc $(SRC) -O $(call Fixpath,$(PROJ_NAME).$(EXEC))
run:Build
	./$(call Fixpath,$(PROJ_NAME).$(EXEC))
