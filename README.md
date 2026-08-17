# AI Worker - Face Verification Service

## Overview

This service verifies whether the face shown in a user's selfie video matches the face shown on the front image of their National ID card.

### The system performs:

### 1. Face extraction from National ID image
### 2. Face extraction from video frames
### 3. Face embedding generation
### 4. Face similarity comparison
### 5. Basic liveness detection
### 6. Verification result generation

---

# Technology Stack

## Backend Framework

### FastAPI ,  ### Python 3.11.5

Purpose:

* REST API development
* File upload handling
* JSON responses

Package:

```bash
pip install fastapi uvicorn
```

---

## Computer Vision

### OpenCV

Purpose:

* Read images
* Read videos
* Extract frames
* Image preprocessing

### Package:

```bash
pip install opencv-python
```

Used in:

```python
import cv2
```

---

### NumPy

Purpose:

* Matrix operations
* Vector calculations
* Face embedding manipulation

Package:

```bash
pip install numpy
```

Used in:

```python
import numpy as np
```

---

## Face Recognition

### InsightFace

Purpose:

* Face detection
* Face alignment
* Face embeddings
* Face recognition

Model:

```text
buffalo_l
```

Main output:

```python
face.embedding
```

Embedding size:

```text
512 dimensions
```

Used in:

```python
from insightface.app import FaceAnalysis
```

---

## Liveness Detection

### MediaPipe

Purpose:

* Face detection
* Face landmarks
* Blink detection (future upgrade)
* Head movement tracking (future upgrade)

Package:

```bash
pip install mediapipe
```

Used in:

```python
import mediapipe as mp
```

Current implementation:

```text
Basic motion-based liveness detection
```


