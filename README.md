# camera-capture

![demo](demo.gif)

## What is this?

A small script to assist with using a DSLR camera as a webcam, using gphoto2, ffmpeg, and v4l2loopback.


## Why is this?

I got sick of not being able to control the camera while 'recording' - change focus, adjust aperture, etc,
which comes in handy with changing lighting conditions and focus needs.


## Installation

Install the needed gems, and run it:

    gem install gphoto2 rmagick tty-prompt tty-spinner
    ./camera-capture

Written for ruby 2.7, but will probably work with as far back as 2.4 - untested, however.


## What can I/can't I do with it?

Currently, you can:

- Autofocus once (or more, if you're lucky!)
- Manually focus
- Adjust aperture
- Adjust shutter speed
- Send arbitrary gphoto2 configs
- Restart the capture


Known bugs:

- Autofocus. At least with my camera, it usually only ever focuses once. Attempting to 'cancel' and then
  re-focus has rarely, if ever, worked for me.
- Adjustment of other camera properties nicely (feel free to use the raw gphoto configs though)


## Tested Cameras

- Canon EOS Rebel T3i
- Canon EOS M50


## Desired features/"roadmap I may or may not ever get to"

- [ ] Bundle into a gem
- [ ] Hotkeys for menus (less arrow/pgup/pgdn usage)
- [ ] Fix autofocus
- [ ] Better interface for changing aperture/etc
- [ ] Feedback for what the current focus level is at (is that even possible..?)
- [ ] Feedback in general (i.e. a "status line" or HUD) for what's going on
- [-] More customizability in terms of ffmpeg options (i.e. device name, type, format)
  - [x] change geometry/aspect at startup
  - [ ] change output geometry on the fly (seems to break the v4l2 device?)
  - [x] change output device
  - [ ] change output format
  - [ ] sub-menu for ffmpeg status/options
- [ ] Ability to mess with the video feed (add filters, frames, rotate...)
- [ ] Configuration saving/restoring

