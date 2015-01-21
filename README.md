# LUCID Frame Viewer

A frame viewer for raw data files from the LUCID experiment.

![screenshot](img/screenshot.png)

## Installation and Usage

### Installation Instructions

To use the viewer you will need the following Python 2 libraries to be installed:

* NumPy
* Tkinter, with imaging support
* PIL
* PyEphem

Or in the terminal:

```
$ sudo apt-get install python-numpy python-tk python-imaging python-imaging-tk
$ sudo pip install ephem
```

Then clone the repository...

```
$ git clone https://github.com/calhewitt/lucid-frame-viewer
```

Finally, add the viewer to your PATH so it can be run from anywhere (replace ~/lucid-frame-viewer with wherever you downloaded the repo to):

```
$ PATH=$PATH:~/lucid-frame-viewer
```

### Usage

To start the viewer on a file, simply run

```
$ frameview datafile.ldat
```

If you need noise masking to be enabled, run the viewer with the *noisemask* option, eg:

```
$ frameview datafile.ldat --noisemask
```

## Getting new Telemetry Data

The frame viewer uses telemetry data from the SpaceTrack API to compute positions, and after time this will become inaccurate. To update the data, run the get_tle script from the terminal.