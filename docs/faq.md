## OBS

- I don’t know how to use this with OBS!  
  Open your model under FIles > Open  
  Set BG Color at the Top Bar to Transparent  
  Set Mode at the Top Bar to PNGTube  
  Add Game Capture in OBS  
  Allow transparency in Game Capture options  
  Capture PNGTube Remix  

## Audio

- My mic doesn’t seem to be picking up no matter what I do?  
  This is a problem with Godot and picking up microphones with more than  
  two channels, not sure what can be done outside of maybe faking a 2  
  channel mic with an application like Voicemeeter Banana.  
  (Note: a custom microphone input extension was made to counter this.  
  Please make sure to use the latest version.)

- I’m trying to set up Advanced Lip Sync and there is only one phoneme…  
  In the lip sync config tab, go to Files > New File in the top right corner  
  and then Files > Save to save it over the broken default one.  

- How do I record sounds for Advanced Lip Sync?  
  Add a new recording slot with the Plus symbol.  
  Then press and release the mic icon, it will record  
  for a split second after it is released.  
  Make sure you only record the viseme and not the  
  surrounding parts of the example words,  
  some sounds will be hard but just do your best. 

- My mouth isn’t opening and closing properly! (Includes Advanced Lip Sync)  
  Most commonly this is a problem with the audio settings you have,  
  make sure you have the mic you’d like to use selected and fiddle with  
  the volume sensitivity and threshold inside of the volume bar until you have the desired effect.  

## Limitations

- I opened up an image/model and there’s a giant black square!  
  Remix seems to have different limits for image sizes depending on your   
  computer, this is especially apparent for giant image files like if you  
  didn’t crop the empty space from your sprite sheets. Keep this in mind when  
  creating a model for another person.  
  Please check [Atlas](atlas) to understand how things work.

- I can’t seem to use hotkeys on Linux when Remix isn’t focused! (Steam Deck runs on Linux)  
  Wayland (The protocol used for handling stuff like hotkeys on Linux)  
  doesn’t currently allow for global inputs without some editing due to  
  security reasons (or it might just not work at all.)  
  You can try enabling Legacy X11 App Support or launching the program with Xwayland.  
  If input still doesn't work, make sure to add the software to Input Group.

- Clipping isn’t working properly!  
  Clipping is done through objects that are parent-child and  
  the child MUST have Z-order value of 0 (It’s near the top of the properties tab.)  
  Remember that the last object attached to the parent will appear in front of the others.  
  You also can’t clip something to a clipped object.  

## Misc

- I can’t unparent an object!  
  Drag it to the model folder at the top of the sprite list.  

- My sprite sheet frames are cutting into each other!  
  To function as spritesheets, each frame of your animation must  
  have the same amount of space allocated to it. Otherwise the  
  frames will cut into each other! Use frames of uniform size and  
  if you must, use an online texture packer.  

- How big should I make my images for the model?  
  Try to think of the scale you’ll be using your model in,  
  no point in making a 4k model if you’re only streaming in 720p.  
  Try not to go overboard either or you can run into issues with performance  
  or if they’re really big, the black box glitch. If you’re still struggling to decide  
  a canvas size of around 1000-2000 px is a decent place to start.  