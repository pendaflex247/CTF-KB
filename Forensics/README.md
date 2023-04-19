CTF Image Steganography Checklist
Each example image contains a flag.

Steg Checklist


1. **File**: To know what file you're working with.  

file filename.png

2. **Strings**: View all strings   

    strings -n 7 -t x filename.png

- n 7 for strings of length  
- t x to view- their position in the file  

3. **Exif**

    exif filename

4. **Binwalk**: To check for hidden embedded files withing images or documents.  

    binwalk -Me filename.png. 

- -Me to extract any files recursively.  


5. **pngcheck**: To view bronken image chunk   

    pngcheck -vtp7f filename.png 

- Use "v" for verbose output.  
- "t" and "7" options display tEXt chunks.  
- Use "p" option to display the contents of certain optional chunks.  
- Use "f" option to continue execution even after encountering major errors.  

6. **Steghide**: Use steghide to check for hidden passwords or data in an image.

    steghide extract -sf filename.png

- Explore colour and bit planes for hidden images using online tools.  
- Extract LSB data from bit planes and select relevant bits.  
- Check RGB values of an image for hidden ASCII characters/data.  
- Use steghide to check for hidden passwords or data in an image.  
