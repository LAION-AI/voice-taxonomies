# LAION Voice Taxonomies

A collection of three complementary taxonomies for describing, annotating, and classifying human vocal audio. Together they cover **speech characteristics**, **emotional expression**, and **non-speech vocalizations**.

## The Three Taxonomies

| Taxonomy | Scope | Categories | Scale |
|----------|-------|-----------|-------|
| [**VoiceNet**](voicenet/) | Speech dimensions (how someone speaks) | 59 dimensions | 7-point (0-6) per dimension |
| [**EmoNet**](emonet/) | Emotional categories (what someone feels) | 40 categories | Categorical with valence/arousal |
| [**VocalBurst**](vocalburst/) | Non-speech sounds (vocal bursts) | 82 categories | Categorical across 16 groups |

## VoiceNet Taxonomy

**59 perceptual dimensions** for describing speech along orthogonal axes.

Organized into 10 groups: Rhythm & Timing, Social & Interpersonal, Speaker Identity, Emotion & Affect, Physical Production, Spectral & Timbral, Temporal Dynamics, Language & Recording, Resonance Placement, and Speaking Style.

Each dimension uses a 7-point scale with detailed anchor descriptions. Example:

```
TEMP (Tempo): Speed of word/syllable production
  0 = Glacially slow, syllables stretched to breaking point
  3 = Standard conversational tempo, balanced and natural
  6 = Hyper-accelerated, blistering speed (auctioneer/panic)
```

- [Full documentation](voicenet/README.md)
- [Machine-readable JSON](voicenet/voicenet_taxonomy.json)
- Dataset: [TTS-AGI/voice-annotation-data-v2](https://huggingface.co/datasets/TTS-AGI/voice-annotation-data-v2)

## EmoNet Taxonomy

**40 emotion categories** with associated keywords, valence, and arousal annotations.

Spans the full emotional spectrum from positive states (Amusement, Elation, Contentment) through neutral (Concentration, Contemplation) to negative (Fear, Anger, Sadness) and mixed states (Longing, Teasing).

Each category includes:
- Valence classification (positive/negative/neutral/mixed)
- Arousal tendency (low to high)
- 4-10 descriptive keywords per category

- [Full documentation](emonet/README.md)
- [Machine-readable JSON](emonet/emonet_taxonomy.json)
- Source: EmoNet Phase Paper

## VocalBurst Taxonomy

**82 non-speech vocal sound categories** across 16 semantic groups.

Covers: Laughter (8), Crying & Distress (5), Breathing (7), Sighs (4), Gasps (3), Groans & Moans (4), Grunts (3), Throat Sounds (7), Humming (4), Coughing & Sneezing (7), Whistling (5), Mouth & Lip Sounds (9), Tongue Clicks (4), Eating & Drinking (6), Screams (2), Hand & Body Sounds (4).

- [Full documentation](vocalburst/README.md)
- [Machine-readable JSON](vocalburst/vocalburst_taxonomy.json)
- Dataset: [laion/vocal-burst-db](https://huggingface.co/datasets/laion/vocal-burst-db)

## How They Fit Together

```
┌─────────────────────────────────────────────────────────────┐
│                    Human Vocal Audio                         │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │  VoiceNet   │  │   EmoNet    │  │     VocalBurst      │ │
│  │             │  │             │  │                     │ │
│  │ HOW someone │  │ WHAT someone│  │ NON-SPEECH sounds   │ │
│  │ speaks      │  │ feels       │  │ someone makes       │ │
│  │             │  │             │  │                     │ │
│  │ 59 dims     │  │ 40 emotions │  │ 82 sound types      │ │
│  │ continuous  │  │ categorical │  │ categorical         │ │
│  └─────────────┘  └─────────────┘  └─────────────────────┘ │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

- **VoiceNet** answers: How fast, loud, rough, warm, formal, etc. is this speech?
- **EmoNet** answers: What emotion is being expressed?
- **VocalBurst** answers: What non-speech sound is this?

## Usage

All taxonomies are available as JSON files for programmatic access:

```python
import json

# Load any taxonomy
with open("voicenet/voicenet_taxonomy.json") as f:
    voicenet = json.load(f)

with open("emonet/emonet_taxonomy.json") as f:
    emonet = json.load(f)

with open("vocalburst/vocalburst_taxonomy.json") as f:
    vocalburst = json.load(f)
```

## License

CC-BY-4.0

## References

- Voice Annotation Data v2: https://huggingface.co/datasets/TTS-AGI/voice-annotation-data-v2
- Vocal Burst Database: https://huggingface.co/datasets/laion/vocal-burst-db
- LAION: https://laion.ai
