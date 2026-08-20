# Official Shadeinator Guide (ENG ONLY)
Last Updated: **17/08/2026**

# 1 - Instalation
- Unzip the zip file into you addons folder
- it should look like this:

![Mi imagen](./images/guide/preview.png)

IMPORTANT:
- DO NOT CHANGE THE FOLDER NAME OF THE ADDON (Shadeinator)
- You must use an action build version, you can get one [HERE](https://codename-engine.com/) (In the experimental builds part)\
Just click on the button of you operative system

![Mi imagen](./images/guide/cnepage.png)

- This is still in porgress so bugs are expected. bugs, questions and feedback on gamebanana or in the [Discord Forum](https://discord.com/channels/860561967383445535/1535923867896254494)

# 2 - Entering the editor
- Before entering the editor, you can adjust some settings in the options menu, such as the language:

![Mi imagen](./images/guide/optionsmenu.png)

- To enter the editor, simply press 7 (or use the developer menu keys) in the main menu and select the "SHADEINATOR V4" option:

![Mi imagen](./images/guide/editorpicker.png)

- Then... do I really have to explain this?
  - Editor: Enter the editor.
  - Scripts Folder: Opens the folder of the scripts you made.
  - CNE Server: A link to the official Codename Engine Discord server.

![Mi imagen](./images/guide/shadeoptions.png)

# 3 - Top menu options

![Mi imagen](./images/guide/topoptions.png)

- ## 3.1 - Shader 

![Mi imagen](./images/guide/shaderoptions.png)

---

- ### 3.1.1 Load Shader:
Allows you to load a saved preset shader

![Mi imagen](./images/guide/shaderload.png)

---

- ### 3.1.2 Import from:
 Allows you to import a preset from a txt file or a shader code

![Mi imagen](./images/guide/shaderimport.png)

---

- ### 3.1.3 Saver shader as:
 Allows you to save the current shader as a preset

![Mi imagen](./images/guide/shadersave.png)

---

- ### 3.1.4 Delete Shader:
 Allows you to delete a shader preset

![Mi imagen](./images/guide/deletepre.png)

---

- ### 3.1.5 Make Script:
 Allows you to make a script to use the current shader 
 - StrumLines ID: Strumlines that will be affected
 - Characters ID: Character in the strumLines that will be affected
 - File Name: Name of the script file\
 (The script file will be in **Shadeinator/scriptsMaked/**)

![Mi imagen](./images/guide/makescript.png)

- ## 3.2 Character
Change the current character in the editor to see how your shader looks on other character colors

![Mi imagen](./images/guide/chars.png)

- ## 3.3 HUD (Useless)
Basically Just a Green Screen

![Mi imagen](./images/guide/hudopt.png)
![Mi imagen](./images/guide/greenscr.png)

---

# This section may be the longest and most important one so please read carefully

- ## 3.4 - Edit 
Allows you to change between what thing are you changing from the shader

![Mi imagen](./images/guide/editsec.png)

- ### 3.4.1 Editing Top Mask Color:
The top mask color is an extra layer of color that goes above the current sprite.\
This can be useful for making effects a little more visible.

- For example, Lets say that I want a warm tome like orange, i could use these settings
- Each slider represents the intensity of a color. For example, you can make red stronger than green to get an orange tone. The alpha slider is the most important one because if it is set to 0, the top mask will not be visible.

![Mi imagen](./images/guide/topmask1.png)

Explanation:
- Red (1): This is to make sure that the light is from the correct color
- Green (0.5): This is to get the orange tone but without getting too yellow
- Blue (0): We don't need blue here
- Alpha (0.4): This is to make sure it is slightly visible but without being too strong

Or if You want something stronger you could use this

![Mi imagen](./images/guide/topmask2.png)
- Do you notice how there is more alpha and green?\
That is what is making it stronger or more visible

---

### 3.4.2 Editing Sprite Color:
Unlike the top mask, the sprite color directly modifies the base color of the sprite. We can use this to highlight effects without having to use another layer.

- Red, Green, Blue (RGB): Adjusts the intensity of each color channel to tint the sprite.
- Alpha: Controls the vibrancy strength of the color effect.

For example, if you increase the Alpha while keeping Red, Green, and Blue at 0, the sprite will look dark or completely black because it's applying zero color intensity to the base sprite texture:

![Mi imagen](./images/guide/spritecol1.png)

Conversely, if you leave the Alpha at 0 but move the RGB sliders, nothing will happen because there is no Alpha intensity to reflect those color changes.

![Mi imagen](./images/guide/spritecol2.png)

By balancing these colors properly, we can also create effects like warm lighting or custom color tones:

![Mi imagen](./images/guide/spritecol3.png)

- Red (1): Kept at maximum to anchor the warm red base
- Green (0.75): Slightly reduced, which helps blend into a softer, warmer look
- Blue (0.5): Lowered further to reduce cool tones, shifting the overall color palette toward a warm, sunset-like lighting
- Alpha (1): Fully opaque, ensuring the custom color tint is completely applied to the sprite

---

- ### 3.4.4 - Light Parameters (Early)
Before you can see any changes in the light color, you must first configure the parameters here to make the light effect visible.

For the moment just set these settings, I'll explain them later:

![Mi imagen](./images/guide/lightparameters.png)

---

- ### 3.4.3 - Editing Light Color
Now, thanks to the previous parameters, the light effect will be visible when you move the color sliders. 

- These work just like the **Top Mask Color**, but specifically for the light source.
- If you notice that bright white light wrapping around the character, it's because all the RGB sliders (Red, Green, Blue) are set to maximum (1), mixing together to create white light:

![Mi imagen](./images/guide/lightcolor.png)

- Just like before, you can lower specific color channels or adjust the Alpha to change the color and intensity of the lighting effect to fit your style.

For example, if we set the sliders like this, we can create a nice orange lighting effect:

![Mi imagen](./images/guide/lightcolor2.png)

- Red (1): Left at maximum to maintain a strong warm base.
- Green (0.75): Set slightly lower to give it that distinct orange tint.
- Blue (0): Completely turned off to remove any cool tones.
- Alpha (1.5): Boosted to make the orange light glow stronger and stand out more.

- ### 3.4.4 - Light Parameters
Please read this section carefully.

Ok yeah, the light is good, but it's kinda boring. However, we can change that with the Light Settings

---

- #### 3.4.4.1 - Angle
Self-explanatory: changes the angle of the light so you can modify where it is coming from.

- 225 angle:

![Mi imagen](./images/guide/lightoptions.png)

- 45 angle:

![Mi imagen](./images/guide/lightoptions2.png)

---

- #### 3.4.4.2 - Size
Controls the size (or range) of the light effect. A higher value will spread the light further across the sprite.

- Size of 3:

![Mi imagen](./images/guide/lightsize1.png)

- Size of 10:

![Mi imagen](./images/guide/lightsize2.png)

---

- #### 3.4.4.3 - Layer Count
Controls how many layers the light effect has. You can definitely notice the difference!

- 1 Layer:

![Mi imagen](./images/guide/lightcount1.png)

- 5 Layers:

![Mi imagen](./images/guide/lightcount2.png)

---

- #### 3.4.4.4 - Layer Spacing
Changes the distance or separation between each of the light layers.

- 10 Spacing:

![Mi imagen](./images/guide/lightspacing1.png)

- 5 Spacing:

![Mi imagen](./images/guide/lightspacing2.png)

---

- ## 3.4.5 - Sprite Settings
This section allows you to adjust global visual properties of the sprite:

![Mi imagen](./images/guide/spriteset.png)

- #### 3.4.4.1 - Hue Rotation
Shifts the entire color spectrum of the sprite, changing its overall color theme.

Example of 50

![Mi imagen](./images/guide/spriteset1.png)

---

- #### 3.4.4.2 - Saturation
Controls how intense or washed out the colors look.

Example of 50

![Mi imagen](./images/guide/spritesat1.png)

Example of -50

![Mi imagen](./images/guide/spritesat2.png)

---

- #### 3.4.4.2 - Brightness
Makes the sprite lighter or darker.

Example of 50

![Mi imagen](./images/guide/spritebri1.png)

Example of -50

![Mi imagen](./images/guide/spritebri2.png)

---

- #### 3.4.4.2 - Contrast
Adjusts the difference between the dark and light areas of the sprite to make it pop more.

Example of 50

![Mi imagen](./images/guide/spritecon1.png)

Example of -50

![Mi imagen](./images/guide/spritecon2.png)

---

# Final Words
That's it for the guide! I really hope this helps you get started. Please be patient with me if some parts felt a bit confusing—I'm not always the best at explaining things, but I'm doing my best to make this tool accessible for everyone.

If you have any questions, feedback, or suggestions, feel free to reach out on the [Discord Forum](https://discord.com/channels/860561967383445535/1535923867896254494). Happy shading!
