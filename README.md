# Gnaural (Web)

Free, open-source binaural beats generator for the modern web, inspired by the original Gnaural project on SourceForge and updated as a pure HTML5/JavaScript web application.

---

## Overview

Gnaural (Web) is a browser-based binaural beats generator that runs entirely client-side using standard web technologies:

- HTML5
- CSS
- JavaScript
- Web Audio API

No plugins, no Java, no frameworks are required. You can open the app directly in a modern browser or host it on any static web server.

Use it for:

- Meditation and relaxation
- Focus and study sessions
- Sleep and power naps
- Experimentation with brainwave entrainment

Warning: Binaural beats are an experimental technique and not a medical treatment. Nothing in this project should be considered medical advice. Use at your own risk and always keep listening volumes at safe levels.

---

## Features

- Runs entirely in the browser
  - No server-side processing
  - No external dependencies beyond standard browser APIs

- Binaural beat synthesis
  - Independent left and right channel frequencies
  - Time-varying carrier and beat frequencies

- Session editor
  - Create, edit, and delete segments defining frequency changes over time
  - Set durations, start/end frequencies, and envelopes (fade in / fade out style behavior)
  - Reorder segments to customize the progression of a session

- Presets and persistence
  - Save sessions to XML files
  - Load sessions from previously exported XML
  - Import of classic Gnaural schedule formats

- Audio controls
  - Master volume control
  - Start, pause, and stop controls
  - Optional background noise (white/pink/brown noise)
  - Optional environmental noise

- Modern web UI
  - Responsive layout suitable for desktop and mobile
  - Built with plain HTML, CSS, and JavaScript

---

## Relationship to the Original Gnaural

This project is inspired by the original Gnaural desktop/Java software and aims to bring similar functionality to the modern web platform.

Key points:

- Conceptually similar:
  - Time-based schedules for controlling frequencies and volumes
  - Presets for different mind states and soundscapes
- Technically different:
  - Implemented in JavaScript using the Web Audio API
  - Designed for in-browser use without additional requirements

This project is not an official port or product of the original Gnaural developers and is not endorsed by them.

---

## Getting Started

### Running from a local folder

You can run Gnaural (Web) directly as a static site:

1. Clone or download this repository.
2. Open `index.html` in a modern browser.

However, for full functionality (especially if your browser restricts some APIs for `file://` URLs), it is recommended to serve the files via a local HTTP server.

For example, using Python 3:

```bash
cd gnaural-web
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

in your browser.

### Browser requirements

- A modern browser with support for:
  - Web Audio API
  - JavaScript ES6 (or later)
- Stereo headphones or earbuds for proper binaural effect

---

## Usage

1. Connect stereo headphones.
2. Open the application in your browser.
3. Load a preset or create a new session:
   - Define one or more segments.
   - For each segment, specify duration and frequency parameters.
4. Press Play to start the session.
5. Adjust the volume to a safe and comfortable level.
6. Optionally export your session to a JSON file for later use or sharing.

Typical brainwave ranges used in binaural beat sessions (for reference only):

- Delta:    about 0.5 to 4 Hz (often associated with deep sleep)
- Theta:    about 4 to 8 Hz (often associated with drowsiness or light meditation)
- Alpha:    about 8 to 12 Hz (often associated with relaxed wakefulness)
- Beta:     about 12 to 30 Hz (often associated with alertness and active thinking)

A binaural beat is created by playing slightly different pure tones in each ear. For example, 200 Hz in the left ear and 208 Hz in the right ear produce an 8 Hz beat.


---

## Roadmap (Suggestions)

Some possible enhancements:

- Session share links (encode session data in URL or use a separate storage backend, if desired).
- Accessibility improvements (keyboard navigation, ARIA labels, reduced-motion options).

---

## Contributing

Contributions are welcome.

1. Fork this repository.
2. Create a branch for your changes:

   ```bash
   git checkout -b feature/my-change
   ```

3. Make and test your modifications.
4. Commit with a clear message describing your change.
5. Open a pull request describing:
   - What you changed
   - Why you changed it
   - Any impact on existing behavior

Please keep changes focused and small where possible. For large or architectural changes, consider opening an issue first to discuss design options.

---

## License

By default, this repository assumes:

```text
SPDX-License-Identifier: GPL-3.0-or-later
```

Additional licenses:
**Gnaural:** GPL-2, Bret Logan, [sourceforge.net/projects/gnaural](https://sourceforge.net/projects/gnaural/)
**Blanket:** GPL-3, Rafael Mardojai, [github.com/rafaelmardojai/blanket](https://github.com/rafaelmardojai/blanket)

### Sounds

| Sound                                                                 | Author        | Editor*       | License       |
| --------------------------------------------------------------------- | ------------- | ------------- | ------------- |
| [Birds](https://freesound.org/people/kvgarlic/sounds/156826/)        | kvgarlic      | Porrumentzio  | CC0           |
| [Boat](https://freesound.org/people/Falcet/sounds/439365/)           | Falcet        | Porrumentzio  | CC0           |
| [City](https://freesound.org/people/gezortenplotz/sounds/44796/)     | gezortenplotz | Porrumentzio  | CC BY         |
| [Coffee Shop](https://soundbible.com/1664-Restaurant-Ambiance.html)  | stephan       | -             | Public Domain |
| [Fireplace](https://soundbible.com/1543-Fireplace.html)              | ezwa          | -             | Public Domain |
| [Rain](https://freesound.org/people/alex36917/sounds/524605/)        | alex36917     | Porrumentzio  | CC BY         |
| [Summer night](https://soundbible.com/2083-Crickets-Chirping-At-Night.html) | Lisa Redfern  | -             | Public Domain |
| [Storm](https://freesound.org/people/digifishmusic/sounds/41739/)    | Digifish music| Porrumentzio  | CC BY         |
| [Stream](https://freesound.org/people/gluckose/sounds/333987/)       | gluckose      | -             | CC0           |
| [Train](https://freesound.org/people/SDLx/sounds/259988/)            | SDLx          | -             | CC BY 3.0     |
| [Waves](https://freesound.org/people/Luftrum/sounds/48412/)          | Luftrum       | Porrumentzio  | CC BY         |
| [Wind](https://freesound.org/people/felix.blume/sounds/217506/)      | felix.blume   | Porrumentzio  | CC0           |

*Editor column refers to the Blanket project curators who trimmed/processed the original recordings.
