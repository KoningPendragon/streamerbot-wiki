---
title: Voice Control
description: 
published: true
date: 2022-07-15T18:24:35.511Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:33:06.759Z
---

Control **Streamer.bot** with your voice!

* [Tutorial *by Daan - Tutorials*](https://youtu.be/qnBckxzIqi0) 
{.links-list}

Leveraging the Microsoft Speech Recognition built into windows, you can add `Commands`, and use `Dictation` to add new ways to activate actions.


![voice-control-settings-018.png](/voice-control-settings-018.png)

> This function currently relies on Microsoft Voice Recognition engine. If Streamerbot is struggling to understand you please follw the steps here to train your voice. 
https://support.microsoft.com/en-us/windows/use-voice-recognition-in-windows-10-83ff75bd-63eb-0b6c-18d4-6fae94050571
You can also add your own words to the dictionary using the Windows Voice control application
https://winaero.com/manage-speech-dictionary-words-windows-10/
{.is-info}

> If the controls are unavailable make sure a supported display language is installed and available in the Speech Recogniser control panel applet
{.is-warning}

### Resources

#### How To Add Languages
> https://www.tenforums.com/tutorials/114085-add-language-windows-10-a.html

#### Change Speech Recognition Language
> https://www.tenforums.com/tutorials/120631-change-speech-recognition-language-windows-10-a.html

***

## Settings

### Auto Start Listen

Enabling this will automatically start listening when the application starts

### Locale

Set the locale of the speech recognition engine, this will report what you currently have installed within Windows

### Confidence Threshold

The minimum confidence value, 0 to 100, that will be used when deciding whether or not the spoken text will be used for a command or dictation.  Any value below this will be ignored

### Audio Input Device

Pick the audio input device to use for speech recognition, this can be changed while the engine is currently listening

### Start Listening

Will start listening to your selected audio device

### Stop Listening

Will stop listening for commands/dictation

***

## Commands
Add/edit/delete commands you would like to react to.

![voice-control-commands.png](/voice-control-commands.png)

`Name` - A friendly name for the command, this is only for user reference
`Command` - The exact string of words Streamer.bot should listen for

`Location` Valid options are `Start`,`Exact` & `Anywhere`

Location | Description
---------|------------
`Exact` | Simplest configuration, it will only trigger with a pause before and after the phrase.
`Start` | Commands require a definate pause before the trigger phrase, but they can contain additional words after it.
`Anywhere` | Commands will trigger even if the phrase is detected in the middle of a sentence

> If a command is set to `Exact`, this will be an exact grammar match, usually resulting in a much higher confidence over using dictation and the `Start` or `Anywhere` location.
{.is-info}


You can also override the global confidence level, if you want the dictation or command to maybe trigger when its less sure, or if the engine is fairly confident only.

Once a trigger phrase has been detected in anything other than `Exact` mode, Streamer.bot will record any remaining text as Dictation until the next pause. `Stop after` will stop processing any further dictation checks on the phrase that was spoken.

### Variables

Any action triggered by Voice Control will have access to the following arguments that can be used in other Sub-Actions or C# code

Name | Description
----:|:------------
`spokenText` | The full spoken phrase detected, *including the trigger phrase* 
`spokenTextConfidence` | Voice Recognition confidence raw value
`spokenTextConfidencePercent` | Confidence value as a percentage
`altPhraseText#` | 
`altPhraseConfidence#` | 
`altPhraseConfidencePercent#` | 


## Log

This tab will show you what the recognition engine is getting.

## Variables

Name | Description
----:|:------------
`spokenText` | The full spoken phrase detected, *including the trigger phrase*
`spokenTextConfidence` | Voice Recognition confidence raw value
`spokenTextConfidencePercent` | Confidence value as a percentage
`altPhraseText#` |
`altPhraseConfidence#` |
`altPhraseConfidencePercent#` |
`spokenTextInput` | Detected spoken phrase with trigger command stripped *v0.1.5+*{.version-badge} <br>(Only works with `Start` based commands)
`spokenCommand` | Detected Trigger command *v0.1.5+*{.version-badge}