# EmoNet Taxonomy

A taxonomy of **40 emotion categories** for classifying vocal emotional expression, derived from the EmoNet framework. Each category represents a distinct emotional state with associated keywords that describe its manifestation in voice.

## Overview

The EmoNet taxonomy organizes human emotions into 40 discrete categories, each annotated with:
- **Valence**: Whether the emotion is positive, negative, neutral, or mixed
- **Arousal tendency**: The typical physiological activation level (low to high)
- **Keywords**: A set of related emotional terms that fall under the category

This taxonomy is designed for vocal emotion classification, enabling annotators and models to label emotional content in speech with fine-grained categories beyond basic "happy/sad/angry" labels.

**Source:** EmoNet Phase Paper
**Machine-readable:** [`emonet_taxonomy.json`](emonet_taxonomy.json)

## Statistics

| Metric | Count |
|--------|-------|
| Total categories | 40 |
| Positive valence | 16 |
| Negative valence | 17 |
| Neutral valence | 4 |
| Mixed valence | 3 |
| Total keywords | 263 |

## Categories by Valence

### Positive Emotions (16)

| Category | Arousal | Example Keywords |
|----------|---------|-----------------|
| Amusement | Medium-High | mirth, joviality, laughter, playfulness |
| Elation | High | happiness, excitement, joy, exhilaration |
| Pleasure/Ecstasy | High | ecstasy, rapture, bliss, beatitude |
| Contentment | Low | relaxation, peacefulness, calmness, serenity |
| Thankfulness/Gratitude | Medium-Low | gratitude, appreciation, gratefulness |
| Affection | Medium | compassion, warmth, trust, caring, tenderness |
| Infatuation | Medium-High | romantic desire, fondness, adoration |
| Hope/Optimism | Medium-High | enthusiasm, optimism, anticipation, courage |
| Triumph | High | triumph, superiority |
| Pride | Medium | dignity, self-confidence, honor |
| Awe | Medium-High | awestruck, wonder |
| Relief | Medium-Low | respite, alleviation, solace, comfort |
| Interest | Medium | fascination, curiosity, intrigue |

### Negative Emotions (17)

| Category | Arousal | Example Keywords |
|----------|---------|-----------------|
| Impatience and Irritability | Medium-High | irritation, restlessness, exasperation |
| Doubt | Medium-Low | distrust, suspicion, skepticism, uncertainty |
| Fear | High | terror, dread, apprehension, panic |
| Distress | Medium-High | worry, anxiety, anguish, trepidation |
| Confusion | Medium | bewilderment, disorientation, perplexity |
| Embarrassment | Medium | shyness, mortification, awkwardness |
| Shame | Medium-Low | guilt, remorse, humiliation |
| Disappointment | Medium-Low | regret, dismay, letdown, chagrin |
| Sadness | Low | sorrow, grief, melancholy, despair, heartache |
| Bitterness | Medium | resentment, acrimony, cynicism, rancor |
| Contempt | Medium | disapproval, scorn, disdain, loathing |
| Disgust | Medium-High | revulsion, repulsion, abhorrence |
| Anger | High | rage, fury, hate, wrath, annoyance |
| Malevolence/Malice | Medium-High | spite, sadism, schadenfreude |
| Sourness | Medium | tartness, acidity, acerbity, sharpness |
| Pain | High | suffering, torment, ache, agony |
| Helplessness | Low | powerlessness, desperation, submission |

### Neutral Emotions (4)

| Category | Arousal | Example Keywords |
|----------|---------|-----------------|
| Astonishment/Surprise | High | amazement, shock, startlement |
| Concentration | Medium | deep focus, engrossment, absorption |
| Contemplation | Medium-Low | thoughtfulness, pondering, reflection |
| Emotional Numbness | Low | detachment, apathy, stoicism, indifference |

### Mixed Emotions (3)

| Category | Arousal | Example Keywords |
|----------|---------|-----------------|
| Longing | Medium-Low | yearning, pining, wistfulness, nostalgia |
| Teasing | Medium-High | bantering, mocking playfully, ribbing |
| Sexual Lust | High | carnal desire, lust |

### Special States (2)

| Category | Arousal | Example Keywords |
|----------|---------|-----------------|
| Fatigue/Exhaustion | Low | weariness, lethargy, burnout |
| Intoxication/Altered States | Medium | stupor, disorientation, altered perception |
| Jealousy & Envy | Medium-High | jealousy, covetousness |

## Quick Reference

```python
import json

with open("emonet_taxonomy.json") as f:
    taxonomy = json.load(f)

# List all categories
for name, info in taxonomy["categories"].items():
    print(f"{info['id']:2d}. {name} [{info['valence']}, {info['arousal_tendency']}]")
    print(f"    Keywords: {', '.join(info['keywords'][:5])}...")
```

## Arousal-Valence Distribution

```
High    |  Fear,Anger,Pain    |  Surprise    |  Elation,Triumph,Ecstasy
        |  Disgust,Distress   |              |  Amusement,Hope
Medium  |  Bitterness,Contempt|  Concentration|  Affection,Pride
        |  Confusion,Embarr.  |  Intoxication |  Interest
Low     |  Sadness,Helpless   |  Numbness     |  Contentment,Relief
        |  Fatigue,Shame      |  Contemplation|  Gratitude
        |---------------------|--------------|------------------
        |     Negative        |   Neutral    |    Positive
```
