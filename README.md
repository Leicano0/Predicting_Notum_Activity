# Predicting Notum Inhibitor Activity

## Aim

Build a model to predict how strongly a molecule would inhibit Notum from its structure alone,
show how well it performs on chemical series it has never seen

## Introduction

Notum is in the Wnt-pathway brake that I have presented on in a group project.
Blocking it is a proposed Alzheimer's strategy, so the target is current and its biology is well understood.

## The data

I queried the ChEMBL API before planning (data accessed on 10/11/26):

| Fact | Value |
| --- | --- |
| Target ID (human) | **CHEMBL3714531** |
| Activity records with a pChEMBL value | 783 |
| Unique molecules | **637** |
| Source papers | 15 |
| Measurement types | IC50 (670), EC50 (112), Kd (1) |
| pChEMBL range | 3.51 – 10.29 (mean 6.37) |
| Mouse target (ignore) | CHEMBL3758064, only 60 records |

The data is saved as `notum_raw.csv`, therefore results should be reproducible.

