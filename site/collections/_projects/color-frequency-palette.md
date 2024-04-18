---
title: Color Frequency Palette
subtitle: Image analysis application to create a palette of the most frequent colors in an image
image: /assets/img/projects/color-frequency-palette.jpg
priority: 2
---

## Prerequisites:
- g++ (C++ compiler)
- Make
- OpenCV

## To run:
1. Clone the repository by running the following in your machine's terminal:<br>
   `git clone https://github.com/cadedupont/color-frequency-palette.git`
3. Navigate to the directory containing the Makefile, which is the root directory of the project
4. Run `make` to compile the program and generate the executable
5. Run `./color_frequency <image_file>` from the root directory to run the program on the image of your choice (include file extension but exclude file path)

Included in the `res/in` directory are some sample images of album covers I used to test the program. The program is hardcoded to look inside the `res/in` directory for the image file, so if you want to use your own image, you'll need to move it into that directory.

## Output:
The program will generate two files in the `res/out` directory:
1. `<image_file_name>.jpg` - a 1000x1000 image containing a palette of the 100 most frequent colors found in the provided image, with each color's hex code written on their respective block in the palette
2. `<image_file_name>.csv` - a csv file containing every color's RGB values, hex code, and frequency in the original image (sorted by frequency in descending order)

## Examples:
<table>
  <tr>
    <td><p style="margin: 0 auto;" align="center">Album Cover</p></td>
    <td><p style="margin: 0 auto;" align="center">Input Image</p></td>
    <td><p style="margin: 0 auto;" align="center">Output Image</p></td>
  </tr>
  <tr>
    <td><p style="margin: 0 auto;" align="center"><i>Lahai</i> - Sampha</p></td>
    <td><img src="https://github.com/cadedupont/color-frequency-palette/raw/main/res/in/lahai.png" width="1000"/></td>
    <td><img src="https://github.com/cadedupont/color-frequency-palette/raw/main/res/out/lahai.jpg"/></td>
  </tr>
  <tr>
    <td><p style="margin: 0 auto;" align="center"><i>Wish You Were Here</i> - Pink Floyd</p></td>
    <td><img src="https://github.com/cadedupont/color-frequency-palette/raw/main/res/in/wish_you_were_here.jpg" width="1000"/></td>
    <td><img src="https://github.com/cadedupont/color-frequency-palette/raw/main/res/out/wish_you_were_here.jpg"/></td>
  </tr>
  <tr>
    <td><p style="margin: 0 auto;" align="center"><i>American Love Call</i> - Durand Jones & The Indications</p></td>
    <td><img src="https://github.com/cadedupont/color-frequency-palette/raw/main/res/in/american_love_call.jpg" width="1000"/></td>
    <td><img src="https://github.com/cadedupont/color-frequency-palette/raw/main/res/out/american_love_call.jpg"/></td>
  </tr>
  <tr>
    <td><p style="margin: 0 auto;" align="center"><i>This Old Dog</i> - Mac DeMarco</p></td>
    <td><img src="https://github.com/cadedupont/color-frequency-palette/raw/main/res/in/this_old_dog.jpg" width="1000"/></td>
    <td><img src="https://github.com/cadedupont/color-frequency-palette/raw/main/res/out/this_old_dog.jpg"/></td>
  </tr>
</table>