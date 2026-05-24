# Devlog for MPW3

A development log note for keeping track of steps & milestones during development.

## 2026-05-18

> Maurizio

Initial setup and first steps with the provided exercise.

First and foremost trying to get the full picture of the actual assignment.

Implementation of the model (a) as described in the paper [Show and Tell](ShowAndTell_2015.pdf):

- Pretrained CNN-based Encoder: Encoding images into internal representation
- LSTM-based Decoder / Generator: Read internal image representation and infer/generate caption

## 2026-05-23

> Joël

New implementations:
- Bleu1 and Bleu2 as function
- Plot function, building upon thre reuseable training loop (see below)

Refactor and changes on existing code:
- Moved training loop to reuseable function
- Added loss history for train and test
- Added bleu history

## 2026-05-24

> Joël

New implementations:
- Sample generator for visual sanity check of model

Fixes and refactor:
- Fixed some bugs in the training loop
- Minor changes to improve code