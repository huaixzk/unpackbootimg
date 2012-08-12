CC = gcc
AR = ar rcv
ifeq ($(windir),)
RM = rm -f
CP = cp
else
RM = del
CP = copy /y
endif

EXT = a
LIB = libmincrypt.$(EXT)
LIB_OBJS = rsa.o sha.o
INC  = -I..

all:$(LIB)

clean:
	$(RM) $(LIB_OBJS) $(LIB)

$(LIB):$(LIB_OBJS)
	$(AR) $@ $^
	$(CP) $@ ..


%.o:%.c
	$(CC) -o $@ -c $< $(INC)




