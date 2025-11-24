# EgoObjects Intention Annotations

This repository contains intention annotations for 100 images from the EgoObjects dataset.

## 📊 Dataset Overview

- **Total Images**: 100
- **Unique Groups**: 100 (one image per group)
- **Annotations**: Each image includes:
  - Target object category
  - 3 context-aware human intentions
  - Scene reasoning

## 🎯 Intention Annotation Task

The intentions were generated using GPT-4o with the following constraints:
1. **No object name mentions**: Intentions describe the human need, not the object
2. **Environment-grounded**: Aligned with visible scene context
3. **Natural language**: First-person perspective (e.g., "I need to...")
4. **Task-focused**: Describes what the user wants to accomplish

## 📁 Repository Structure

```
.
├── index.html           # Interactive table view
├── intentions.json      # Raw annotation data
├── annotations.json     # Original EgoObjects annotations
└── images/              # 100 sampled images
```

## 🌐 View Online

Simply open `index.html` in your browser to explore the annotations.

## 📖 Data Format

```json
{
  "image_id": {
    "image_file": "xxx.jpg",
    "target_object_id": 12345,
    "target_category": "spoon",
    "scene_reasoning": "Kitchen setting with breakfast items...",
    "intentions": [
      "I'm about to enjoy this boiled egg...",
      "I want to add sugar to my coffee...",
      "It's time for breakfast..."
    ]
  }
}
```

## 🔧 Generation Details

- **Model**: GPT-4o
- **Selection Strategy**: Priority to `is_main` objects, otherwise random selection
- **Prompt Engineering**: Few-shot examples with strict constraints

## 📜 License

This dataset is derived from EgoObjects V1. Please refer to the original dataset license.

## 🙏 Acknowledgments

Based on the EgoObjects dataset for egocentric object understanding.

