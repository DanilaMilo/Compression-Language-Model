# DistillationNLP

Results of methods.
Base model - DeepPavlov/rubert-base-cased-conversational
| Method | Size MB | F1_Score | GPU time inf. sec. | CPU time inf. sec. | Size model difference |
| ------------- | ------------- |  ------------- |  ------------- |  ------------- |  ------------- |
| No one  | 711 | 0.966 | 0.036 | 1.51 | 0% |  
| Quantization of Linear Layers | 454 | 0.966 | N/A | 1.18 | 56% |
| Quantization of Linear and Embedding Layers | 179 | 0.966 | N/A | 1.13 | 397% |
| Tucker Decomposition of Linear Layers | 385 | 0.966 | 0.036 | 0.78 | 84% |
| Tucker Decomposition of Linear Layers + Emb. Quantization | 109 | 0.967 | N/A | 0.817 | 652% |
| Model Distillation | 10.3 | 0.952 | 0.005 | 0.12 | 6900% |
| Quantization Linears and Emb. Layers | 2.68 | 0.952 | N/A | 0.105 | 26529% |
| Model Distillation + Tucker Decomposition | 3.43 | 0.961 | 0.02 | 0.11 | 20700% |
| Model Distillation + Tucker Decomposition + Quantization Emb. Layer | 1.69 | 0.958 | N/A | 0.1 | 42000% |

All calculations were carried out on Free Colab

Jupyter Notebook summary:
  Tested methods compression of models:
    - Quantization
    - Layer Decomposition
    - Distillation
  And combination of these methods
