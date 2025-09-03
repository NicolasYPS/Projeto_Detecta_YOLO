# Detecção de Objetos com YOLOv4 e Transfer Learning

Este projeto implementa um modelo de detecção de objetos personalizado utilizando **YOLOv4 (You Only Look Once)** com **transfer learning**, treinado sobre o framework **Darknet**. O objetivo é detectar objetos específicos em imagens com alta precisão, aproveitando um modelo pré-treinado (weights COCO) para acelerar o aprendizado e reduzir o tempo de convergência.
As classes escolhidas foram **Morango** e **Brocolis**

---

##  Visão Geral

- **Arquitetura**: YOLOv4 (customizada)
- **Framework**: Darknet
- **Técnica**: Transfer Learning (partida de `yolov4.weights` pré-treinado no COCO)
- **Resolução**: 512x512
- **Número de classes**: 2
- **Treinamento esperado**: 6000 iterações (batches)
- **Progresso atual**: 1000 iterações (em andamento)
- **Ambiente**: Google Colab (GPU Tesla T4)

---

##  Transfer Learning

Em vez de treinar o modelo do zero, utilizamos **pesos pré-treinados no dataset COCO** como ponto de partida. Isso permite:

- Aprendizado mais rápido  
- Melhor generalização com menos dados  
- Redução significativa de tempo e recursos computacionais

O modelo é então **ajustado finamente (fine-tuned)** com um dataset personalizado, adaptando-se às classes-alvo com apenas algumas milhares de iterações.

---

## Configurações do Modelo

### Hiperparâmetros principais (`yolov4_custom.cfg`)
```cfg
batch=64
subdivisions=64
width=512
height=512
learning_rate=0.0013
max_batches=6000
steps=4800,5400
classes=2
```

## Sobre o Autor

Projeto desenvolvido por **Nicolas**.  
Fique à vontade para colaborar, testar ou dar feedback!

[LinkedIn](https://www.linkedin.com/in/nicolas-y-p-souza) | [GitHub](https://github.com/NicolasYPS)
