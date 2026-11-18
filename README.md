# Group 3 CurricularFace Face Recognition

A deep learning course project that recognizes four enrolled identities and rejects faces that do not meet a calibrated recognition threshold. The implementation is provided as a Jupyter notebook.

## Approach

- InceptionResnetV1 pretrained on VGGFace2 for 512-dimensional face embeddings
- A custom CurricularFace classification head
- Fine-tuning of the final backbone blocks
- MTCNN face detection and cropping for webcam inference
- Validation-based threshold calibration with Labeled Faces in the Wild (LFW) unknown identities

## Dataset and privacy

The face dataset, trained checkpoint, LFW cache, and screenshots are not included in this repository. They contain biometric data or outputs derived from it. To run the notebook, provide your own authorized dataset locally using this structure:

```text
data/
  train/member_1/ ... member_4/
  validate/member_1/ ... member_4/
  test/member_1/ ... member_4/
```

Use the notebook's dataset setup section to point `ZIP_PATH` to your local dataset archive. The notebook and results folders are excluded from Git by `.gitignore`.

## Setup

Install Python dependencies in an environment compatible with your PyTorch and CUDA setup:

```bash
python -m pip install -r requirements.txt
```

Open `Group_3.ipynb`, update the local dataset path if needed, and run the cells in order. Webcam inference requires a working camera.

## Team

Group 3

