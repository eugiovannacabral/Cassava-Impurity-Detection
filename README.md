# 🌿 Detecção de Impurezas em Esteiras de Mandioca

### Visão computacional aplicada à produção de polvilho azedo

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Ultralytics](https://img.shields.io/badge/Ultralytics-111F68?style=for-the-badge)
![YOLO11m](https://img.shields.io/badge/YOLO11m-00A98F?style=for-the-badge)
![Roboflow](https://img.shields.io/badge/Roboflow-6706CE?style=for-the-badge&logo=roboflow&logoColor=white)
![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)

## 📌 Sobre o projeto

Projeto de iniciação científica iniciado em 2025 no Instituto Nacional
de Telecomunicações (Inatel), desenvolvido por Giovanna C. R. Mesquita
e Layla V. S. Teles.

A pesquisa investiga o uso de visão computacional para detectar
impurezas em esteiras de seleção de mandioca utilizadas na produção
de polvilho azedo.

O trabalho envolveu a construção de um dataset próprio com imagens
coletadas em ambiente industrial, a anotação dos objetos, o treinamento
de um modelo de detecção e a avaliação dos resultados.

## 🎯 Objetivo

Identificar mandiocas e fragmentos de madeira presentes na esteira,
apoiando a inspeção da matéria-prima antes da moagem e contribuindo
para a proteção dos equipamentos e a qualidade do produto.

## 🛠️ Tecnologias utilizadas

| Tecnologia | Aplicação |
| --- | --- |
| **Python** | Desenvolvimento dos experimentos |
| **Ultralytics** | Biblioteca utilizada para trabalhar com o modelo YOLO |
| **YOLO11m** | Detecção e classificação dos objetos |
| **Roboflow** | Extração de frames, anotação e preparação do dataset |
| **Kaggle** | Ambiente de execução do treinamento |
| **Roboflow Workflows** | Integração e testes de detecção com câmera |

### Técnicas empregadas

- Transfer learning.
- Fine-tuning.
- Data augmentation.
- Anotação com bounding boxes.
- Avaliação por precision, recall, mAP e matriz de confusão.

## 📸 Dataset próprio

As imagens foram obtidas a partir de vídeos gravados em unidades
de produção de polvilho em **Conceição dos Ouros, Minas Gerais**,
contemplando diferentes ângulos e condições de iluminação.

| Característica | Descrição |
| --- | --- |
| Material coletado | Aproximadamente 200 minutos de vídeo a 60 fps |
| Imagens anotadas inicialmente | 1.094 |
| Total após ampliação de dados, conforme o artigo | 1.685 imagens |
| Classes | Mandioca e madeira |
| Divisão informada | 70% treinamento, 20% validação e 10% teste |
| Ampliação de dados | Rotação de 90°, redimensionamento e variação de brilho |

O conjunto apresenta maior quantidade de objetos da classe mandioca,
refletindo a predominância das raízes na esteira de produção.

> O acesso ao dataset e suas condições de uso serão documentados
> conforme a definição de compartilhamento dos materiais do projeto.

## 🔬 Metodologia

1. Coleta de vídeos das esteiras em ambiente industrial.
2. Seleção de trechos e extração de frames.
3. Anotação das classes mandioca e madeira.
4. Preparação e ampliação do dataset.
5. Treinamento do YOLO11m utilizando transfer learning.
6. Avaliação das métricas e análise visual das predições.
7. Testes com câmera de dispositivo móvel via Roboflow Workflows.

O treinamento descrito no artigo foi configurado para **150 épocas**.
O checkpoint `best.pt` foi selecionado para a etapa de predição.

O artigo também descreve um treinamento na plataforma Roboflow
para disponibilizar o modelo utilizado no Workflow. Essa etapa deve
ser documentada separadamente dos experimentos realizados no Kaggle.

## 📊 Resultados

| Indicador | Resultado reportado no artigo |
| --- | --- |
| Precisão (precision) | Aproximadamente 80% |
| Revocação (recall) | Superior a 80%, conforme o resumo e a conclusão |
| Saída das predições | Classes, caixas delimitadoras e confiança |
| Validação prática | Testes com câmera via Roboflow Workflows |

Os indicadores apresentados resumem os resultados reportados no
artigo e não representam métricas exclusivas da classe madeira.

Também foram analisadas a matriz de confusão, as curvas de perda
e as métricas mAP@50 e mAP@50–95.

## ⚠️ Limitações

- Desbalanceamento entre as classes mandioca e madeira.
- Semelhança visual entre raízes e fragmentos de madeira.
- Dificuldades em determinadas condições de iluminação e contraste.
- Necessidade de ampliar a avaliação em novos cenários de produção.

## 🚀 Possibilidades de evolução

- Ampliar o dataset e a diversidade de impurezas.
- Melhorar a detecção da classe madeira.
- Avaliar o desempenho em novos ambientes.
- Medir latência e velocidade de inferência.
- Investigar execução embarcada em Raspberry Pi.
- Integrar alertas para auxiliar os operadores.

## 👩‍💻 Autoria

**Desenvolvimento discente:**

- Giovanna C. R. Mesquita.
- Layla V. S. Teles.

**Instituição:** Instituto Nacional de Telecomunicações — Inatel.

**Início da pesquisa:** 2025.

## 📄 Artigo associado

*Computer Vision Real-Time Impurity Detection in Sour Cassava
Starch Production*

**Autores:** Giovanna C. R. Mesquita, Layla V. S. Teles,
Mateus R. Cruz, Samuel B. Mafra e William O. F. Carvalho.

## 📜 Licenciamento

A licença do código e as condições de uso do dataset, dos pesos
e do artigo serão informadas após definição com os responsáveis
pelo projeto.
