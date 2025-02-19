# DeusEx GOTY Resolution and Audio Fix With some Mods
DeusEx GOTY Resolution Fix With Some Mods
How to use:

1. Install Deus EX GOTY from Steam Or GoG
2. Download the files from this repo extract somewhere
3. Launch Deus EX GOTY at least once
4. Copy/Paste contents of DeusEx DX 10 into folder C:\Program Files (x86)\Steam\steamapps\common\Deus Ex\System
5. Copy/Paste contents of DeusExe Kentjes Launcher into folder C:\Program Files (x86)\Steam\steamapps\common\Deus Ex\System
6. Copy/Paste contents of OpenAL_v2.4.7_DeusEx/OpenAL_v2.4.7_DeusEx into folder C:\Program Files (x86)\Steam\steamapps\common\Deus Ex\System
7. Launch Deus Ex again select Direct3D 10 Support in Kentje's launcher, this fixes most of lightning issues and scaling issues on Windows
8. To Fix audio issues Go C:\Program Files (x86)\Steam\steamapps\common\Deus Ex\System and select DeusEx.ini
9. Find the line  AudioDevice=Galaxy.GalaxyAudioSubsystem
10. Change the line from  AudioDevice=Galaxy.GalaxyAudioSubsystem to AudioDevice=ALAudio.ALAudioSubsystem
11. Add this block of code to the end of your DeusEx.ini
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
14. You need files from OpenAL_v2.4.7_DeusEx/OpenAL_v2.4.7_DeusEx to use the audio fix, this fixes the intro cut off issues with the original audio galaxy for Deus EX.
15. That is it, you can enjoy the Deus Ex without any other changes.
* Kentje's launcher and dx10 renderer by Kentje, OpenAL fix by Smirftsch from Oldunreal, compiled for ease of use by silentgameplays.
