# Part 3 - Repository Overview

Here is a brief overview of Meadowlark's repositories, as well as some notable dependencies.

* [`main repository`](https://github.com/MeadowlarkDAW/Meadowlark)
   * license: [GPLv3]
   * This houses the core application of Meadowlark including the UI, state management system, and the glue tying it all to the backend engine.
* [`dropseed`](https://github.com/MeadowlarkDAW/dropseed)
   * license: [GPLv3]
   * This houses the core backend engine. More specifically it provides a highly flexible audio graph system with automatic delay compensation and summation of edges, as well as providing plugin hosting (with a special focus on CLAP plugins).
   * It depends on the [`audio-graph`](`https://github.com/MeadowlarkDAW/audio-graph`) crate, which houses the pure abstract graph compilation algorithm. This helps us separate areas of concern and focus on the pure compilation algorithm at hand.
   * It depends on the [`clack`](https://github.com/prokopyl/clack) crate for its bindings to the CLAP plugin API.
* [`rainout`](https://github.com/MeadowlarkDAW/rainout)
   * license: [MIT]
   * This crate is responsible for connecting to the system's audio and MIDI devices. It's goal is to provide a powerful, cross-platform, highly configurable, low-latency, and robust solution for connecting to audio and MIDI devices.
   * [rainout design document](https://github.com/MeadowlarkDAW/rainout/blob/main/DESIGN_DOC.md)
* [`creek`](https://github.com/MeadowlarkDAW/creek)
   * license: [MIT]
   * This crate handles realtime-safe disk streaming to/from audio files.
   * It depends on the [`Symphonia`] crate for decoding a wide variety of codecs.
* [`pcm-loader`](https://github.com/MeadowlarkDAW/pcm-loader) (name in progress)
   * license: [MPL-2.0]
   * This crate handles loading audio files into RAM. It is mostly an easy-to-use wrapper around the [`Symphonia`] decoding library.
   * This crate also handles resampling to a target sample rate either at load-time or in realtime during playback. It uses the [`samplerate-rs`](https://github.com/MeadowlarkDAW/samplerate-rs) crate for samplerate conversion.
* [`meadowlark-plugins`](https://github.com/MeadowlarkDAW/meadowlark-plugins)
   * license: [GPLv3]
   * This repository houses the DSP for Meadowlark's internal plugins. Note that the UI for the plugins will live inside the main repository.
   * Later on this repo may also wrap the DSP code into plugins that can be loaded into other DAWs, complete with custom UIs. We will likely use [`nih-plug`](https://github.com/robbert-vdh/nih-plug) for this.
   * [meadowlark-plugins design document](https://github.com/MeadowlarkDAW/meadowlark-plugins/blob/main/DESIGN_DOC.md)
* [`meadowlark-clap-exts`](https://github.com/MeadowlarkDAW/meadowlark-clap-exts)
   * license: [MIT]
   * This repository houses our custom CLAP extensions that external plugins can use to better integrate with Meadowlark.
   * Most important is the extension that allows defining custom inline UIs inside Meadowlark's horizontal FX rack.
* [`meadowlark-offline-audio-fx`](https://github.com/MeadowlarkDAW/meadowlark-offline-audio-fx) (name in progress)
   * license: [GPLv3]
   * This repository will house various offline audio effect DSP such at pitch shifting, time stretching, formant shifting, transient detection, convolution, etc.
   * *design document WIP*
* [`meadowlark-factory-library`](https://github.com/MeadowlarkDAW/meadowlark-factory-library)
   * license: [Creative Commons Zero] (CC0)
   * This repository will house the factory samples and presets that will be included in Meadowlark.
* [`MeadowlarkDAW.github.io`](https://github.com/MeadowlarkDAW/MeadowlarkDAW.github.io)
   * license: [GPLv3]
   * This houses the official website.
* [`project-board`](https://github.com/MeadowlarkDAW/project-board)
   * This houses the kanban-style project board for the entire project.
   * (I'm not a fan of how GitHub Projects assigns every task as an "issue" in that repository and clutters up the issues tab. So I'm using this repository as a dedicated place to hold all of the generated issues instead.)

[`Symphonia`]: https://github.com/pdeljanov/Symphonia
[GPLv3]: https://choosealicense.com/licenses/gpl-3.0/
[MIT]: https://choosealicense.com/licenses/mit/
[MPL-2.0]: https://choosealicense.com/licenses/mpl-2.0/
[Creative Commons Zero]: https://creativecommons.org/choose/zero/