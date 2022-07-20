# midibot
Text-controlled MIDI device and sequencer.

This takes text commands and makes a MIDI device to output the messages to your DAW or MIDI-compatible software.

Initially intended to function with a twitch/IRC bot for multi-user interactivity.

To run, install requirements.txt and run midibot/midibot.py. 

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

    Macros:

    !macro [macro name] [sequence]

    $[macroname] (this will recall the macro
    

Example commands:

    !add synth a4[4] c3[4] f2[0.5] c#4[1]

        (Specify track, note names and durations)

    !add synth c3 d3 e3 f4

        (Duration defaults to 1 if not specified)

    !add synth a2-c3-e3[4] g2-b2-d3-f3[8]

        (Chords use dashes to combine notes)

    !res 0 100 40 45
        (CC durations also default to 1)

    !cutoff loop 30[4] 100[4] 127[8]

        (Looped CC commands)

    !macro macro1 c3-c4[4]

        (Create a macro named 'macro1')

    !add synth $macro1

        (Reference the macro)