# FormCalibration
Calibration Tests For the Formlabs Form1+

# Manual Galvo Calibration

At this time, the following procedure requires a Windows PC because the tools I've created are Windows Executables.

1) Connect your Form 1+ to your PC via USB.
2) Download and install the OpenFL version of Preform on your Windows PC: https://s3.amazonaws.com/FormlabsReleases/Release/2.3.3/PreForm_setup_2.3.3_release_OpenFL_build_2.exe
3) Download and run Zadig: https://github.com/pbatard/libwdi/releases/download/b730/zadig-2.5.exe
  A) Select the Options Menu at the top of the window, and ensure that "List All Devices" has a check mark next to it.
  B) Select the drop down in the upper center of the window, and select "Form1" from the list.
  C) In the center of the screen to the right of the green arrow there is a selection box, click the down arrow button next to the selection box until the "libusbK (v3.0.7.0)" option is selected.
  D) Click the Replace Driver button and wait for the "The Driver was Installed Successfully" message.
  E) Close Zadig (you can delete it from your PC now if you want to).
4) Install a clean/empty vat and a clean build plate in the Form 1+
5) Cut a piece of white paper and trim so that fits inside the vat, covering the entire print area. It needs to be larger than the build plate and lay flat in the bottom of the vat.
5) Download the OpenFL executables: https://github.com/opensourcemanufacturing/OpenFL/releases/download/0.01/OpenFL_Executables.zip
6) Unzip OpenFL Executables and run "Z_Jog_052320.exe" (please wait - it may take a moment for the application to start, this is normal)
  A) Select the "5 milimeter" radio buttom
  B) Click the "Z Down" button until the build plate is close to the vat. You can then use the 1mm setting to move the build plate closer to the paper, you only need it to be close enough that you can trace the shape of the build plate onto the paper.
  C) Trace the outline of the build plate onto the paper.
  D) Press the "Home All" button.
  E) Once the homing sequence finishes, Press the "Exit" button.
  F) Without removing the paper and without shifting it's position in the vat, carefully measure and draw a line across the center of the build plate outline from side to side and another line from front to back. You can use a strip of paper to find the center point (see the pictures below).
  G) leave the paper in the vat for the rest of the process.
7) Run the Preform software you installed in Step 2 (if it is currently running, it is a good idea restart it)
  A) Open the Printers Window (select File > Printers), expand your printer and run the firmware update process.
  B) Download and open the Galvo Calibration STL: https://github.com/opensourcemanufacturing/FormCalibration/blob/master/Form%201%2B%20Galvo%20Calibration.stl
  C) Download the  
