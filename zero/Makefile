# INCFLAGS  = -I /usr/include/GL
# INCFLAGS += -I /mit/6.837/public/include/vecmath

INCFLAGS += -I /usr/local/include/GL
INCFLAGS += -I /usr/local/include/vecmath

# LINKFLAGS  = -lglut -lGL -lGLU
# LINKFLAGS += -L /mit/6.837/public/lib -lvecmath

LINKFLAGS = -lglut -lglfw -framework OpenGL
LINKFLAGS += -L /usr/local/lib/vecmath -lvecmath

CFLAGS    = -O2
CC        = g++
SRCS      = main.cpp
OBJS      = $(SRCS:.cpp=.o)
PROG      = bin/main

all: $(SRCS) $(PROG)

$(PROG): $(OBJS)
	$(CC) $(CFLAGS) $(OBJS) -o $@ $(INCFLAGS) $(LINKFLAGS)

.cpp.o:
	$(CC) $(CFLAGS) $< -c -o $@ $(INCFLAGS)

depend:
	makedepend $(INCFLAGS) -Y $(SRCS)

clean:
	rm $(OBJS) $(PROG)

