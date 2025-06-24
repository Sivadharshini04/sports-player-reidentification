
# Report on  Player Re-identification 

**Project:** Sports Player Re-identification using YOLOv11  
**Author:** Sivadharshini Saminathan
**Date:** June 24, 2025

---

##  Objective

Re-identify players in a sports video using the given pre-trained Ultralytics YOLOv11 model. The goal is to ensure that players retain consistent IDs even if they leave and later re-enter the camera frame.

---

## Approach and Methodology

- Used the fine-tuned YOLOv11 model (`best.pt`) for detecting players and the ball.
- Processed the given 15-second input video (`15sec_input_720p.mp4`) frame-by-frame.
- For every frame:
  - Detected players using the YOLOv11 model.
  - Applied simple feature-based comparison, ie, bounding box size and position, for re-identification.
- Assigned IDs incrementally to detected players.
- Output video saved with bounding boxes and ID overlays as `output.mp4`.

---

## Techniques Tried and Outcomes

- Pure detection-based tracking using YOLOv11.
- Feature matching based on position and bounding box dimensions.
- Players were detected in each frame.
- However, only 2 IDs were assigned due to limited visual differentiation and simple matching logic.

---

## Challenges Encountered

- Players looked visually similar, making appearance-based tracking difficult.
- No access to GPU, so all processing was done on CPU, resulting in slower inference (around 1.5–2 seconds/frame).
- The YOLOv11 model could not use appearance embeddings.
- Limited re-identification as multiple players were labeled `Player 0` or `Player 1` incorrectly.

---

## What Remains

- Robust re-identification: Tracking player identities on re-entries was only partially successful.
- Adding OCR (jersey number recognition) would help distinguish similar-looking players. 

---

## Future Improvements (Given More Time/Resources)

- Integrate a multi-object tracker (like Deep SORT or ByteTrack).
- Extract visual embeddings for each player to improve identity matching.
- Leverage GPU for faster frame processing and real-time application.

---

## Summary

This baseline version achieves simple player tracking using YOLOv11 but falls short on robust re-identification. It serves as a starting point for integrating more advanced methods like OCR, embedding-based tracking, and multi-object trackers.

