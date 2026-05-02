# VocalBurst Taxonomy

A taxonomy of **82 non-speech vocal sound categories** covering the full range of human vocalizations beyond intelligible speech — from laughter and crying to breathing patterns, mouth sounds, and body sounds.

## Overview

The VocalBurst taxonomy classifies non-speech vocal sounds into 16 semantic groups. Each category has a short label and a description defining the acoustic characteristics and typical emotional/physical context of the sound.

This taxonomy was developed alongside the [LAION Improved Synthetic Vocal Bursts Dataset](https://huggingface.co/datasets/laion/vocal-burst-db) containing 15,680 annotated audio samples with BM25-searchable captions.

**Source:** [laion/vocal-burst-db](https://huggingface.co/datasets/laion/vocal-burst-db)
**Machine-readable:** [`vocalburst_taxonomy.json`](vocalburst_taxonomy.json)

## Statistics

| Metric | Count |
|--------|-------|
| Total categories | 82 |
| Semantic groups | 16 |
| Audio samples in dataset | 15,680 |
| Gender balance | 7,851 female / 7,829 male |
| Audio duration range | 4–10 seconds |

## Category Groups

### Laughter (8 categories)
Vocal expressions of amusement ranging from suppressed to unrestrained.

| Category | Description |
|----------|-------------|
| Breathy Giggle | Soft airy laugh |
| Cackle | Harsh sharp laugh, sometimes unsettling |
| Childlike Giggle | Light playful laugh |
| Chuckle | Soft suppressed laugh showing mild amusement |
| Guffaw | Loud unrestrained laugh of strong amusement |
| Nervous Giggle | High-pitched laugh indicating anxiety |
| Snicker | Stifled laugh often conveying mockery or sarcasm |
| Snorting Giggle | Brief nasal snort combined with laughter |

### Crying & Distress (5 categories)
Vocalizations of grief, pain, or emotional distress.

| Category | Description |
|----------|-------------|
| Convulsive Sob | Intense crying with heaving breaths |
| Mournful Wail | Long high cry of grief |
| Quiet Sob | Soft crying with short broken breaths |
| Sobs | Audible heavier crying with convulsive gasps |
| Trembling Whimper | Faint cry indicating fear or pain |

### Breathing (7 categories)
Patterns of inhalation and exhalation with varying intensity and rhythm.

| Category | Description |
|----------|-------------|
| Deep Breath | Large inhalation to calm or refocus |
| Deep Breathing | Slow deliberate inhalations and exhalations for relaxation |
| Fast Breathing | Rapid inhalation and exhalation from excitement or stress |
| Heavy Breathing | Deep labored breaths of fatigue or tension |
| Normal Breathing | Regular rhythmic breaths at rest |
| Panting | Rapid breathing due to exertion or excitement |
| Slow Breathing | Paced controlled breaths for calm |

### Sighs (4 categories)
Audible exhales conveying emotional states.

| Category | Description |
|----------|-------------|
| Contented Sigh | Deep exhale expressing satisfaction |
| Exasperated Sigh | Audible breath of frustration |
| Relief Sigh | Release of tension after stress |
| Wistful Sigh | Soft exhale tinged with longing |

### Gasps & Inhales (3 categories)
Sudden or sharp breath intakes.

| Category | Description |
|----------|-------------|
| Fearful Gasp | Sudden inhale showing shock or anxiety |
| Sharp Inhale | Quick breath of sudden realization |
| Surprised Gasp | Quick intake of breath in astonishment |

### Groans & Moans (4 categories)
Low-pitched sustained vocalizations.

| Category | Description |
|----------|-------------|
| Exhausted Groan | Weary sound indicating fatigue |
| Frustrated Groan | Deep sound of annoyance |
| Pain Moan | Low vocalization signaling discomfort |
| Pleasure Moan | Soft prolonged sound of enjoyment |

### Grunts (3 categories)
Short forceful vocal bursts.

| Category | Description |
|----------|-------------|
| Affirmative Grunt | Short sound indicating agreement |
| Displeased Grunt | Harsh vocalization of dissatisfaction |
| Effort Grunt | Short forceful sound during physical strain |

### Throat & Vocal Sounds (7 categories)
Sounds produced in the throat or with indistinct vocalization.

| Category | Description |
|----------|-------------|
| Ahem | Clearing throat to gain attention or show discomfort |
| Clears Throat | Brief intentional effort to remove phlegm or gain attention |
| Growl | Low guttural rumble conveying anger |
| Gurgling | Bubbling sound in the throat |
| Hiss | Sustained sibilant sound of disapproval |
| Low Mumble | Indistinct vocalization of uncertainty or drowsiness |
| Whispered Mumble | Very quiet muddled speech sounds |

### Humming (4 categories)
Sustained tonal sounds with closed or partially closed mouth.

| Category | Description |
|----------|-------------|
| Humming | Low continuous vocal tone, often tuneful or absent-minded |
| Purr | Soft continuous vibrating hum showing contentment |
| Resonant Hum | Lower-pitched thoughtful hum |
| Soft Hum | Steady tone with closed lips in contentment |

### Coughing & Sneezing (7 categories)
Reflexive respiratory sounds.

| Category | Description |
|----------|-------------|
| Cough | Sharp expulsion of air from lungs |
| Coughing | Series of forceful expulsions of air from lungs |
| Hiccup | Spasmodic contraction of diaphragm creating a 'hic' sound |
| Hiccups | Involuntary diaphragmatic spasm producing 'hic' sound |
| Sniff | Audible inhalation through the nose, possibly sadness or restraint |
| Snort | Quick burst of air through the nose, often disbelief |
| Yawn | Involuntary wide-mouthed breath showing tiredness |

### Whistling (5 categories)
Tonal sounds produced by directed airflow.

| Category | Description |
|----------|-------------|
| Person Whistling Playfully | Lighthearted melodic whistle |
| Person Whistling to Get Attention | Serious sharp whistle |
| Sharp Whistle | Quick high-pitched attention grabber |
| Soft Whistle | Gentle tuneful blowing of air |
| Wolf Whistle | Two-note whistle expressing admiration |

### Mouth & Lip Sounds (9 categories)
Sounds produced by lips, tongue contact, or oral suction.

| Category | Description |
|----------|-------------|
| Blowing a Kiss | Brief airy sound of sending affection |
| Kissing Noises | Repetitive gentle lip compression for affection |
| Kissing Sounds | Soft repeated lip contact expressing affection |
| Lip Smack | Soft pop of parted lips indicating anticipation |
| Smack One's Lips | Light pop of lips, often from dryness or taste anticipation |
| Smacks Lips | Repetitive lip popping after tasting or anticipating food |
| Licking Sound | Light quick contact of tongue on surface |
| Spitting | Forceful expulsion of saliva |
| Sucking Noise | Soft pulling sound created by suction |

### Tongue Clicks (4 categories)
Sharp percussive sounds made with the tongue.

| Category | Description |
|----------|-------------|
| Click One's Tongue | Short 'tch' sound by flicking tongue off palate |
| Clicks Tongue | Distinct click by tapping tongue against the palate |
| Tongue Click | Distinct clack made by tongue against palate |
| Tsk | Clicking sound of reprimand or annoyance |

### Eating & Drinking (6 categories)
Sounds associated with food and liquid consumption.

| Category | Description |
|----------|-------------|
| Chewing Noises | Crunching or moist sounds from the mouth |
| Drinking Noises | Audible liquid intake with gulps or slurps |
| Gulps | Short audible swallow from nervousness or ingesting |
| Nervous Gulp | Audible swallow indicating anxiety |
| Slurping Noises | Wet sucking sound typically when consuming liquids |
| Swallows | Audible movement of liquid down the throat |

### Screams & Shrieks (2 categories)
High-intensity vocal outbursts.

| Category | Description |
|----------|-------------|
| Scream | Loud high-pitched outburst of extreme emotion |
| Shriek | Sharp piercing cry typically of fear |

### Hand & Body Sounds (4 categories)
Non-vocal physical sounds produced by the body.

| Category | Description |
|----------|-------------|
| Finger Snaps | Brief sharp click made by friction of thumb and finger |
| Hand Scratching Head | Soft rustling of fingers on scalp |
| Hand Slaps | Solid impact sound of palm against a surface or another hand |
| Slap Face | Sharp impact sound of palm against face |

## Quick Reference

```python
import json

with open("vocalburst_taxonomy.json") as f:
    taxonomy = json.load(f)

# List all groups and their categories
for group_name, group_data in taxonomy["categories"].items():
    items = group_data["items"]
    print(f"\n{group_name} ({len(items)} categories):")
    for name, info in items.items():
        print(f"  - {name}: {info['description']}")
```
