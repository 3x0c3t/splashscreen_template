# splashscreen_template

# /**************************************************************************************
CODE_REFERENCES :
_______________________________________________________________________________________
CODE_NAME :       SplashScreen_template
CODE_VERSION :    V1.0
CODE_DATE :       2022/12/20
CODE_AUTHOR :     -3XØC3T-
CODE_WEBSITE :    www.3x0c3t.com
CODE_REPOSITORY : 
CODE_RIGHTS :     XXX
/**************************************************************************************
CODE_DESCRIPTIONS :
_______________________________________________________________________________________
This code display a SplashScreen on an OLED SSD1306 128x64 screen.
***************************************************************************************
COMPONENTS LIST :
_______________________________________________________________________________________
  QTY   NAME                        REF
  1     COMPONENT                   COMPONENTS_REF
          
_______________________________________________________________________________________
CODE START HERE ! please 3njØÿ ! -3xØc3t-
***************************************************************************************

**************************************************************************************/
#include "ssd1306.h"

void setup()
{ 
  #define codeAuthor "-codeAuthor-"
  #define codeName "codeName"
  #define codeVersion "V1.0"
  #define codeDate "YYYY/MM/DD"
  #define codeCheck ".codeCheck."
  

  
  /*DISPLAY ON THE SCREEN*/
  ssd1306_128x64_i2c_init();
  ssd1306_clearScreen();
  ssd1306_fillScreen(0x00);
  ssd1306_setFixedFont(ssd1306xled_font6x8);
  ssd1306_printFixedN (15, 0, codeAuthor, STYLE_BOLD, FONT_SIZE_2X);
  ssd1306_drawLine(0,20,128,20);
  ssd1306_drawLine(0,24,128,24);
  ssd1306_printFixed (0, 35,codeName , STYLE_BOLD);
  ssd1306_printFixed (0, 45,codeVersion , STYLE_BOLD);
  ssd1306_printFixed (0, 55,codeDate , STYLE_BOLD);
  ssd1306_printFixed (0, 63,codeCheck, STYLE_NORMAL);


  
}
  

void loop()
{
}
