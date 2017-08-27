CC = gcc
CFLAGS = -std=c99 -D_GNU_SOURCE
LD_FLAGS = -lrt

all: pshm_create_simple pshm_write pshm_read

pshm_create_simple: pshm_create_simple.o
	$(CC) $(CFLAGS) -o $@ $^ $(LD_FLAGS) 

pshm_write: pshm_write.o
	$(CC) $(CFLAGS) -o $@ $^ $(LD_FLAGS)

pshm_read: pshm_read.o
	$(CC) $(CFLAGS) -o $@ $^ $(LD_FLAGS)

%.o: %.c
	$(CC) -c $(CFLAGS) -o $@ $^

clean:
	rm -f *.o pshm_create_simple pshm_write pshm_read
