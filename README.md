# translate-video

Translate a video's spoken audio to another language while keeping the original visuals. Runs on Google Colab with GPU.

Uses Meta's [SeamlessM4T v2](https://huggingface.co/facebook/seamless-m4t-v2-large) for direct speech-to-speech translation.

## Quick start

1. Open `translate_video.ipynb` in Google Colab
2. Set `VIDEO_PATH` to your video on Google Drive (10s–2min)
3. Set `TARGET_LANG` (e.g. `"hin"` for Hindi)
4. Run all cells

The translated video is saved next to the original as `<name>_<lang>.mp4`.

## How it works

1. Extracts audio from the video
2. Translates speech in chunks (20s) using SeamlessM4T v2
3. Muxes the translated audio back with the original video

Model weights (~9 GB) are cached on Google Drive so they only download once.

## Supported languages

`hin` Hindi · `spa` Spanish · `fra` French · `deu` German · `ita` Italian · `por` Portuguese · `rus` Russian · `zho` Chinese · `jpn` Japanese · `kor` Korean · `ara` Arabic · `tur` Turkish · `ben` Bengali · `tam` Tamil · `tel` Telugu · `urd` Urdu · and [more](https://huggingface.co/facebook/seamless-m4t-v2-large)
