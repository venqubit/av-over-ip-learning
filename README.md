# AV over IP & Broadcast — Learning Roadmap

A step-by-step path to understand audio, video and broadcast signals, and to process them in software and hardware.
Each stage builds on the previous one. Repos are also saved in my GitHub Stars lists (**AV 1 – AV 5**).

**Goal:** understand audio, video and broadcast signals, then process them in software (FFmpeg/GStreamer) and hardware (FPGA/MCU), including professional IP workflows (SRT, NDI, AES67, SMPTE ST 2110, NMOS).

---

## Stage 1 — Signal fundamentals (start here)
| Repo | What you learn |
|---|---|
| [leandromoreira/digital_video_introduction](https://github.com/leandromoreira/digital_video_introduction) | Pixels, frames, YUV color, chroma subsampling, how codecs compress video |
| [AllenDowney/ThinkDSP](https://github.com/AllenDowney/ThinkDSP) | Audio DSP in Python: sampling, FFT, spectrum, filters (runnable notebooks) |
| [leandromoreira/ffmpeg-libav-tutorial](https://github.com/leandromoreira/ffmpeg-libav-tutorial) | Containers, codecs, decoding, transcoding in real C code |
| [krzemienski/awesome-video](https://github.com/krzemienski/awesome-video) | Curated index of video tools and resources for later exploration |

- [ ] Explain sample rate, bit depth, frame rate, resolution, YUV 4:2:2 vs 4:2:0
- [ ] Plot the spectrum of an audio file with ThinkDSP

## Stage 2 — Process audio/video in software
| Repo | What you learn |
|---|---|
| [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg) | Decode, scale, filter, encode — the industry's Swiss army knife |
| [GStreamer/gstreamer](https://github.com/GStreamer/gstreamer) | Pipeline-based media processing used in broadcast & embedded |
| [obsproject/obs-studio](https://github.com/obsproject/obs-studio) | Real-time capture, mixing, encoding in a production app |
| [juce-framework/JUCE](https://github.com/juce-framework/JUCE) | C++ framework for audio apps and plugins |

- [ ] Transcode a file, change resolution/frame rate, extract audio with FFmpeg
- [ ] Build a GStreamer pipeline: `videotestsrc ! x264enc ! ...`

## Stage 3 — AV over IP / streaming
| Repo | What you learn |
|---|---|
| [bluenviron/mediamtx](https://github.com/bluenviron/mediamtx) | Ready-to-run SRT / WebRTC / RTSP / RTMP / HLS server |
| [Haivision/srt](https://github.com/Haivision/srt) | Reliable low-latency video transport over the internet |
| [DistroAV/DistroAV](https://github.com/DistroAV/DistroAV) | NDI in OBS — try NDI on your home network |
| [bondagit/aes67-linux-daemon](https://github.com/bondagit/aes67-linux-daemon) | AES67 / RAVENNA audio over IP, PTP sync, RTP |
| [teodly/inferno](https://github.com/teodly/inferno) | Unofficial open Dante implementation |
| [video-dev/hls.js](https://github.com/video-dev/hls.js) | HLS playback in the browser |
| [gpac/gpac](https://github.com/gpac/gpac) | Packaging (MP4, DASH, HLS) and streaming |

- [ ] Stream FFmpeg → MediaMTX over SRT and watch in VLC
- [ ] Capture RTP packets in Wireshark and identify headers/timestamps

## Stage 4 — Professional broadcast IP (SMPTE ST 2110 & NMOS)
| Repo | What you learn |
|---|---|
| [OpenVisualCloud/Media-Transport-Library](https://github.com/OpenVisualCloud/Media-Transport-Library) | Software ST 2110 (uncompressed video/audio/ancillary over IP) |
| [sony/nmos-cpp](https://github.com/sony/nmos-cpp) | NMOS IS-04/IS-05 discovery and connection management |
| [AMWA-TV/nmos-testing](https://github.com/AMWA-TV/nmos-testing) | Official AMWA NMOS compliance test suite |
| [ebu/pi-list](https://github.com/ebu/pi-list) | EBU LIST — analyze ST 2110 pcaps, timing and packet pacing |

- [ ] Read ST 2110-20/-30/-40 overviews and PTP (ST 2059) basics
- [ ] Run an NMOS registry + virtual node with nmos-cpp

## Stage 5 — Hardware processing
| Repo | What you learn |
|---|---|
| [hdl-util/hdmi](https://github.com/hdl-util/hdmi) | HDMI output from an FPGA — video timing at signal level |
| [enjoy-digital/litex](https://github.com/enjoy-digital/litex) | Build FPGA SoCs, used in many open video projects |
| [PaulStoffregen/Audio](https://github.com/PaulStoffregen/Audio) | Real-time audio DSP on Teensy microcontrollers |

- [ ] Simulate/display a test pattern via FPGA HDMI
- [ ] Build a simple audio filter/effect on a Teensy

---

## Suggested timeline
| Weeks | Focus |
|---|---|
| 1–2 | Stage 1 (fundamentals) |
| 3–5 | Stage 2 (FFmpeg, GStreamer hands-on) |
| 6–8 | Stage 3 (SRT, NDI, AES67 labs) |
| 9–11 | Stage 4 (ST 2110, NMOS, PTP) |
| 12+ | Stage 5 (FPGA / MCU projects) |

## My notes

