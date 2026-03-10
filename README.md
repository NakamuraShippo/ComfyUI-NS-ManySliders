# ComfyUI-NS-ManySliders
Node for ComfyUI to manipulate values with multiple sliders.  
[日本語はこちら](https://github.com/NakamuraShippo/ComfyUI-NS-ManySliders/blob/main/README_JP.md)  

This repository is no longer being updated and has been merged into [ComfyUI-NS-Util](https://github.com/NakamuraShippo/ComfyUI-NS-Util).  

<br>

///////////////////////////////////////////////////////////////////////////////////////////////////////

<br>


## Overview

ComfyUI-NS-ManySliders is a custom node developed for ComfyUI that allows you to manipulate values using multiple sliders. With this node, you can easily adjust numerous numerical parameters intuitively, making it useful for various purposes.

## Features

- Ability to adjust parameters using multiple sliders.  
- The number and range of sliders can be flexibly customized via a settings file.  
- Dynamically add sliders from a minimum of 1 to the maximum specified count.  
- Provides a simple output (single value) when the number of sliders is set to 1.

## File Structure
- nodes.py: Implements the main logic of the node.
- settings.yaml: Manages settings such as the number of sliders, minimum value, maximum value, and default value.
- README.md: This document.
- __init__.py: Initialization file to register the NS_ManySliders node with ComfyUI.

## Installation
1. Clone this repository locally.
2. Place it in the custom nodes directory of ComfyUI.
3. Edit the settings.yaml file as needed to configure the number of sliders and other parameters.

## Settings
- settings.yaml allows you to configure the following settings:
- count: Number of sliders (default is 15)
- min_value: Minimum value for each slider (e.g., -1.0)
- max_value: Maximum value for each slider (e.g., 1.0)
- default_value: Default value for each slider (e.g., 0.0)

## Usage
1. Add the "NS_ManySliders" node in ComfyUI.
2. Specify the number of sliders to use via the slider_count parameter.
3. Adjust the value of each slider to reflect in the output.
4. When slider_count is set to 1, a single value will be output. Otherwise, the values of the sliders will be output as a comma-separated string.

## Notes
- Ensure that slider_count does not exceed the maximum number of sliders specified in the settings.
- After modifying the settings.yaml file, you need to restart ComfyUI.

## Examples
- If slider_count = 1, the output will be a single value (e.g., "0.0").
- If slider_count = 3, the output will be a comma-separated string (e.g., "0.0,0.0,0.0").
