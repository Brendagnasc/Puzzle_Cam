# Puzzle Cam

Jogo interativo de quebra-cabeça controlado por gestos das mãos, usando visão computacional em tempo real no navegador.

Demo: https://brendagnasc.github.io/puzzle-cam/

## Como funciona

1. A webcam detecta suas mãos em tempo real
2. Uma contagem regressiva captura sua foto
3. A foto é dividida em peças embaralhadas
4. Você monta o quebra-cabeça arrastando as peças no ar com gesto de pinça

## Visão computacional

- **Detecção de mãos**: MediaPipe Hands, modelo de deep learning que estima 21 pontos de referência (landmarks) da mão por frame de vídeo
- **Reconhecimento de gestos**: o gesto de pinça é detectado pela distância euclidiana entre as pontas do polegar e do indicador, normalizada pelo tamanho da mão
- **Rastreamento em tempo real**: os landmarks são mapeados das coordenadas normalizadas do modelo para o espaço do canvas, com espelhamento horizontal para interação natural

## Tecnologias

- JavaScript puro (sem frameworks)
- MediaPipe Hands
- Canvas API

## Rodando localmente

```bash
python -m http.server 5500
```

Abra http://localhost:5500 e permita o acesso à webcam.

## Autora

Brenda Gabrielle Alves Nascimento — Ciência da Computação, UFOP
