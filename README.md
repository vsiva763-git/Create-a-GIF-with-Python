# Create-a-GIF-with-Python

A simple Python script to create animated GIFs from multiple image files.

## Description

This project demonstrates how to create animated GIFs using Python and the `imageio` library. The script takes multiple image files as input and combines them into a single animated GIF file.

## Features

- Simple and straightforward implementation
- Uses the `imageio` library for image processing
- Customizable duration between frames
- Creates looping animations

## Requirements

- Python 3.x
- imageio library

## Installation

Install the required dependency:

```bash
pip3 install imageio
```

## Usage

1. Place your image files (PNG, JPG, etc.) in the same directory as the script
2. Update the `filenames` list in `create_gif.py` with your image names
3. Run the script:

```bash
python create_gif.py
```

## Example

The script reads multiple images and combines them into an animated GIF:

```python
import imageio.v3 as iio

filenames = ['team-pic1.png', 'team-pic2.png']
images = []

for filename in filenames:
    images.append(iio.imread(filename))

iio.imwrite('team.gif', images, duration=500, loop=0)
```

This example creates an animated GIF from two images with 500ms duration between frames and infinite looping.

## Configuration

You can customize the GIF output by modifying:
- `duration`: Delay between frames in milliseconds (default: 500)
- `loop`: Number of loops (0 = infinite loop)
- Output filename: Change `'team.gif'` to your desired filename

## Output

The script generates an animated GIF file (e.g., `team.gif`) that combines all specified images into a seamless animation.

## License

This project is open source and available for personal and educational use.