# Trabalho de Visão Computacional — Detecção de Camisa Vermelha

Trabalho acadêmico da disciplina de Visão Computacional, com o objetivo de detectar pessoas e identificar aquelas que possivelmente estão usando camisas vermelhas em imagens.

## Objetivo

Utilizar o modelo YOLOv8 para detectar pessoas nas imagens e o OpenCV para analisar a presença de tons vermelhos na região aproximada do tronco.

## Tecnologias

- Python
- Ultralytics YOLOv8
- OpenCV
- NumPy
- Matplotlib
- Google Colab

## Estrutura do repositório

```text
TrabalhoVisaoComputacional/
├── images/
│   ├── Image 01.jpg
│   ├── Image 02.jpg
│   └── ... (demais imagens de entrada)
├── notebooks/
│   └── Trabalho de Visão Computacional - João Paulo Alves.ipynb
├── outputs/
│   ├── Resultado_Image_01.jpg
│   └── ... (demais imagens processadas)
├── src/
│   └── README.md
├── .gitignore
├── requirements.txt
└── README.md
```

## Como executar

1. Clone ou baixe este repositório.
2. Abra o notebook `notebooks/Trabalho de Visão Computacional - João Paulo Alves.ipynb` no Google Colab.
3. Certifique-se de que as imagens originais, de `Image 01` até `Image 08`, estejam na pasta `images/`.
4. Execute as células do notebook na ordem indicada.
5. Aguarde o processamento das imagens.
6. Consulte os resultados gerados na pasta `outputs/`.

**Observação:** o notebook deve ser executado com o diretório do projeto configurado corretamente. Na primeira execução, o Ultralytics poderá baixar automaticamente os pesos do modelo `yolov8m.pt`.

## Critérios utilizados

- O YOLOv8 detecta pessoas utilizando a classe `person` (`classes=[0]`).
- São consideradas apenas detecções com confiança estritamente superior a 60%.
- O OpenCV converte a região aproximada do tronco para o espaço de cores HSV e identifica tons vermelhos.
- Uma pessoa é classificada como possível usuária de camisa vermelha quando pelo menos 20% dos pixels da região analisada são classificados como vermelhos.
- As detecções selecionadas são destacadas com caixas verdes e rótulos contendo a confiança do YOLO.

## Resultados

As imagens processadas são salvas na pasta `outputs/`, com nomes de `Resultado_Image_01.jpg` até `Resultado_Image_08.jpg`.

Os resultados podem variar conforme a iluminação, a qualidade das imagens, as cores presentes no ambiente e a precisão da detecção da pessoa.

## Limitações

A região do tronco é estimada a partir da caixa delimitadora da pessoa detectada pelo YOLO, não sendo uma segmentação precisa da camisa.

O percentual de pixels vermelhos é um critério heurístico e não representa a probabilidade de a pessoa estar usando uma camisa vermelha. Estampas, iluminação, objetos vermelhos próximos, oclusões e erros no recorte podem produzir falsos positivos ou falsos negativos.

A confiança exibida no rótulo corresponde à detecção da pessoa pelo YOLO, e não à classificação da cor da camisa.

## Dependências

As principais dependências estão listadas no arquivo `requirements.txt`. No Google Colab, os pacotes também podem ser instalados pela primeira célula do notebook.

## Uso acadêmico

Projeto desenvolvido para fins educacionais na disciplina de Visão Computacional.
