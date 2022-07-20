# midibot
Text-controlled MIDI device and sequencer.

This takes text commands and makes a MIDI device to output the messages to your DAW or MIDI-compatible software.

Initially intended to function with a twitch/IRC bot for multi-user interactivity.

The function 'recieve_message' will take a command string, and if valid, send the relevant MIDI message. It will also return a string with relevant information to pass back to the user.

Commands and Track Names are defined in the .ini files within /settings

Pre-defined Commands:
    Sequencer:
    !add [track name] [sequence]
    !replace [track name] [sequence]
    !choice [track name] [sequence]
    !rand [track name] [sequence]
    !apend [track name] [sequence]
    !clear or !reset
    !bpm [value]
    !help