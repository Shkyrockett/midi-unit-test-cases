# Standard Midi File Format (SMF) Header

Standard Midi files start with the ASCII sequence "`MThd`" (0x4D54_6864).

## File Type

| Type# | Description | Example |
|---:|:---|:---:|
| 0 | Single Track Type Header. | <audio src=".\tracks\header-type-00-single.mid" controls preload="auto"></audio> |
| 1 | Multi-Track Type Header. | <audio src=".\tracks\header-type-01-multi-track.mid" controls preload="auto"></audio> |
| 2 | Multi-Song Type Header. | <audio src=".\tracks\header-type-02-multi-song.mid" controls preload="auto"></audio> |

## References

- [Standard MIDI Files (SMF) Specification](https://www.midi.org/specifications/item/standard-midi-files-smf)
