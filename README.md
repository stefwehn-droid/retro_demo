# AFTERGLOW – retro_demo

Eine Echtzeit-Grafik- und Sound-Demo im Stil der Demoszene von der fiktiven Gruppe „Neon Circuit“.
Alles ist **100 % prozedural**: Es gibt keine Bilder und keine Samples. Die Grafik entsteht in
GLSL-Shadern (WebGL2), die Musik wird live mit Oszillatoren der Web Audio API synthetisiert.

**Starten:** `index.html` in einem aktuellen Browser öffnen (Chrome, Edge, Firefox, Safari) und auf START klicken.

| Taste | Funktion |
|---|---|
| `F` | Vollbild |
| `Leertaste` | Pause |
| `M` | Ton an/aus |
| `1`–`7` | zu einer Szene springen |

`?scale=0.5` an die URL anhängen erzwingt eine feste Renderauflösung (für langsame Rechner).
Ohne den Parameter passt sich die Auflösung automatisch an die Bildrate an.

## Ablauf (ca. 2:40 min, 108 BPM, a-Moll)

| Takte | Szene | Musik |
|---|---|---|
| 0–8 | Sternenfeld und Copper-Bars (Amiga) | Pads, Arpeggio mit sich öffnendem Filter |
| 8–16 | XOR-Rotozoomer und Sinus-Laufschrift | Kick, Hi-Hats, Bass |
| 16–32 | Synthwave-Landschaft, Chrom-Titel | volles Arrangement mit Lead-Melodie |
| 32–44 | Raymarching: Chrom-Objekt mit Spiegelungen, das seine Form ändert | Breakdown, Build-up mit Snare-Wirbel |
| 44–52 | Kaleidoskop-Glow-Tunnel | Drop |
| 52–60 | Vector-Balls über Plasma | Drop mit Harmonie-Stimme |
| 60–71 | Synthwave bei Nacht, Abspann | Outro |

## Technik
- Szenen-Shader → Übergänge (Überblendung, Pixel-Dissolve, Wipe) → Text-Overlay → mehrstufiger Bloom →
  Chromatic Aberration, Scanlines, Vignette, Filmkorn, ACES-Tonemapping
- Synthesizer: Kick, Snare und Hi-Hats aus Oszillatoren und Rauschen, Saw-Bass, Super-Saw-Pads,
  Arpeggio, Lead mit Glide und Vibrato, Ping-Pong-Delay, Hall per Faltung, Sidechain-Ducking
- Grafik und Musik laufen auf derselben Audio-Uhr, deshalb reagiert die Grafik exakt auf Kick und Snare
