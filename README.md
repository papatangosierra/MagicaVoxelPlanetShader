# MagicaVoxelPlanetShader
 A Magicavoxel shader that can be used to create interesting sphere-shaped objects

##  Getting Started
After seelctinbg the shader, you will see a result that looks something like this:

[Default Planet and Palette](<img width="250px" src="images/default_planet.png"/>


This looks like a mess because the default palette is fairly erratic.  You can create your own pallete,or load one of the ones provided in this repo.

<img src="images/default_planet_landmass.png" width="250px" />

## Parameters

| Parameter         | Descruotuib|
| ---               | ---       |
| Zoom              | Determines scale of our noise.  Smaller values is more 'zoomed out', larger more 'zoomed in'  |
| X/Y/Z Offset      | Translation of our noise.  You can use this to 'move' around int he noise. |
| StartColor        | Our first color indext to use to color our planet. |
| EndCOlor          | Last index to use for our planet. |
| Cut-off           | If > 0, any voxels with a color index above this value will be removed from the model.   This can be used ot make more abstract models. |
| WaterThresh       | Used for ReliefHeight.  If set, colors below this value are considered 'water' and will be removed from the layers reserved for relief height | | 
| ReliefHeight      | How may voxels of projection you want. Any colors below WaterThresh will be removed for this many layers.|
| RemoveColor       | Use this to remove voxels with the given index.  Useful for creating cavernous structures, along with Cut-off. |
| Octaves           | Determines how many iterations of noise to apply to our noise values.   Increaasing this will make the result look more rough, decreasing will make things look more uniform. |
| OctaveMultiple    | Changes how much the results change in each octave.  Increaseing this will make edges look more noisy. |
| Amplitude         | Scales the results of the noise.   This can incase/reduce the peaks/troughs of the noise |
| AmplitudeMultiple | The amount which the amplitude increases with each octave.  This can dampen/enhance the effects of the amplutide over each octave. |
| RemapType         | 0 will eliminate negative index colors from the noise values.   1 will allow negative noise values (which will just be mapped to the 1st color) |


## Zoom


Zoom set to 10, 60, 120,and 360

<img src="images/zoom_10.png" width="120px" /><img src="images/zoom_60.png" width="120px" /><img src="images/zoom_120.png" width="120px" /><img src="images/zoom_360.png" width="120px" />

## X/Y/Z Offset 

You can pan the resulting noise by adjusting these values.   The following examples show the X offset at 0.0, 0.1, and 0.5:

<img src="images/offset_0.png" width="120px" /><img src="images/offset_1.png" width="120px" /><img src="images/offset_5.png" width="120px" />

## StartColor

<img src="images/startcolor_1.png" width="120px" /><img src="images/startcolor_30.png" width="120px" />

## EndColor

<img src="images/endcolor_30.png" width="120px" /><img src="images/endcolor_128.png" width="120px" />

## Cut-off

This value can be used to create eroded/cavernous structures.

The following are cut-off values of 0 (default), 33, and 128:
<img src="images/cutoff_0.png" width="120px" /><img src="images/cutoff_33.png" width="120px" /><img src="images/cutoff_128.png" width="120px" />

## Relief
Along with WaterThresh, this can be used to add a bit of releif to the model.   This method simply removes 'water' from the upper layers, so it can make the 'land' look like it's tpaered out if it's too  high.

<img src="images/relief_0.png" width="120px" /><img src="images/relief_1.png" width="120px" /><img src="images/relief_2.png" width="120px" />

## WaterThresh

The following are examples of setting waterthresh to 1, 60, and 120:

<img src="images/waterthresh_1.png" width="120px" /><img src="images/waterthresh_60.png" width="120px" /><img src="images/waterthresh_2.png" width="120px" />

## RemoveColor

Selectively remove a single color.   The following are examples where we have no removeal and one with the 2nd index removed (out of 5 total colors):

<img src="images/removecolor_0.png" width="120px" /><img src="images/removecolor_1.png" width="120px" />

## Octaves

Octaves are essentialyl the number of times the noise is called on itself.  More octaves will produce a more complex contour.  

<img src="images/octaves_1.png" width="120px" /><img src="images/octaves_2.png" width="120px" /><img src="images/octaves_3.png" width="120px" /><img src="images/octaves_12.png" width="120px" />










