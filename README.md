# Seamless Video Loop Creator

A browser-based tool for creating audio-reactive visuals and exporting them as seamless MP4 videos. No build step or account is required.

**GitHub Pages:** [https://sulqwerty.github.io/seamless-video-loop/](https://sulqwerty.github.io/seamless-video-loop/)

## Features

- Load an audio track and preview playback, looping, and real-time audio processing.
- Customize audio mastering presets and playback controls.
- Create audio spectrum visualizations with adjustable frequency range, band count, scale, position, sensitivity, spacing, gradient, glow, and pulse effects. Includes multiple spectrum styles and wireframe wave/mesh styles.
- Add image or video backgrounds, including MP4 and MOV, and loop background video to match the audio.
- Add image overlays, a draggable logo/watermark, and draggable title or subtitle text. Adjust scale, position, opacity, color, stroke, alignment, and font. Fonts include Google Fonts and fonts installed on your computer.
- Add lyrics, synchronize lines to playback, and style their font and appearance.
- Export the canvas and configured audio to MP4 with render progress, when the browser supports the required encoders.
- Save and load the application configuration as JSON, including background, overlay, and logo image data.
- Choose English or Indonesian and use Auto, Light, or Dark theme. Language and theme choices are remembered in the browser.
- Drag and drop supported files onto their file input areas.

## Run locally

Python 3 is required. From the project folder, run:

```bash
python run.py
```

On Windows, you can also use:

```powershell
py run.py
```

The script starts a temporary HTTP server on your computer and opens the app in your browser. If it does not open automatically, use the `http://127.0.0.1:...` address printed in the terminal. Press **Ctrl+C** to stop the server.

Serving the app this way lets the browser load the language files. For the language selector and translations to work reliably, use this local server or the GitHub Pages link instead of opening `index.html` directly.

## Local processing and privacy

Audio, images, videos, lyrics, and configuration files are processed in your browser. The app does not upload your media or saved configurations to GitHub or another application server. The local Python server only serves the app files to your own browser; it does not receive the media you select.

The app uses browser-side libraries, icons, and fonts delivered through CDNs. An internet connection is needed to fetch these assets the first time (or when they are not cached). After the assets have been cached, the app's media processing remains local and can work without sending media online. A fresh, uncached installation is not guaranteed to start completely offline.

## Opening the HTML file directly

Opening `index.html` with a `file://` URL can prevent the browser from loading files in the `lang/` folder because of browser security restrictions. As a result, the language catalog may fail to load and some labels can remain in their original language or fall back to English. This does not mean media is uploaded. Run `python run.py` to avoid this language-loading limitation.

## MP4 export compatibility

MP4 export depends on browser support for H.264 video and AAC audio encoding. If the browser cannot provide those encoders, export will not be available. The app renders the canvas in the browser; it does not send the video to a remote rendering service.
