****LIVE, realtime 360 Camera viewer and controller, in browser.****

Great for use as a PTZ in a live event setting that can fit in odd-ball spots, or to have one camera get multiple different angles at the same time, *live!*, or as a great shorter-distance "spy" camera.

Utilizes the wonderful "Photo Sphere Viewer" Javascript library. https://github.com/mistic100/Photo-Sphere-Viewer

Prerequisites:
- Must have a 360 camera capable of live, 360° video output (typically equirectangular format).
    - IF 360 camera has a standard video output (HDMI, SDI), you need a capture card to convert to UVC.
    - IF 360 camera has a "Webcam" USB output, you *might* need a UVC-to-HDMI and capture card for long distances. See below.
- Internet connection to reach a web address. Javascript runs locally from there. **It will still work if you temporarily lose internet, don't refresh!**


How to use:
1.  Set 360 camera to output "equirectangular" 360° video
2a. IF CAMERA HAS HDMI (or such) OUTPUT:
    - Camera output will need to be brought in to your PC with a capture card, such that you now have a UVC input.
    - If any social chat platform can see the camera, you're in good shape.
    - Does not currently support Decklink!
2b. IF CAMERA HAS "Webcam" OUTPUT:
    - For short distances, plug USB directly to PC and continue.
    - If long distances are required, conversion from UVC to HDMI (or such) is probably required. Use a capture card again to connect to PC, like above.
3.  Open https://360.danieleastman.com/ in your browser of choice.
4.  It will request your video input from the 360 camera, hit allow for as long as desired.
5.  Use your mouse "scroll" to zoom in or out. Hold "left click" and drag to reposition.


Inputting to OBS:
- Use the "Window Capture" source to grab the view from your browser window.
    - HINT: Most browsers allow multiple tabs of this page to be open, all grabbing the same video input, and each allowing different perspectives!
- Remember to disable "Capture Cursor," as your cursor will be used to reposition the camera.




TODO:
- Enable touch support.
- Remove visible interface to allow fully clean screen.
- Add ability to pre-set positions.
    - Hold "Shift" and click keyboard number (ex. "SHIFT+1") to set current position as pre-set.
    - Click keyboard number (ex. "1") to immediately jump to pre-set position.
