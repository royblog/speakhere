# SpeakHere

## 效果
![代码启动界面](https://github.com/royblog/speakhere/blob/master/screen.jpg)

## 概述
SpeakHere demonstrates basic use of Audio Queue Services, Audio File Services, and Audio Session Services on the iPhone and iPod touch for recording and playing back audio.

The code in SpeakHere uses Audio File Services to create, record into, and read from a CAF (Core Audio Format) audio file containing uncompressed (PCM) audio data. The application uses Audio Queue Services to manage recording and playback. The application also uses Audio Session Services to manage interruptions and audio hardware route changes (as described in Core Audio Overview).

SpeakHere can record using any audio recording format supported on the iPhone or iPod touch. To set the recording format, modify the argument to the SetupAudioFormat call in AQRecorder.mm.

To test the application's interruption behavior, place a phone call to the device during recording or playback; then choose to ignore the phone call.

To test the application's audio hardware route change behavior, plug in or unplug a headset while playing back or recording.

This application shows how to:

	* Set up a linear PCM audio format.
	* Set up a compressed audio format.
	* Create a Core Audio Format (CAF) audio file and save it to an application's Documents directory.
	* Reuse an existing CAF file by overwriting it.
	* Read from a CAF file for playback.
	* Create and use recording (input) and playback (output) audio queue objects.
	* Define and use audio data and property data callbacks with audio queue objects.
	* Set playback gain for an audio queue object.
	* Stop recording in a way ensures that all audio data gets written to disk.
	* Stop playback when a sound file has finished playing.
	* Stop playback immediately when a user invokes a Stop method.
	* Enable audio level metering in an audio queue object.
	* Get average and peak audio levels from a running audio queue object.
	* Use audio format magic cookies with an audio queue object.
	* Use OpenGL to indicate average and peak recording and playback level.
	* Use Audio Session Services to register an interruption callback.
	* Use Audio Session Services to register property listener callback.
	* Use Audio Session Services to set appropriate audio session categories for recording and playback.
	* Use Audio Session Services to pause playback upon receiving an interruption, and to then resume playback if the interruption ends.
	* Use UIBarButtonItem objects as toggle buttons.

SpeakHere does not demonstrate how to record multiple files, nor does it provide a file picker. It always records into the same file, and plays back only that file.
