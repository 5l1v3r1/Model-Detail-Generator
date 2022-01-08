# Model-Detail-Generator
Autoregressive Generative Model of 3D Meshes

This is a generative model of 3D meshes that sequentially outputs mesh
vertices and faces. This Model  consists of two parts: A vertex model, that
unconditionally models mesh vertices, and a face model, that models the mesh
faces conditioned on input vertices. The vertex model uses a masked Transformer
decoder to express a distribution over the vertex sequences.

In this repository the data and module is cloned from **Deepmind-research** Colabs that demo
training PolyGen from scratch on a toy dataset, as well as sampling from a
pre-trained model is provided here.

*Training is only with shifting augmentation<br/>
*I have  used [ReZero](https://arxiv.org/abs/2003.04887) which improves training speed.<br/>
*Added global information (e.g. class label embeddings) as an additional input in the first sequence.

## Training Colab [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1EkMYbgjM_Xad4uSRQ31IJZgQwVuQX829?usp=sharing)

To train a PolyGen model from scratch on a collection of simple meshes use this
colab. This demonstrates the data pre-processing required to create inputs for
the vertex and face models.
