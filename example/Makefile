CC=gcc
CFLAGS=-Wall -Wextra -Wpedantic

SOURCE=test.c Bitmap.c ../Font_Driver.c
OBJECTS=$(SOURCE:%.c=%.o)

Test: $(SOURCE)
	$(CC) $^ $(CFLAGS) -o $@

$(SOURCE): Font.font.h

Font.font.h: Font.bmp
	./img2font.sh

clean:
	rm -f $(OBJECTS) Font.font.h
