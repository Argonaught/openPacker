# openPacker
A simplified open source version of Texture Packer.

It is used to combine many images into a single one so that the combined image does not have much empty space.

For more on the problem: see [the packing problems (wikipedia)](https://en.wikipedia.org/wiki/Packing_problems), [the Bin Packing Problem (wikipedia)](https://en.wikipedia.org/wiki/Bin_packing_problem), [this paper](http://www.aaai.org/Papers/ICAPS/2003/ICAPS03-029.pdf), or [this article (codeproject)](https://www.codeproject.com/Articles/210979/Fast-optimizing-rectangle-packing-algorithm-for-bu#basic).

# How to run
```
python openPacker.py image1.png image2.png image3.png
```

# Output
The output is two things:
1) An atlas (spritesheet) image named 'spritesheet.png'
2) A JSON file on how to read the 'spritesheet.png'


# Example run on the images in the 'imgs' folder
```
python openPacker.py imgs/green.png imgs/dirt_green.png imgs/dirt.png imgs/cinema.png imgs/house_blue.png imgs/house_green.png imgs/house_red.png imgs/tilenew.png imgs/tree.png
```

1) Image (located at 'output/spritesheet.png'):

![alt tag](https://github.com/skaparelos/openPacker/blob/master/output/spritesheet.png?raw=true)

2) JSON (located at 'output/out.json'):
```
[
    {
        "frame": {
            "y": 0, 
            "x": 0, 
            "w": 256, 
            "h": 200
        }, 
        "filename": "imgs/cinema.png"
    }, 
    {
        "frame": {
            "y": 0, 
            "x": 256, 
            "w": 128, 
            "h": 110
        }, 
        "filename": "imgs/house_blue.png"
    }, 
    {
        "frame": {
            "y": 0, 
            "x": 384, 
            "w": 128, 
            "h": 110
        }, 
        "filename": "imgs/house_green.png"
    }, 
    {
        "frame": {
            "y": 0, 
            "x": 512, 
            "w": 128, 
            "h": 110
        }, 
        "filename": "imgs/house_red.png"
    }, 
    {
        "frame": {
            "y": 0, 
            "x": 640, 
            "w": 128, 
            "h": 110
        }, 
        "filename": "imgs/tree.png"
    }, 
    {
        "frame": {
            "y": 110, 
            "x": 256, 
            "w": 128, 
            "h": 64
        }, 
        "filename": "imgs/green.png"
    }, 
    {
        "frame": {
            "y": 110, 
            "x": 384, 
            "w": 128, 
            "h": 64
        }, 
        "filename": "imgs/dirt_green.png"
    }, 
    {
        "frame": {
            "y": 110, 
            "x": 512, 
            "w": 128, 
            "h": 64
        }, 
        "filename": "imgs/dirt.png"
    }, 
    {
        "frame": {
            "y": 110, 
            "x": 640, 
            "w": 128, 
            "h": 64
        }, 
        "filename": "imgs/tilenew.png"
    }
]
```
