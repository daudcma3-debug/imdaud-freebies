# Otter.ai vs whisper.cpp: paid vs free meeting transcription

*Prices as of 19 Nov 2026 · By Abu Daud, CMA*

## The two tools

| | Otter.ai (paid, cloud) | whisper.cpp (free, open source) |
|---|---|---|
| What it does | AI meeting notetaker: joins Zoom, Teams and Google Meet, writes the transcript, speaker names, summary and action items | Runs OpenAI's Whisper speech-to-text model on your own computer (C/C++ port) |
| Price | Basic $0 · Pro $16.99/user/mo ($8.33 billed yearly) · Business $30/user/mo ($19.99 billed yearly) · Enterprise custom | $0 · MIT licence |
| Free-tier limits | Basic: 300 min/month, 30 min per conversation, 3 lifetime file imports | No monthly cap; speed depends on your computer |
| Setup | Sign up, connect your calendar (about 2 minutes) | Four terminal commands, one time (about 20 minutes) |
| Where audio goes | Otter's cloud service | Stays on your computer |
| Link | https://otter.ai/pricing | https://github.com/ggml-org/whisper.cpp |

Otter plan detail (otter.ai/pricing, 19 Nov 2026): Pro 1,200 min/month, 90 min per conversation, 10 file imports a month. Business: unlimited meeting minutes, 4 hours per conversation. List prices shown; the page also shows time-limited promos, which are not used here.

## whisper.cpp quick start

```
git clone https://github.com/ggml-org/whisper.cpp.git
cd whisper.cpp
sh ./models/download-ggml-model.sh base.en
cmake -B build
cmake --build build -j --config Release
./build/bin/whisper-cli -f meeting.wav
```

Tip: whisper-cli reads 16-bit WAV files. Convert other recordings first, e.g. `ffmpeg -i meeting.m4a -ar 16000 -ac 1 -c:a pcm_s16le meeting.wav`. Then paste the transcript into Claude for a summary and action items.

## Who should pick which

- **Otter.ai:** teams that want a notetaker on every call with zero setup, and built-in summaries.
- **whisper.cpp:** confidential calls (audit, board, payroll), many hours of recordings a month, and someone comfortable with a terminal.
- Neither is "better". Pick by volume, privacy and who will run it. For sensitive meetings, follow your company's policy first.

## Sources

- Otter.ai pricing page: https://otter.ai/pricing (checked 19 Nov 2026)
- whisper.cpp by ggml-org (MIT licence, ~55k stars): https://github.com/ggml-org/whisper.cpp (checked 19 Nov 2026)

---
By Abu Daud, CMA · WhatsApp +966 57 561 5384 · Instagram @imdaud
