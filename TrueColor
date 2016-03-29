#include <iostream>
#include <fstream>

using namespace std;

int main()
{
 unsigned char header_24bits_4096x4096_BMP[] =  {0x42 ,0x4D ,0x36 ,0x00 ,0x00 ,0x03 ,0x00 ,0x00 ,0x00 ,0x00 ,0x36 ,0x00 ,0x00 ,0x00 ,0x28 ,0x00 ,0x00 ,0x00 ,0x00 ,0x10 ,0x00 ,0x00 ,0x00 ,0x10 ,0x00 ,0x00 ,0x01 ,0x00 ,0x18 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x03 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00 ,0x00};
 unsigned char red = 0x00;
 unsigned char green = 0x00;
 unsigned char blue = 0x00;
 
 ofstream myfile;
 myfile.open ("example.bmp", ios::out | ios::binary);

 // Print BMP header array
 for(int i=0 ; i < sizeof(header_24bits_4096x4096_BMP) ; i++){
  myfile << header_24bits_4096x4096_BMP[i];
 }

 // print RGB chars
 for (int blue_count=0 ; blue_count<256 ; blue_count++){
  for(int green_count=0; green_count<256 ; green_count++){
   for(int red_count=0; red_count<256 ; red_count++){
    // Output the RGB chars
    myfile << blue << green << red;
    if(red_count==255){red=0x00;} else {red++;}
   }
   if(green_count==255){green=0x00;} else {green++;}
  }
  if(blue_count==255){blue=0x00;} else {blue++;}
 }
 myfile.close();

 cout << "BMP Output completed" << endl; 
 return 0;
}

