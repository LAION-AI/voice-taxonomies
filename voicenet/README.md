# VoiceNet Taxonomy

A comprehensive taxonomy of **59 perceptual dimensions** for describing human speech characteristics, covering everything from tempo and pitch to emotional affect and speaking style.

## Overview

The VoiceNet taxonomy provides a standardized framework for annotating speech along multiple orthogonal dimensions. Each dimension uses a 7-point scale (0-6) with detailed anchor descriptions at each level, enabling consistent human and machine annotation of voice properties.

**Source:** [TTS-AGI/voice-annotation-data-v2](https://huggingface.co/datasets/TTS-AGI/voice-annotation-data-v2)
**License:** CC-BY-4.0
**Machine-readable:** [`voicenet_taxonomy.json`](voicenet_taxonomy.json)

## Dimension Categories

| Category | Dimensions | Description |
|----------|-----------|-------------|
| Rhythm & Timing | 8 | Tempo, chunking, smoothness, articulation, pitch range, emphasis, disfluency, structure |
| Social & Interpersonal | 3 | Stance, focus, vulnerability |
| Speaker Identity | 3 | Perceived gender, voice age, register |
| Emotion & Affect | 3 | Valence, arousal, volatility |
| Physical Production | 4 | Respiration, tension, cognitive load, attack |
| Spectral & Timbral | 7 | Brightness, roughness, harmonicity, fullness, warmth, metallic character, esthetics |
| Temporal Dynamics | 4 | Velocity flux, dynamic arc, arousal shift, valence shift |
| Language & Recording | 5 | Language, accent, recording quality, background noise, content appropriateness |
| Resonance Placement | 7 | Chest, throat, oral, mask, nasal, head, mixed resonance |
| Speaking Style | 15 | Casual, conversational, formal, dramatic, narrator, newsreader, teacher, authoritative, playful, cartoonish, ASMR, whisper, ranting, storytelling, monologue |

**Total: 59 dimensions across 10 categories**

## Scale Design

Most dimensions use a symmetric 7-point scale:
- **0** = Extreme low end / absence
- **3** = Neutral / standard / balanced
- **6** = Extreme high end / maximum presence

Exceptions:
- **LANG** (Language): Categorical, 12 values (0=English, 1=German, ... 11=Other)
- **EXPL** (Content Appropriateness): 3-point scale (0=Safe for School, 1=Safe for Work, 2=NSFW)

## Temporal Markers

Some dimensions carry temporal markers indicating how they should be measured:
- **[TEMPORAL PATTERN]**: Measured as an aggregate/average over the full clip
- **[TEMPORAL TRAJECTORY]**: Measured as a directional change from start to finish

## Statistics

- **Total buckets (dimension x value combinations):** 399
- **Validated with:** Gemini 2.0 Flash (positive + negative sample pairs)
- **Audio format:** MP3, mono, 64 kbps, 44.1 kHz

## Quick Reference

```python
import json

with open("voicenet_taxonomy.json") as f:
    taxonomy = json.load(f)

# Get all dimension codes
print(list(taxonomy.keys()))

# Look up a specific dimension
tempo = taxonomy["TEMP"]
print(f"{tempo['name']}: {tempo['measures']}")
for val, desc in tempo["values"].items():
    print(f"  {val}: {desc}")
```

## Dimension Codes

| Code | Name | Category |
|------|------|----------|
| TEMP | Tempo | Rhythm & Timing |
| CHNK | Chunking | Rhythm & Timing |
| SMTH | Smoothness | Rhythm & Timing |
| CLRT | Articulation Clarity | Rhythm & Timing |
| RANG | Pitch Range | Rhythm & Timing |
| EMPH | Emphasis | Rhythm & Timing |
| DFLU | Disfluency | Rhythm & Timing |
| STRU | Structure | Rhythm & Timing |
| STNC | Stance | Social & Interpersonal |
| FOCS | Focus | Social & Interpersonal |
| VULN | Vulnerability | Social & Interpersonal |
| GEND | Perceived Gender | Speaker Identity |
| AGEV | Voice Age | Speaker Identity |
| REGS | Register | Speaker Identity |
| VALN | Valence | Emotion & Affect |
| AROU | Arousal | Emotion & Affect |
| VOLT | Volatility | Emotion & Affect |
| RESP | Respiration | Physical Production |
| TENS | Tension | Physical Production |
| COGL | Cognitive Load | Physical Production |
| ATCK | Attack | Physical Production |
| BRGT | Brightness | Spectral & Timbral |
| ROUG | Roughness | Spectral & Timbral |
| HARM | Harmonicity | Spectral & Timbral |
| FULL | Fullness | Spectral & Timbral |
| WARM | Warmth | Spectral & Timbral |
| METL | Metallic Character | Spectral & Timbral |
| ESTH | Esthetics | Spectral & Timbral |
| VFLX | Velocity Flux | Temporal Dynamics |
| DARC | Dynamic Arc | Temporal Dynamics |
| ARSH | Arousal Shift | Temporal Dynamics |
| VALS | Valence Shift | Temporal Dynamics |
| LANG | Language | Language & Recording |
| ACNT | Accent | Language & Recording |
| RCQL | Recording Quality | Language & Recording |
| BKGN | Background Noise | Language & Recording |
| EXPL | Content Appropriateness | Language & Recording |
| R_CHST | Chest Resonance | Resonance Placement |
| R_THRT | Throat Resonance | Resonance Placement |
| R_ORAL | Oral Resonance | Resonance Placement |
| R_MASK | Mask Resonance | Resonance Placement |
| R_NASL | Nasal Resonance | Resonance Placement |
| R_HEAD | Head Resonance | Resonance Placement |
| R_MIXD | Mixed Resonance | Resonance Placement |
| S_CASU | Casual Style | Speaking Style |
| S_CONV | Conversational Style | Speaking Style |
| S_FORM | Formal Style | Speaking Style |
| S_DRAM | Dramatic Style | Speaking Style |
| S_NARR | Narrator Style | Speaking Style |
| S_NEWS | Newsreader Style | Speaking Style |
| S_TECH | Teacher/Didactic Style | Speaking Style |
| S_AUTH | Authoritative Style | Speaking Style |
| S_PLAY | Playful Style | Speaking Style |
| S_CART | Cartoonish Style | Speaking Style |
| S_ASMR | ASMR Style | Speaking Style |
| S_WHIS | Whisper-Talk Style | Speaking Style |
| S_RANT | Ranting/Angry Style | Speaking Style |
| S_STRY | Storytelling Style | Speaking Style |
| S_MONO | Monologue Style | Speaking Style |
