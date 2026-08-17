# Current task state (animated GIF + Discord, Aug 18 2026)

## User request (latest)
1. REMOVE BOTH static images from the profile README (the wide banner `soft-banner.png`
   and the anime-girl static image `anime-girl.png` at top of README).
2. Instead add ONE anime girl as an animated GIF (not a statue/image — must have living
   subtle motion: hair, rain, light, breathing). Design her even better.
3. Add Discord badge/link: https://discord.com/users/npc_with_thoughts
   (username displayed as npc_with_thoughts; link https://discord.com/users/npc_with_thoughts)

## Repo / files
- Local clone: ~/profile (branch main, remote sphangcho203-afk/sphangcho203-afk)
- README.md: lines 58-71 = social badges section (Telegram, X, Spotify, Instagram), all
  centered <p align="center"> with a href + img height=26 shields.io badges:
  - Telegram-211b24?style=flat-square&logo=telegram&logoColor=8b3a46 → https://t.me/Zulurux98
  - X-211b24?style=flat-square&logo=twitter&logoColor=8b3a46&logoSize=auto → https://x.com/PhangchoSo60056
  - Spotify-211b24?style=flat-square&logo=spotify&logoColor=8b3a46 → https://open.spotify.com/user/31snn46vcywdzfq3aalcghwr3uru
  - Instagram-211b24?style=flat-square&logo=instagram&logoColor=8b3a46 → https://www.instagram.com/nerfed_irl._
- Banner referenced near top of README (~line 15-20 area) as assets/soft-banner.png.
- Anime girl static image referenced ~lines 25-35 as assets/anime-girl.png (square hero).
- Palette: charcoal plum #211B24, muted burgundy #8B3A46, dusty rose #B65C65,
  rainy blue-gray #65758B, warm amber #CB9A6B.
- Latest commits: e267556 (X badge fix). After this task: commit + push origin main.
- Verify live: curl https://raw.githubusercontent.com/sphangcho203-afk/sphangcho203-afk/main/README.md

## Plan for the GIF
- Use existing assets/anime-girl.png as the character reference (dusty-rose/burgundy hair,
  amber eyes, dark sweater, at desk by rainy window, lamp, headphones, mug, butterflies).
- generate_video from that image (first keyframe) with gemini-omni-flash-preview,
  portrait 9:16, 720p, no audio, subtle loops (hair sway, rain on window, lamp flicker,
  butterflies drifting, blinking). Then convert mp4 → looping gif with ffmpeg:
  ffmpeg -i clip.mp4 -vf "fps=12,scale=480:-1:flags=lanczos,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" -loop 0 anime-girl.gif
  (aim for < 2MB if possible; GitHub allows up to 10MB GIF in README images.)
- Aspect: generate_image base keyframes must be 16:9 or 9:16 per skill — anime-girl.png is
  1:1; may need to upscale/reframe to 9:16 keyframe first via generate_image_variation or
  crop. Simplest: use anime-girl.png as FIRST keyframe reference only; video tool can take
  it as reference image (not keyframe) if ratio mismatches, or reframed 9:16 version.
- Put GIF in assets/anime-girl.gif, commit, push.

## Discord badge URL pattern (shields.io)
https://img.shields.io/badge/Discord-211b24?style=flat-square&logo=discord&logoColor=8b3a46
Discord link: https://discord.com/users/npc_with_thoughts
