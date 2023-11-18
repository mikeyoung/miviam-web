# MiViAm 2.0
#### Video Demo:  https://youtu.be/mNCxTsWdmJI
#### Description:
MiViAm 2.0 is a web app version of the classic and no longer available iOS app "MiViAm".

MiviAm also made a brief appearance as a Chrome App but is no longer available.

The goal of this project was to make a regular web app that can live in any environment that has any browser.

The web app version runs in all major browsers and is very light on network and local resources.

MiViAm uses sound samples from a Mellotron and a Fender Rhodes electric piano to produce an endless sequence of relaxing notes which play over a bed of ambient vinyl LP surface sound. Since MiViAm produces unique sequences which will not repeat there is no pattern to focus on and tire of. The frequency of the chimes can be set and each instrument can be turned on or off.

Audio formats for all major browsers are included.

Future versions will remove jQuery dependencies and use vanilla javascript.  While there are some functions that manually keep certain settings "bound" to variables, it is simple enough at this scale that it seemed like overkill to introduce a build step and use React or Vue.  Future versions may also introduce chord progressions, utilizing standard chord wheel patterns.  With time there may eventually be an Android version!  When these enhancements emerge it will likely be a good time to refactor as a React app in order to keep settings and UI bound tightly.  Ultimately though would like to keep it in vanilla JS just to minimize dependencies and security risks introduced with underlying libraries.

For now the logic to maintain the rate of chime playback depends on the chimes being under a certain default length.  This proved to be a simpler solution to handling the audio queue than detecting completion of playback of each event.  The events for audio start and completion were not firing dependably during testing.  A future version will likely utilize a library that can better track the start and finish of playback on multiple elements.

Please feel free to extend or totally change this code as it is still in its infancy.  The original spirit is to be ambient with no rhythm or pattern.

The Mellotron sounds were sourced from the GForce Mellotron VSTi.  They did an incredible job with that instrument and deserve most of the credit for how nice the tones are.  Future versions might include a larger sampling from the Mellotron library.  Note that each sound was EQ'd to favor midrange and compressed so that they occupy the same area of frequencies.  If you wish to add new sounds to the library, keep in mind that you might want to replace the defaults altogether if you want a broader dynamic range - or compress the added sounds in accordance with the above style.  The Mellotron out of the box already has much of the high and low end rolled off - a quality which was probably not by design but by limitation of the original hardware.

There is a sleep timer function which will turn off the tones after 60 minutes.

There is an alarm function that will start the tones at the given time (in 24 hour format).

The web app uses cookies to retain the last settings.  If any of this is not working, please let me know.  Thanks!

Right now the layout is set to scale well across multiple devices and screens therefore there are no css breakpoints or usage of Bootstrap.  The elements are centered and scaled in proportion to the client's screen.
