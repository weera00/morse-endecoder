# Morse EnDecoder #

My take on an Arduino-based Morse code encoder and decoder. It's a library easily integrated into any Arduino program (sketch), that consists of two classes:

  * The morseDecoder class
  * The morseEncoder class

It can also decode audible Morse code via the analog inputs.

Full duplex decoding and encoding, with different speeds if necessary, is possible. It is also possible to define more than one decoder and / or encoders.

They are non-blocking, so your code loop can do other things while en-/de-coding Morse, unless the loop takes too long to complete.

Supports the Standard International Morse code, with the addition of punctuation. But no non-english characters for now.
  * One exception to the punctuation is the dollar-sign ($), it is not incuded (as it would require a doubling of the Morse table).
  * One addition to the punctuation is the exclamation-mark (!) is represented twice, both the "MN digraph" and the "KW digraph" (from the Morse code page at wikipedia: http://en.wikipedia.org/wiki/Morse_code).
    * For encoding only the KW exclamation mark signal is used.


More details in the [Usage](Usage.md) page.

Also some other details in my blog: http://raronoff.wordpress.com/2010/12/16/morse-endecoder/