# Track Chunks

## Track Count
 
Track count is a 16 bit big-endian unsigned integer. However, it should be noted that some midi parsers expect a signed 16-bit integer. This may not matter in most cases though, as few midi files use more than 12 tracks.

The following test cases are to test various track count ranges that could possibly be found in a Midi file. The test files all have blank tracks to only require reading the header and track chunks without messages getting in the way.

| Count | Hex | Description | Example |
|---:|---:|:---|:---:|
| 0 | 0x0000 | File header only (Single Track Header). | <audio src=".\tracks\empty-00000-tracks.mid" controls preload="auto"></audio> |
| 1 | 0x0001 | Single track file. | <audio src=".\tracks\empty-00001-tracks.mid" controls preload="auto"></audio> |
| 2 | 0x0002 | Minimal Multi-track file. | <audio src=".\tracks\empty-00002-tracks.mid" controls preload="auto"></audio> |
| 3 | 0x0003 |  | <audio src=".\tracks\empty-00003-tracks.mid" controls preload="auto"></audio> |
| 4 | 0x0004 |  | <audio src=".\tracks\empty-00004-tracks.mid" controls preload="auto"></audio> |
| 5 | 0x0005 |  | <audio src=".\tracks\empty-00005-tracks.mid" controls preload="auto"></audio> |
| 6 | 0x0006 |  | <audio src=".\tracks\empty-00006-tracks.mid" controls preload="auto"></audio> |
| 7 | 0x0007 |  | <audio src=".\tracks\empty-00007-tracks.mid" controls preload="auto"></audio> |
| 8 | 0x0008 |  | <audio src=".\tracks\empty-00008-tracks.mid" controls preload="auto"></audio> |
| 9 | 0x0009 |  | <audio src=".\tracks\empty-00009-tracks.mid" controls preload="auto"></audio> |
| 10 | 0x000A |  | <audio src=".\tracks\empty-00010-tracks.mid" controls preload="auto"></audio> |
| 11 | 0x000B |  | <audio src=".\tracks\empty-00011-tracks.mid" controls preload="auto"></audio> |
| 12 | 0x000C | A common number of tracks. | <audio src=".\tracks\empty-00012-tracks.mid" controls preload="auto"></audio> |
| 13 | 0x000D |  | <audio src=".\tracks\empty-00013-tracks.mid" controls preload="auto"></audio> |
| 14 | 0x000E |  | <audio src=".\tracks\empty-00014-tracks.mid" controls preload="auto"></audio> |
| 15 | 0x000F | Eight Bits. | <audio src=".\tracks\empty-00015-tracks.mid" controls preload="auto"></audio> |
| 16 | 0x0010 | Eight Bits, Plus One. A Common number of tracks. | <audio src=".\tracks\empty-00016-tracks.mid" controls preload="auto"></audio> |
| 23 | 0x0017 | Twelve Bits. | <audio src=".\tracks\empty-00023-tracks.mid" controls preload="auto"></audio> |
| 24 | 0x0018 | Twelve Bits, Plus One. | <audio src=".\tracks\empty-00024-tracks.mid" controls preload="auto"></audio> |
| 25 | 0x0019 |  | <audio src=".\tracks\empty-00025-tracks.mid" controls preload="auto"></audio> |
| 31 | 0x001F | Eight Bits. | <audio src=".\tracks\empty-00031-tracks.mid" controls preload="auto"></audio> |
| 32 | 0x0020 | Eight Bits, Plus One. | <audio src=".\tracks\empty-00032-tracks.mid" controls preload="auto"></audio> |
| 63 | 0x003F | Sixteen Bits. | <audio src=".\tracks\empty-00063-tracks.mid" controls preload="auto"></audio> |
| 64 | 0x0040 | Sixteen Bits, Plus One. | <audio src=".\tracks\empty-00064-tracks.mid" controls preload="auto"></audio> |
| 99 | 0x0063 |  | <audio src=".\tracks\empty-00099-tracks.mid" controls preload="auto"></audio> |
| 100 | 0x0064 |  | <audio src=".\tracks\empty-00100-tracks.mid" controls preload="auto"></audio> |
| 101 | 0x0065 |  | <audio src=".\tracks\empty-00101-tracks.mid" controls preload="auto"></audio> |
| 127 | 0x007F | One Nibble. | <audio src=".\tracks\empty-00127-tracks.mid" controls preload="auto"></audio> |
| 128 | 0x0080 | One Nibble, Plus one. | <audio src=".\tracks\empty-00128-tracks.mid" controls preload="auto"></audio> |
| 255 | 0x00FF | Byte Boundary. | <audio src=".\tracks\empty-00255-tracks.mid" controls preload="auto"></audio> |
| 256 | 0x0100 | Byte Plus one. If reader mistakenly reads the track count as a byte, this will fail. | <audio src=".\tracks\empty-00256-tracks.mid" controls preload="auto"></audio> |
| 511 | 0x01FF | Double of a byte. | <audio src=".\tracks\empty-00511-tracks.mid" controls preload="auto"></audio> |
| 512 | 0x0200 | Double of a Byte Plus one. | <audio src=".\tracks\empty-00512-tracks.mid" controls preload="auto"></audio> |
| 1023 | 0x03FF |  | <audio src=".\tracks\empty-01023-tracks.mid" controls preload="auto"></audio> |
| 1024 | 0x0400 |  | <audio src=".\tracks\empty-01024-tracks.mid" controls preload="auto"></audio> |
| 2047 | 0x07FF |  | <audio src=".\tracks\empty-02047-tracks.mid" controls preload="auto"></audio> |
| 2048 | 0x0800 |  | <audio src=".\tracks\empty-02048-tracks.mid" controls preload="auto"></audio> |
| 4095 | 0x0FFF | One Byte plus one Nibble. | <audio src=".\tracks\empty-04095-tracks.mid" controls preload="auto"></audio> |
| 4096 | 0x1000 | One Byte plus one Nibble, Plus one. | <audio src=".\tracks\empty-04096-tracks.mid" controls preload="auto"></audio> |
| 9999 | 0x270F |  | <audio src=".\tracks\empty-09999-tracks.mid" controls preload="auto"></audio> |
| 10000 | 0x2710 |  | <audio src=".\tracks\empty-10000-tracks.mid" controls preload="auto"></audio> |
| 10001 | 0x2711 |  | <audio src=".\tracks\empty-10001-tracks.mid" controls preload="auto"></audio> |
| 65535 | 0xFFFF | Two bytes. Maximum size for a 16 bit big-endian integer. | <audio src=".\tracks\empty-65535-tracks.mid" controls preload="auto"></audio> |
| 65536 | 0x10000 | Too large to fit in a 16 bit big-endian integer. | No example. <!-- <audio src="" controls preload="auto"></audio> --> |

## References

- [Standard MIDI Files (SMF) Specification](https://www.midi.org/specifications/item/standard-midi-files-smf)