# Game and Engine for Windows <br> (Currently private, avaliable upon request)

---
<img width="2378" height="1330" alt="game_snap_3" src="https://github.com/user-attachments/assets/387861cb-f5da-4b6a-9c4a-eed45cef4de3" />
<img width="2376" height="1337" alt="game_snap_1" src="https://github.com/user-attachments/assets/b86302ea-63c8-4f89-be07-f11aed3b67fd" />
<img width="2377" height="1342" alt="game_snap_4" src="https://github.com/user-attachments/assets/23487012-c53b-4c9b-a5e6-cf4325909bbf" />

## How to Run

Run the `build.bat` file in the project root, then execute `win32.exe`

---

## How to Play
Use the arrow keys to move the triangle player around

Npc triangles will spawn every so often and follow the player

---

## Features (this list is frequently out of date)

- Creates a basic Win32 window with a message pump and callback handler
- Custom memory allocator using an arena built on top of `VirtualAlloc`
  - Supports memory alignment to an arbitrary byte boundary
- Plays a sine wave using XAudio2  
  **Note**: Audio is muted by default. To enable it, remove the `#if` guard on `SourceVoice->Start();` or add `/DAUDIO_PLAYING` to the build batch file.
- File I/O system  
  - Currently writes `"hello!"` to a test file as a demonstration
- Initializes OpenGL on Windows
  - VAO, VBO, and EBO setup  
  - Runtime shader compilation with error checking  
  - Pre-multiplied alpha blending  
  - Nearest-neighbor texture filtering
- Polling user input using `GetAsyncKeyState`
- 2D rotation
- Lighting
- AABB collision detection, using Minimum Translation Vector resolution.
- Minimal entity system
- NPCs that track the player
- Separation between platform and game code for future cross-platform integration
- Particle system
