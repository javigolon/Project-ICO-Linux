# Project ICO Tools (Linux Fork)

A Linux-compatible fork of the ICO Tools, designed to extract and work with game assets from the ICO PlayStation 2 disc image.

## Requirements:
* A valid ICO game ISO file. (If you have a `.bin` file, convert it to `.iso` using PowerISO or another image conversion tool.)

## Usage:
1. Clone this repository.
   ```
   git clone https://github.com/javigolon/Project-ICO-Linux.git
   cd Project-ICO-Linux
   ```
2. Mount your ICO ISO image and copy `data.df` into the project root directory.
3. Make sure `df-read2` can be executable.
   ```
   chmod +x df-read2
   ```
5. Run the extraction tool.
   ```
   python main.py data.df
   ```
* All game files will be extracted into the `data` folder.
* Model files (.p2o and .p2c) will be converted into .obj and .mtl files.
* Texture files (.tm2) will be converted into .png files.

## Notes:
* Tested with the game version `ICO (USA)`.
* Some textures fail to convert. This is usually because the resolution hasn't been programmed in texture_export.py.
* Model normals are broken. Enabling backface-culling will make 50% of the models polygons invisible.
* Terrain is upside-down. (Might be all .p2o models)

## Thanks:
* Half-asian for original project.
* majo33 for the creation of df-read2 https://github.com/majo33/df-read2
* ps23dformat.wikispaces.com (Archive.org only) for hosting valuable information on Ico's file structures. It is sad that the website is defunct as they had information on dozens of games, which you can find almost nowhere else.

Hopes and dreams:
People will make cool stuff with the Ico content. Also, full debug symbols for the Ico binary are literaly included on the European version of the disc. They are just waiting to be reverse engineered.
