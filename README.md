# DeusEx GOTY Resolution and Audio Fix With some Mods
DeusEx GOTY Resolution Fix With Some Mods
How to use:

1. Install Deus EX GOTY from Steam Or GoG

2. Download the files from this repo extract somewhere

3. Launch Deus EX GOTY at least once

4. Copy/Paste contents of DeusEx DX 10 into folder C:\Program Files (x86)\Steam\steamapps\common\Deus Ex\System

5. Copy/Paste contents of DeusExe Kentjes Launcher into folder C:\Program Files (x86)\Steam\steamapps\common\Deus Ex\System

6. Launch Deus Ex again select Direct3D 10 Support in Kentje's launcher, this fixes most of lightning issues and scaling issues on Windows

# 7. OpenAL AUDIO Fix Experimental Prone to Crashes at some points

* Copy/Paste contents of OpenAL_v2.4.7_DeusEx into folder C:\Program Files (x86)\Steam\steamapps\common\Deus Ex\System
* To Fix audio issues Go C:\Program Files (x86)\Steam\steamapps\common\Deus Ex\System and select DeusEx.ini
* Find the line  AudioDevice=Galaxy.GalaxyAudioSubsystem
* Change the line from  AudioDevice=Galaxy.GalaxyAudioSubsystem to AudioDevice=ALAudio.ALAudioSubsystem

# Add this block of code to the end of your DeusEx.ini without the *
* [ALAudio.ALAudioSubsystem]
* ALDevice=DefaultDevice
* OutputRate=44100Hz
* SampleRate=44100Hz
* SoundVolume=64
* SpeechVolume=64
* MusicVolume=255
* EffectsChannels=64
* AmbientFactor=0.700000
* DopplerFactor=0.010000
* UseOriginalUnreal=True
* bSoundAttenuate=True
* UseDigitalMusic=True
* MusicInterpolation=SPLINE
* MusicDsp=DSP_ALL
* MusicPanSeparation=50
* MusicStereoMix=100
* MusicAmplify=1
* EmulateOldReverb=True
* UseReverb=True
* OldReverbIntensity=0.2
* ProbeDevicesOnly=False
* UseHRTF=Enable

# The game starts crashing on Windows 11 due to OpenAL issues it is possible to set the Output and Sample Rate frequency to 48000Hz in the DeuxEx.ini 
# Another option is to reinstall the game by deleting everything in the game folder and System folder located in C:\Users\User\Documents\Deus Ex\

* OutputRate=48000Hz
* SampleRate=48000Hz

* You need files from OpenAL_v2.4.7_DeusEx to use the audio fix, this fixes the intro cut off issues with the original audio galaxy for Deus EX.

8. If the game fails to register the 1080p or whatever resolution you use and 32bit colors with kentje's launcher, it is possible to change it manually by editing the DeusEX.ini
* [WinDrv.WindowsClient]
* WindowedViewportX=1920
* WindowedViewportY=1080
* WindowedColorBits=32
* FullscreenViewportX=1920
* FullscreenViewportY=1080
* FullscreenColorBits=32

# Deus Ex Linux Fix

1. Install Deus EX GOTY

2. Dowbload this fix 

3. Copy/paste contents of DeusExe Kentjes Launcher into folder /home/username/.local/share/Steam/steamapps/common/Deus Ex/System

4. Instead of DX10 copy/paste the OpenGlDrv.dll from this fix for newer OpenGL renderer or you can leave the original DX 9 renderer it goes through Vulkan compatibility layer and is not as dark as the Windows version.

5. For best performance it is recommended to use these settings in the DeusEx.ini file for Windrv general settings and OpenGL Renderer:

* [WinDrv.WindowsClient]
* WindowedViewportX=1920
* WindowedViewportY=1080
* WindowedColorBits=32
* FullscreenViewportX=1920
* FullscreenViewportY=1080
* FullscreenColorBits=32
* Brightness=0.600000
* MipFactor=1.000000
* UseDirectDraw=True
* UseJoystick=False
* CaptureMouse=True
* StartupFullscreen=True
* CurvedSurfaces=True
* ScreenFlashes=True
* NoLighting=False
* SlowVideoBuffering=False
* DeadZoneXYZ=True
* DeadZoneRUV=False
* InvertVertical=False
* ScaleXYZ=1000.000000
* ScaleRUV=2000.000000
* SkinDetail=High
* TextureDetail=High
* Decals=True
* MinDesiredFrameRate=30.000000
* UseDirectInput=False
* NoDynamicLights=False

* [OpenGLDrv.OpenGLRenderDevice]
* ZRangeHack=False
* NoAATiles=True
* NumAASamples=4
* UseAA=True
* MaskedTextureHack=True
* SmoothMaskedTextures=True
* SceneNodeHack=True
* FrameRateLimit=120
* SwapInterval=0
* UseFragmentProgram=True
* UseVertexProgram=True
* UseCVA=False
* UseMultiDrawArrays=True
* TexDXT1ToDXT3=False
* DynamicTexIdRecycleLevel=100
* CacheStaticMaps=True
* UseTexPool=True
* UseTexIdPool=True
* UseSSE=True
* UseSSE2=True
* BufferTileQuads=True
* SinglePassDetail=False
* SinglePassFog=False
* ColorizeDetailTextures=False
* DetailClipping=False
* DetailMax=2
* RefreshRate=0
* MaxTMUnits=0
* NoFiltering=False
* MaxAnisotropy=16
* UseTNT=False
* Use16BitTextures=False
* UseS3TC=True
* UseAlphaPalette=True
* UseTrilinear=False
* UsePrecache=True
* ShareLists=False
* UsePalette=True
* UseMultiTexture=True
* UseBGRATextures=True
* UseZTrick=False
* MaxLogTextureSize=12
* MinLogTextureSize=0
* OneXBlending=True
* GammaCorrectScreenshots=False
* GammaOffsetBlue=0.000000
* GammaOffsetGreen=0.000000
* GammaOffsetRed=0.000000
* GammaOffset=0.000000
* LODBias=0.000000
* DetailTextures=True
* DescFlags=0
* Description=
* HighDetailActors=True
* Coronas=True
* ShinySurfaces=True
* VolumetricLighting=True 

6. For Sound Fix set the latency in kentje's launcher to 0, if issues occur revert latency back to 40

# Additional hidden settings for all renderers:

1. Enter chat default key is T
2. Delete say and type in preferences
3. Now you can adjust settings for all renderers like triple buffering anisotropic filtering and disable what you don't need like bloom in DX 10 renderer.

# That is it, you can enjoy the Deus Ex without any other changes.

* Kentje's launcher and dx10 renderer by Kentje, OpenAL fix by Smirftsch from Oldunreal, compiled for ease of use by silentgameplays.
