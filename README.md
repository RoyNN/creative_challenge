My Blog URL: http://roy-img.blogspot.hk/2015/04/print-out-167millions-different-colors.html

Print Out 16.7millions Different Colors In One Picture Using C++ (1x1 pixel per color)

Explanation:

BMP(bitmap) is an old uncompressed image format (wiki) , and it uses three 8bits(or three bytes) to represent colors in the image (or, equal to three 2-digits hexadecimal number 0x00 to 0xFF).

Therefore, it gives a total 16,777,216 colors. (16.7millions)




It could be calculated as below:

16,777,216 = 28 x 28 x 28 (three 8 bits) , OR 224 (So called 24-bit colors) , OR

16,777,216 = (16x16) x (16x16) x (16x16) = 256x256x256 (three 2-digits hexadecimal number))

(since 0x0~0xF has 16 combinations, then 0x00~0xFF has 16x16 = 256 combinations, refer to hexadecimal (wiki))


With using C++, we could simply produce 16.7millions different colors (1x1 pixel per color) in one BMP image file.

First of all, to simplify the effort, we use a header from a 4096x4096 24bits-BMP image as header template. (If you require a more advanced control, such as width & height, color bit-depth,etc., you need to google for a BMP file specification)

Then, it is the time to loop out 3 colors(with increment) which they each have a range (0-255/0x00~0xFF). We use a "unsigned char" to represent a color, and write file using binary.
