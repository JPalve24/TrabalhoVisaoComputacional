# Trabalho de Visão Computacional — Detecção de camisa vermelha

Trabalho acadêmico da disciplina de Visão Computacional.

## Objetivo

Detectar pessoas em imagens e identificar possíveis pessoas usando camisa vermelha por meio de detecção de objetos com YOLO e análise de cor com OpenCV.

## Tecnologias

- Python
- Ultralytics YOLOv8
- OpenCV
- NumPy
- Matplotlib
- Google Colab / Google Drive

## Estrutura do repositório

```text
TrabalhoVisaoComputacional/
├── notebooks/
│   └── deteccao_camisa_vermelha.ipynb
├── outputs/
│   └── .gitkeep
├── src/
│   └── README.md
├── .gitignore
├── requirements.txt
└── README.md
```

## Como executar

1. Abra o notebook `notebooks/deteccao_camisa_vermelha.ipynb` no Google Colab.
2. Coloque as imagens de entrada `Image 01` até `Image 08` na pasta `Meu Drive/Trabalho Visão Computacional`.
3. Execute as células na ordem.
4. Autorize o acesso ao Google Drive quando solicitado.
5. O notebook processará as imagens e salvará os resultados na pasta `Meu Drive/Trabalho Visão Computacional/outputs`.

## Critérios utilizados

- O modelo YOLO detecta pessoas (classe `person`) com confiança superior a 60%.
- O OpenCV analisa tons vermelhos em uma região aproximada do tronco.
- A caixa é desenhada quando pelo menos 20% dos pixels dessa região são classificados como vermelhos.

## Limitações

A região do tronco é uma aproximação, não uma segmentação precisa da camisa. O percentual de pixels vermelhos não representa a probabilidade de a pessoa estar usando camisa vermelha. Estampas, iluminação, objetos vermelhos próximos e oclusões podem causar falsos positivos ou falsos negativos. Os resultados devem ser interpretados como uma heurística visual.

## Resultados

Adicione à pasta `outputs/` as imagens geradas pelo notebook (`Resultado_Image_01.jpg` até `Resultado_Image_08.jpg`). O repositório inicial contém apenas um arquivo `.gitkeep` nessa pasta, pois as imagens precisam ser copiadas após a execução do notebook.

## Dependências

As dependências principais estão listadas em `requirements.txt`. No Google Colab, o notebook instala os pacotes necessários na primeira célula.

## Uso acadêmico

Projeto desenvolvido para fins educacionais na disciplina de Visão Computacional.
