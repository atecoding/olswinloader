CC = gcc
CFLAGS = -g -O0 -std=c99
LDFLAGS =
APP = ols_loader
OBJS =  ols_loader.o ols.o data_file.o serial.o

ifeq ($(shell uname), Darwin)
	CFLAGS = -g -O0 -std=c99 -DMACOSX=1 -force_cpusubtype_ALL -arch i386 -arch ppc
endif

all: $(APP)

$(APP):  $(OBJS)
	$(CC) $(CFLAGS) -o $(APP) $(OBJS) $(LFD_OBJS) $(LDFLAGS)

%.o:	%.c 
	$(CC) $(CFLAGS) $(DEFS) -c $<


clean:
	rm -f $(APP) *.o

