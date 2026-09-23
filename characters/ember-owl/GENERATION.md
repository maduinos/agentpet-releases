> 만든 사람: maduinos<br>
> 문서 만든 날짜: 2026-07-16<br>
> https://maduinos.blogspot.com/

# Ember Owl generation record

## Source

- Generated: 2026-07-16
- Tool: OpenAI built-in image generation
- Source dimensions: 1402×1122 RGBA PNG on a chroma-key background
- Source SHA-256: `faae880b9f382ae01e17cb64aec7a303534bbb197e750c65a3673c3785736c3d`
- Input images: none

The generated source remains in the generating user's local Codex image store. The runtime package
contains only the transparent, cropped state frames.

## Exact prompt

```text
Use case: stylized-concept
Asset type: AgentPet desktop-pet pixel-art sprite sheet
Primary request: Create one original anthropomorphic owl librarian companion for the Claude provider, shown in eight distinct state poses in a precise 4-column by 2-row grid.
Scene/backdrop: one perfectly flat solid #00ff00 chroma-key background covering the entire sheet for later background removal. No cell borders or grid lines.
Subject: the exact same small round owl character in every cell, with a clearly owl-shaped silhouette, warm terracotta and cream feathers, dark brown short librarian mantle, tiny amber scarf, amber eyes, and a small satchel. Original design only. Top row left to right: idle; thinking/reading an open book; editing/writing with a quill; running/working with a tiny glowing gear. Bottom row left to right: waiting calmly; approval with one wing raised and a small punctuation-free alert gesture; success with subtle star sparkles; error/offline with dim lantern and drooped posture.
Style/medium: polished crisp pixel art desktop-pet game sprite, classic 16-bit/32-bit RPG character aesthetic, strong readable silhouette, limited palette, hard pixel clusters, no painterly texture, no photorealism.
Composition/framing: exactly 4 equal columns and 2 equal rows; each full-body owl centered independently with identical scale, body proportions, outfit, face, and palette; generous clear padding around every pose; no pose may touch or cross a cell boundary; each cell should suit a 12:13 portrait crop.
Lighting/mood: clean neutral sprite lighting; friendly, thoughtful, calm.
Color palette: terracotta orange, warm cream, dark brown, muted amber; do not use #00ff00 or any bright green anywhere in the character or props.
Constraints: same character identity in all eight poses; no text, letters, numbers, logos, trademarks, watermark, frame lines, floor plane, cast shadow, contact shadow, reflection, gradient, background texture, or extra characters. The background must be one uniform exact chroma-key color with crisp separation from the subject.
```

## Post-processing

1. Removed the sampled `#04f904` border key with the imagegen skill's
   `remove_chroma_key.py` helper using soft matte and despill.
2. Split the result into a 4×2 grid.
3. Trimmed each pose, resized it uniformly to 54%, and placed it bottom-aligned on a transparent
   192×208 canvas.
4. Stripped PNG metadata. Runtime frames contain only `IHDR`, `IDAT`, and `IEND` chunks.

No semantic repainting or third-party source image was used during post-processing.
