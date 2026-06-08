# How to Use the Terraform Project
Reece Dickinson, Kai Frimodig, and Trevor Troy Tumwesigye

<u>**Step 1 (installing the file):**</u>
Install the TouchDesigner file (.toe) from my github page: https://github.com/lettuce
(Yes, my username is just lettuce)

<u>**Step 2 (hardware setup):**</u>
Ensure your depth camera, preferably a Kinect or Kinect model, works properly. On the left side of the program, there is an operator titled “kinect1”, which should automatically connect to your Kinect camera. If it does not, then there is a problem with the depth feature on your camera.

<u>**Step 3 (API key creation):**</u>
Get an API key for the ai model by going to the website Daydream, visited here:
https://app.daydream.live/dashboard/api-keys
You will have to make an account with Daydream, it is free and a well-known trusted website.

<u>**Step 4 (AI diffusion setup):**</u>
Back on TouchDesigner, navigate to the purple section titled “SteamDiffusion Input-Output”, and select the node titled “StreamDiffusionTD”. Once this has been selected:
A window menu should pop up with parameters that can be adjusted. (If it does not, pressing ‘p’ on your keyboard will open it.) 
Once in this window menu, navigate to the tab named “Install”. Here, the API key you received from the previous step should be entered into the section called “DayDream Apikey”. When it says “Loaded”, then it has been loaded successfully
Now, navigate to the tab named “Settings 1”
Once in this tab, locate Start Server and press the button next to it that says “Pulse”
Now, once the server has finished starting (it may take some time), you may select the “Pulse” button next to “Start Stream” 
Wait for a bit, and it should load. You should see an ai output on screen (default has been set to a topological view of mountains and water)

<u>**Step 5 (Display setup and output):**</u>
**Note: The aspect ratio has been set to 5:3 through the node titled “res1”. If you wish to change the aspect ratio, it can be done through this node under the tab titled “Common” and through the parameter titled “Aspect”**
On the right side of the program, find the green box titled “WindowOut” and navigate to the very far right end of the box. Select the node titled “window1” and a window menu should pop up. (Again, if the window menu does not display, pressing ‘p’ should display it). Once in the menu:
Locate the parameter called “Display” inside the tab named “Window”. It should be 5 or so parameters from the top of the menu.
Think about your display setup and which display you would like the AI-processed output to be visible on. In TouchDesigner, monitors start at 0 and increase from left to right. For example, even if your main monitor is on the left, it will be listed as “Display 0”, and every monitor on the right from it will have a display number one greater than the one to the left of it
Once the proper display has been chosen, remain under the tab named “Window” and locate the section that has “Width” and “Height”. It may be grayed out, changing the parameter “Opening Size” to “Custom” will fix this. Change the Width and Height to the same dimensions as your display.
Now, navigate to the tab named “Open/Close” at the top, and locate the parameter named “Open as Separate Window”
Press “Open” to open a window on the chosen display, separate from the TouchDesigner program. If you wish to close this window, navigate to the parameter titled “Close” and press “Close”

<u>**Step 6 (optional) (Changing the prompt and AI sensitivity settings)**</u>
If you wish to alter the prompt or the settings in the AI model such as canny, depth, feedback, etc, this can be done rather simply.
At the top left corner of the TouchDesigner screen, select the tab titled “Dialogs” and then select the option titled “Window Placement”. This should open a window where three window components are listed. One of them, probably the one at the bottom, should already be open and should have the option to close it. This will close the output being displayed. The option titled “/perform/” should not be open by default, and opening it will open a window where aspects about the ai, such as the prompt and sensitivity settings can be adjusted. This window can be dragged so it does not overlay the output on the display. Selecting stop will cause the ai to stop functioning until it is started again. Starting the AI will take some time for it to boot up again.
