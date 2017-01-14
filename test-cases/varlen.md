# Variable Length Quantities

The maximum byte length of a variable length value in Midi is 5 bytes, to be represented in the file within a 4 byte 32-bit integer.

[http://www.fileformat.info/format/midi/corion.htm](http://www.fileformat.info/format/midi/corion.htm)
0FFFFFFF==268435455

16 bit value = 65536

25 bit value = 16777216

32 bit value = 268435455

| Description | File |
|---|---|
| A binary blob of valid integer values in variable length format in assending order. | [ordered-variable-length-integer-values](ordered-variable-length-integer-values.bin) |
| A Binary blob of valid integer values in static little-endian format in assending order. | [ordered-static-length-integer-values](ordered-static-length-integer-values.bin) |

## References

- [Standard MIDI Files (SMF) Specification](https://www.midi.org/specifications/item/standard-midi-files-smf)