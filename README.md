# PS4-Ancestors-Offsets_v1.01
These are offsets that I obtained using PS4 Cheater for Ancestors: The Humankind Odyssey. I decided to post them myself since I didn't see anyone else posting an offset list for this game in particular. This list includes additional offsets such as Neural Energy, Dopamine, Reinforcement points, etc. I am currently trying to find the offsets for the rest of the Protection bar.

Please note that these offsets include the base address 0x400000.

**Neural Energy**
- Outside Evolve Screen:
  - Offsets: 1007331E6C, 1007331E68
  - Type: float
  - Segment: (NoName)eboot.bin[6]-33-10300000000

- Inside Evolve Screen:
  - Offset: 10342D9BF4
  - Type: float
  - Segment: (NoName)eboot.bin[6]-33-10300000000

**Dopamine Levels**
- Offset: 10284F4B18
  - Type: float
  - Segment: (NoName)eboot.bin[5]-33-1028000000
- When dopamine is modified, this assembly instruction gets called:
  ```asm
  vmovss dword ptr [rbx+0x1228], xmm0 ; where xmm0 is the new dopamine value
  ```
