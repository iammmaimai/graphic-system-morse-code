#vga morse code writer
this project is a morse code text editor made in verilog for tiny tapeout. you type morse code using the inputs and it converts it into letters/numbers on a vga display screen.

it stores up to 256 characters in memory and shows a preview of your dots and dashes on the bottom left before you send the character to the main text area.

controls
uses the inputs on ui_in:

ui_in[0] - dot (.)

ui_in[1] - dash (-)

ui_in[2] - submit letter (decodes morse pattern and prints character)

ui_in[3] - space

ui_in[7] - backspace / clear current morse input

features
morse decoder: maps combinations of dots/dashes to letters A-Z and numbers 0-9. invalid codes show as ?.

live preview: shows the dots and dashes you are typing at the bottom of the screen before submitting.

font bitmap: custom 5x7 bitmap generator for all rendered characters.

vga display: outputs standard 640x480 timing with green text and a small cursor line.

pins & outputs
uo_out: outputs vga sync signals (hsync, vsync) and 2-bit RGB color signals.

uio_out / uio_oe: set to zero (unused).
