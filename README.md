# FiveBless Dataset — Metadata Only

This repository provides **structured metadata** for the *FiveBless Dataset*, a curated collection of images related to the Chinese cultural concept of the **"Five Blessings"** (五福):  
- 福 (Luck)  
- 禄 (Prosperity)  
- 寿 (Longevity)  
- 喜 (Double Happiness)  
- 财 (Wealth)

> ⚠️ **No images are included in this repository.**  
> All images remain on their original platforms (e.g., Zcool, Behance, Baidu). This dataset contains only **metadata and source URLs**.

---

## 📁 Files Included

- `metadata.csv`: Tabular metadata for negative samples, including image IDs, labels, and source links.

---

## 🏷️ Annotation Guidelines (v1.0)

### Negative Sample Criteria
Images labeled as negative (`is_negative = yes`) must:
- **Not contain any symbolic elements** of the Five Blessings (e.g., 福字, longevity symbols, double-happiness motifs).
- Resemble positive samples in **style, color, or composition** (e.g., red tones, traditional aesthetics) to challenge model robustness.
- Examples: modern red designs, plain ceramics, urban scenes with traditional architecture but no decorations.

> ❗ **Important**: Images with ambiguous or partial symbols are excluded.

### Metadata Schema
Each entry includes:
| Field | Value Example | Description |
|------|----------------|------------|
| `image_id` | `neg_002.jpg` | Unique identifier |
| `primary_blessing` | `none` | Always "none" for negative samples |
| `symbol_objects` | `none` | No symbolic objects present |
| `is_negative` | `yes` | Confirmed negative sample |
| `symbol_reason` | `"no clear symbols of the Five Blessings"` | Justification |
| `time_period` | `Modern` | Era of the item/design |
| `product_function` | `poster`, `decoration`, `architecture` | Functional category |
| `source_reference` | `https://www.zcool.com.cn/...` | Original image URL |

---

## ⚠️ Copyright Notice

- This dataset **does NOT include any images**.
- All images remain on their original websites (e.g., [Zcool](https://www.zcool.com.cn), [Behance](https://www.behance.net), Baidu).
- The **copyright of images belongs to their respective creators or platforms**.
- This metadata is provided for **academic research only**.
- Users **must comply** with the terms of use of the source websites.

> 🔒 Downloading, redistributing, or commercializing the linked images may require separate permission from the rights holders.

---

## 📜 License

The **metadata** in this repository is released under the **[CC0 1.0 Universal License](LICENSE.txt)**.  
You are free to:
- Copy, modify, and distribute this metadata
- Use it for academic or commercial purposes
- Without asking permission or providing attribution

> 📌 **Note**: This license **applies ONLY to the metadata**, not to the images linked via `source_reference`.

---

## 📚 Reference

Han, Dan. (2025). *FiveBless Dataset Annotation Guidelines* (Version 1.0).  
Inspired by cultural concepts discussed in:  
> *Five-fold Happiness: Chinese Concepts of Luck, Prosperity, Longevity, Happiness, and Wealth*  
> ISBN: 978-1-4521-3939-5  
> [Palace Museum Publications](https://www.dpm.org.cn)

---

## 💡 Intended Use

- Training and evaluating computer vision models for cultural symbol detection
- Studying visual representations of traditional Chinese values
- Robustness testing against style-matched negative samples
