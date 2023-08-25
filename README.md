# EsViT Histopathology Image Retrieval

## Description

This project implements an image retrieval system for histopathology images using the EsViT (Efficient Self-supervised Vision Transformers) model. The goal is to retrieve similar histopathology images given a query image.

## Model

EsViT is a self-supervised vision transformer model designed for representation learning. It incorporates ideas from vision transformers (ViT) and autoencoders to learn useful visual features from unlabeled images. 

Key aspects of EsViT include patchification, masking, and an asymmetric encoder-decoder structure. These allow the model to reconstruct masked image patches and learn robust representations.

In this project, an EsViT model pre-trained on ImageNet is used as the image encoder. Histopathology images are passed through to generate feature vectors for indexing and retrieval.

## Datasets

The model is trained and evaluated on these histopathology image datasets:

- [BracS](https://www.bracs.icar.cnr.it/) - Breast Cancer Histopathology Images
- [CRC](https://warwick.ac.uk/fac/cross\_fac/tia/data/extended\_crc\_grading/) - Colorectal Cancer Histopathology Images  
- [BATCH](https://iciar2018-challenge.grand-challenge.org/Dataset/) - BreAst Cancer Histology Images

## Usage

The system allows uploading a query histology image. It indexes the datasets based on EsViT features to find the most similar images. The top k retrieved images are returned, ranked by similarity.

The project provides code to fine-tune EsViT on histopathology data and utilities for indexing/retrieval. 

## References

[EsViT Paper](https://arxiv.org/abs/2106.09785)
