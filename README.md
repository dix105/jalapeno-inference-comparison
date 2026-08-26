# OpenAI Jalapeño vs GPU

Inference cost and speed comparison. OpenAI published work-per-watt for
Jalapeño, not tokens-per-second. This page puts that announced figure next
to speeds other chips and APIs have actually posted.

Static single-page tool. No build step, no dependencies.

## What it shows

Three dimensions:

- **Power** — 1.5–1.9× work per watt vs GPUs (the only Jalapeño number in
  the 25 Aug 2026 release), 700 W, Broadcom.
- **Speed** — tok/s by model, so Gemma 4 31B is not mixed with GPT OSS 120B
  unless you ask. Jalapeño has no tok/s; the row stays blank on purpose.
- **Cost** — implied energy saved vs the GPU class, derived from the
  announced multiplier. Not an API price. Jalapeño is not a service.

Every bar is tagged **measured** (Artificial Analysis), **official**
(provider page), or **announced** (press release).

## Numbers on the page

- Jalapeño: 1.5–1.9× work/watt vs GPUs, 700 W, Broadcom, announced 25 Aug 2026. Not a service.
- NVIDIA Groq 3 LPX: 3,400 tok/s on Gemma 4 31B (announced). [Release note](https://blog.toolsnetwork.ai/releases/nvidia-groq-3-lpx-production/).
- Cerebras WSE-3: GPT OSS 120B at 3,000 tok/s (official) and 1,715 (Artificial Analysis).
- Groq LPU: Llama 3.1 8B at 1,800 tok/s; GPT OSS 120B at 500 tok/s (official).
- OpenAI API: GPT-5.6 Sol at 90 tok/s (Artificial Analysis).
- Cerebras Ultrafast: GPT-5.6 Sol at 750 tok/s (announced).
- NVIDIA H100 / H200 / B200: named as the GPU comparison class. No per-chip tok/s in this dataset.

## Deploy

Static site, no build step.

    vercel --prod

Framework preset **Other**, no build command, output directory `.`.

## Licence

MIT.
