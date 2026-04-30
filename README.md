<p align="center">
<a href="https://www.fiap.com.br/">
  <img src="https://upload.wikimedia.org/wikipedia/commons/d/d4/Fiap-logo-novo.jpg" alt="FIAP Logo" width="160px">
</a>
</p>

<br>

# 🌾 FarmTech Solutions — Fase 6: Sistema de Visão Computacional com YOLO

---

## 👨‍🎓 Integrantes

| Nome | RM |
|------|-----|
| Gustavo Borges Marinho Peres | RM 567477 |


---

## 📜 Descrição do Projeto

A **FarmTech Solutions** está expandindo seus serviços de IA para além do agronegócio. Nesta fase, o grupo atua como parte do time de desenvolvedores da empresa, visitando um cliente interessado em entender na prática como funciona um sistema de **visão computacional**.

O projeto desenvolve um **sistema de detecção de objetos** utilizando a arquitetura **YOLOv5**, capaz de identificar e classificar dois tipos de objetos distintos em imagens. O objetivo é demonstrar o potencial e a acurácia de um sistema de visão computacional moderno, comparando diferentes configurações de treinamento.

### Contexto

Os objetos escolhidos para este projeto foram:

- **Classe A:*Garrafa* 
- **Classe B:*Som* 

---

## 📁 Estrutura do Repositório

```
fase6-farmtech-yolo/
│
├── README.md                          ← Este arquivo
│
├── notebook/
│   └── NomeSobrenome_rmXXXXX_pbl_fase6.ipynb  ← Notebook principal (Colab)
│
├── dataset/
│   ├── images/
│   │   ├── train/                     ← 64 imagens de treino (32A + 32B)
│   │   ├── val/                       ← 8 imagens de validação (4A + 4B)
│   │   └── test/                      ← 8 imagens de teste (4A + 4B)
│   └── labels/
│       ├── train/                     ← Labels YOLO das imagens de treino
│       ├── val/                       ← Labels YOLO das imagens de validação
│       └── test/                      ← Labels YOLO das imagens de teste
│
├── data.yaml                          ← Arquivo de configuração do dataset YOLO
│
├── results/
│   ├── exp_30epochs/                  ← Resultados — 30 épocas
│   └── exp_60epochs/                  ← Resultados — 60 épocas
│

```

---

## 🗂️ Dataset

O dataset foi organizado manualmente e rotulado utilizando a ferramenta **[Make Sense IA](https://www.makesense.ai/)**.

| Split | Classe A | Classe B | Total |
|-------|----------|----------|-------|
| Treino | 32 | 32 | 64 |
| Validação | 4 | 4 | 8 |
| Teste | 4 | 4 | 8 |
| **Total** | **40** | **40** | **80** |

As imagens e labels estão armazenadas no **Google Drive** do grupo, conectado ao Colab via `drive.mount`.

---

## 🚀 Como Executar

### Passo a passo

1. **Acesse o notebook** pelo link abaixo:
   > 📓 **[Abrir no Google Colab](#)** ← https://colab.research.google.com/drive/1oG6Drbe4mRhXNc76KU8vYqv9En2IEWTh#scrollTo=6c0e6fe1

2. **Faça uma cópia** do notebook para o seu Drive (`Arquivo > Salvar uma cópia no Drive`)

3. **Execute as células em ordem**, do início ao fim. O notebook irá:
   - Montar o Google Drive
   - Instalar as dependências (YOLOv5, ultralytics)
   - Configurar o dataset
   - Realizar o treinamento em duas configurações de épocas
   - Exibir os resultados e métricas
   - Rodar a inferência nas imagens de teste


## 🧠 Metodologia

O projeto segue o pipeline completo de treinamento de uma rede YOLO customizada:

```
Coleta → Rotulação → Organização → Treinamento → Validação → Teste → Análise
```

### Etapas

| # | Etapa | Ferramenta |
|---|-------|-----------|
| 1 | Coleta de imagens (80 imagens) | Manual / web |
| 2 | Rotulação (bounding boxes) | Make Sense IA |
| 3 | Organização do dataset | Google Drive |
| 4 | Treinamento YOLOv5 | Google Colab + PyTorch |
| 5 | Validação (mAP, precision, recall) | YOLOv5 nativo |
| 6 | Inferência nas imagens de teste | YOLOv5 `detect.py` |
| 7 | Análise comparativa (30 vs 60 épocas) | Matplotlib / pandas |

---

## 📊 Resultados (resumo)

> Os resultados completos, com gráficos e prints das imagens processadas, estão detalhados no notebook.

| Configuração | mAP@0.5 | Precision | Recall 
|--------------|---------|-----------|--------
| 30 épocas | 0.9950% | 0.9613% | 1.0000% 
| 60 épocas | 0.9950% | 0.9765% | 1.0000% 

## 🎥 Vídeo de Demonstração

> 📺 **[Assistir no YouTube (não listado)](#)** ← _(inserir link aqui)_

Vídeo de até 5 minutos demonstrando:
- Estrutura do dataset
- Execução do treinamento no Colab
- Resultados das duas configurações de épocas
- Inferência nas imagens de teste

---

## 🔗 Links Importantes

| Recurso | Link |
|---------|------|
| Notebook no Colab | [_(a inserir)_](https://colab.research.google.com/drive/1oG6Drbe4mRhXNc76KU8vYqv9En2IEWTh#scrollTo=be8a8325) |
| Dataset no Google Drive | [_(a inserir)_](https://drive.google.com/drive/folders/1n3MPkPBAPAMKq4GeKvrNLLGgsJ-2n9dM?hl=pt-br) |
| Vídeo no YouTube | _(a inserir)_ |


---


---

## 📋 Licença

<img alt="FIAP License" src="https://img.shields.io/badge/license-FIAP-red" />

Desenvolvido como projeto acadêmico para a **FIAP — Fase 6 / PBL**.  
Proibida a reprodução ou uso fora do contexto acadêmico sem autorização.

---

<p align="center">
  Feito com ❤️ pela equipe FarmTech Solutions • FIAP 2025
</p>
