# FormCalibration
Calibration Tests For the Formlabs Form1+

# Galvo Alignment Verification

# Never look look inside the Form 1+ when the laser is on. Never run the laser with the orange cover open. Wear appropriate PPE (personal protective equipment). Protect your eyes. Proceed at your own risk!

At this time, the following procedure requires a Windows PC because the tools I've created are Windows Executables.

1) Remove the rear panel of your Form 1+
2) Connect your Form 1+ to your PC via USB.
3) Download and install the OpenFL version of Preform on your Windows PC: https://s3.amazonaws.com/FormlabsReleases/Release/2.3.3/PreForm_setup_2.3.3_release_OpenFL_build_2.exe
4) Download and run Zadig: https://github.com/pbatard/libwdi/releases/download/b730/zadig-2.5.exe
  A) Select the Options Menu at the top of the window, and ensure that "List All Devices" has a check mark next to it.
  B) Select the drop down in the upper center of the window, and select "Form1" from the list.
  C) In the center of the screen to the right of the green arrow there is a selection box, click the down arrow button next to the selection box until the "libusbK (v3.0.7.0)" option is selected.
  D) Click the Replace Driver button and wait for the "The Driver was Installed Successfully" message.
  E) Close Zadig (you can delete it from your PC now if you want to).
5) Install a clean/empty vat and a clean build plate in the Form 1+
6) Cut a piece of white paper and trim so that fits inside the vat, covering the entire print area. It needs to be larger than the build plate and lay flat in the bottom of the vat.
7) Download the OpenFL executables: https://github.com/opensourcemanufacturing/OpenFL/releases/download/0.01/OpenFL_Executables.zip
8) Unzip OpenFL Executables and run "Z_Jog_052320.exe" (please wait - it may take a moment for the application to start, this is normal)
  A) Select the "5 milimeter" radio buttom
  B) Click the "Z Down" button until the build plate is close to the vat. You can then use the 1mm setting to move the build plate closer to the paper, you only need it to be close enough that you can trace the shape of the build plate onto the paper.
  C) Trace the outline of the build plate onto the paper.
  D) Press the "Home All" button.
  E) Once the homing sequence finishes, Press the "Exit" button.
  F) Without removing the paper and without shifting it's position in the vat, carefully measure and draw a line across the center of the build plate outline from side to side and another line from front to back. You can use a strip of paper to find the center point (see the pictures below).
  G) Leave the paper in the vat for the rest of the process.
  H) Remove the build platform for the rest of the process.
9) Download and unzip the galvo calibration files: https://github.com/opensourcemanufacturing/FormCalibration/releases/download/0.01/Galvo.Calibration.Files.zip
10) Run the Preform software you installed in Step 3 (if it is currently running, it is a good idea restart it)
  A) Open the Printers Window (select File > Printers), expand your printer and run the firmware update.
  B) Open the "Fine Tuning" window and make sure your X/Y Offsets are both set to 0.00mm.
  B) Open the Printer Settings (lower right corner of Preform). Ensure that the Form 1+ option is selected, then click "Load Custom Material..." and select the "GalvoCalibration.ini" file from the Galvo Calibration files you downloaded in Step 8.
  C) Make sure the cover is closed on your Form 1+, then open and print the "GalvoCalibrationModel.form" file you unzipped in step 8.
  D) Observe the pattern of the cross that is drawn by the galvonometers. It should cross the center of the build plate outline you drew in Step 7; if the alignment is off, continue below.
  
# Never look look inside the Form 1+ when the laser is on. Never run the laser with the orange cover open. Wear appropriate PPE (personal protective equipment). Protect your eyes. This involves putting your hands inside of a piece of equipment that is energized with electricity. Proceed at your own risk!

# Galvo adjustment - Keep the cover closed!

1) While the printer is turned off (or paused - be smart about this), loosen the cap screw the galvo you intend to adjust. Position the printer so you cannot see inside the rear cover, and carefully hold the body of the galvo with one hand.
2) With your other hand press the button to unpause the print job. As the pattern is printed, slowly and carefully rotate the body of the galvo until the axis is aligned with the lines you drew in the vat.
3) When you are satisfied with the alignment of that axis, turn off the printer (or pause it - be smart about this) and tighten the cap screw for that galvo. 
4) Repeat steps 1-3 for the other axis, if necessary.
5) Congratulations, you've manually adjusted your galvos!
