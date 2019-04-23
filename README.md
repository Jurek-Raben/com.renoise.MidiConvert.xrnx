# com.renoise.MidiConvert.xrnx
Extended midi export for R3.1.1

Here is another test version of export.lua. All new features:

- midi control device automation support -> MIDI CC 21 - 31 (max. 10 parameters)
- instr. automation device support -> MIDI CC 103 - 113 (max. 10 parameters)
- pattern midi pitchbend
- pattern midi pitchbend -> MIDI CC 20 (for DAWs not supporting pitchbend import…)
- pattern channel aftertouch
- pattern channel aftertouch -> MIDI CC 102 (for DAWs not supporting pressure import…)
- sequence slot mute support
- sequence slot mute -> note off support
- corrected LPB
- Track names also contain Renoise track names
- Numbering is now in Hex
- Sequence comments -> marker support (buggy, actually didn’t find a DAW supporting it at import)
- Actual midi channel used now
- Instr.-/midi-/plugin-transpose support
- You can copy the automation from the imported MIDI CC lane to the correct VSTi’s automation lane then. Try to end all notes with note-off somewhere at least. You also can use a following muted slot.

Keep in mind the following limitations:

- Only use one instrument per track
- Always use only one midi control device and one instr. automation device per instrument
- Put the devices always onto the track where the instrument plays
- Max. 10 automated parameters in automation devices, position doesn’t matter
- Always start with the first instrument at position 00, don’t leave an instrument slot empty

It may be buggy or install a trojan horse.
