# godot-sugar

Experimental post-processing toolkit for Godot.

## Showcase

![pixelate](./media/pixelate.gif?raw=true "pixelate")

Video: [https://www.youtube.com/watch?v=C4oMqvwJ4FU](https://www.youtube.com/watch?v=C4oMqvwJ4FU)

## Features

This project provides a couple of nodes:

* `SugarLayer` (`CanvasLayer`) - works with both - 2D and 3D scenes
* `SugarQuad` (`MeshInstance` with `1x1` quad) - works with 3D scenes only

which apply selected effect to the entire screen:

* `None` - no effect
* `Blurr` - applies blurr effect
* `Pixelate` - pixelate effect - provides a pixel-art look in runtime
* `Grayscale` - changes colors to grayscale
* `Sepia` - applies sepia effect
* `Grain` - adds/removes/mixes-in a grain (open simplex noise) effect
* `Palette` - changes color palete (with optional dithering effect)
* `Lut` - changes color space using lookup table (LUT)
* `Darken` - makes scene darker
* `Depth` - shows depth buffer
* `Outline` - draws the outline using depth buffer (it gives a poor effect with artifacts for now)

## Caveats

This Godot addon is experimental and it may even crash the entire editor. I recommend to use it with care - for prototyping purposes only.

## Installation

1. Get the contents of this repository to your project's `res://addons/godot-sugar` directory:
    * either download
    * or clone
    * or add as a submodule: `git submodule add https://github.com/Scony/godot-sugar.git addons/godot-sugar`
2. Enable plugin in `Project Settings/Plugins`

## Usage

After enabling the plugin in the `Project Settings` you can add eiter `SugarLayer` or `SugarQuad3D`:

![add node](./media/add_node.png?raw=true "add node")

and once it's done, you can select `Effect` in ispector and tweak parameters under `Parameters->Shader Param`.
