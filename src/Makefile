test: clean_buff.o vector.o ydl_hash.o ydl_catalog.o ydl_block.o ydl_stub.o ydl_main
clean_buff.o: clean_buff.cpp clean_buff.h
	g++ -c clean_buff.cpp
vector.o: vector.cpp vector.h
	g++ -c vector.cpp
ydl_hash.o: ydl_hash.cpp ydl_hash.h clean_buff.o
	g++ -c clean_buff.o ydl_hash.cpp
ydl_catalog.o: ydl_catalog.cpp ydl_catalog.h clean_buff.o
	g++ -c clean_buff.o ydl_catalog.cpp
ydl_block.o: ydl_block.cpp ydl_block.h clean_buff.o
	g++ -c clean_buff.o ydl_block.cpp
ydl_stub.o: ydl_stub.cpp ydl_stub.h
	g++ -c ydl_stub.cpp
ydl_main: ydl_main.cpp ydl_main.h ydl_block.o ydl_catalog.o ydl_hash.o
	g++ -o ydl_main ydl_block.o ydl_catalog.o ydl_hash.o ydl_main.cpp
