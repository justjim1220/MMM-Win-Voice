# MMM-Win-Voice

Voice Recognition Module for MagicMirror<sup>2</sup> for Windows users,
based off of the module [MMM-voice](https://github.com/fewieden/MMM-voice) by @fewieden.

## Information

Go to [Mykle1's Complete Walkthrough to install and run MM<sup>2</sup> using Windows](https://forum.magicmirror.builders/topic/4089/complete-walkthrough-install-magicmirror-on-a-pc-windows-7-10).

## Dependencies

_Latest versions of:_

* [MagicMirror<sup>2</sup>](https://github.com/MichMich/MagicMirror)
* [Git for Windows](https://git-scm.com/download/win)
* [Node.js](https://nodejs.org/en/)
* [SphinxBase](https://github.com/cmusphinx/sphinxbase)
* [PocketSphinx](https://github.com/cmusphinx/pocketsphinx)
* [PocketSphinx-continuous](https://www.npmjs.com/package/pocketsphinx-continuous)
* [lmtool](https://www.npmjs.com/package/lmtool)

* a microphone with Windows Speech Recognition turned on and configured

## Installation

1. cd MagicMirror
2. cd modules
3. git clone https://github.com/justjim1220/MMM-Win-Voice.git
4. cd MMM-Win-Voice
5. npm i

## Configuration

    ```
    {
        disabled: false,
        module: "MMM-Win-Voice",
        position: "bottom_center",
        config: {
            microphone: "RealTech High Definition Audio",
            keyword: "MAGIC MIRROR",
            timeout: 10
        }
    },
    ```

## Config Options

| **Option** | **Default** | **Description** |
| --- | --- | --- |
| `microphone` | REQUIRED | Id of microphone shown in the Device Manager in Windows Settings. |
| `keyword` | `"MAGIC MIRROR"` | Keyword the mirror starts to listen. IMPORTANT: Only UPPERCASE Letters |
| `timeout` | `15` | time the keyword should be active without saying something |

## Usage

You need to say your KEYWORD (Default: MAGIC MIRROR), when the KEYWORD is recognized the microphone will start to flash and as long as the microphone is flashing (timeout config option) the mirror will recognize COMMANDS or MODES (Keep in mind that the recognition will take a while, so when you say your COMMAND right before the microphone stops flashing the COMMAND will propably not be recognized).

### Commands

* HIDE MODULES
* SHOW MODULES
* WAKE UP
* GO TO SLEEP
* OPEN HELP
* CLOSE HELP

### Select Mode

To select a MODE, the specfic MODE has to be the first word of a COMMAND or right after the KEYWORD, while the microphone is flashing.

Mode of this module: 'VOICE'

To get the module to start listening, say: "Magic Mirror". Wait for microphone icon to show that it is 'LISTENING'. Then say "Voice", then your command.
IE: "Magic Mirror, Voice, Hide Modules".

## Acknowledgements

@fewieden for creating the voice module which gave me a base to create a voice module for us 'Windows' users (I'm pretty sure I could be the ONLY one! :P ).

@Mykle1 for his awesome 'Walkthrough' which got me started with MM<sup>2</sup> in the first place. And, even though he pushes for the use of Ubuntu, he has always been helpful whenever I had issues. ;)

@Seann for encouraging me to keep up the research and development of MM<sup>2</sup> for Windows.

@Strawberry 3.141, @cowboysdude, @sdetweil, @bhepler, & @Sean for all the help they have given me over the past couple of years. :)
