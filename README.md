<p align="center">
<a href="https://www.fiap.com.br/">
  <img src="https://upload.wikimedia.org/wikipedia/commons/d/d4/Fiap-logo-novo.jpg" alt="FIAP Logo" width="160px">
</a>
</p>

<br>

# 🌾 FarmTech Solutions — Fase 6: Sistema de Visão Computacional com YOLO

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python" />
  <img src="https://img.shields.io/badge/YOLOv5-Ultralytics-red?logo=github" />
  <img src="https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=white" />
  <img src="https://img.shields.io/badge/Status-Em%20desenvolvimento-yellow" />
  <img src="https://img.shields.io/badge/FIAP-Fase%206-orange" />
</p>

---

## 👨‍🎓 Integrantes

| Nome | RM |
|------|-----|
| _(Seu Nome Completo)_ | RM XXXXX |
| _(Nome do Integrante 2)_ | RM XXXXX |
| _(Nome do Integrante 3)_ | RM XXXXX |

---

## 👩‍🏫 Professores

| Tipo | Nome |
|------|------|
| Tutor(a) | _(Nome do tutor)_ |
| Coordenador(a) | _(Nome do coordenador)_ |

---

## 📜 Descrição do Projeto

A **FarmTech Solutions** está expandindo seus serviços de IA para além do agronegócio. Nesta fase, o grupo atua como parte do time de desenvolvedores da empresa, visitando um cliente interessado em entender na prática como funciona um sistema de **visão computacional**.

O projeto desenvolve um **sistema de detecção de objetos** utilizando a arquitetura **YOLOv5**, capaz de identificar e classificar dois tipos de objetos distintos em imagens. O objetivo é demonstrar o potencial e a acurácia de um sistema de visão computacional moderno, comparando diferentes configurações de treinamento.

### Contexto

> _"Você é livre para escolher o cenário de imagens que servirá para a etapa de treinamento, validação e testes."_ — Enunciado da Fase 6

Os objetos escolhidos para este projeto foram:

- **Classe A:** `[OBJETO_A — a ser definido]`
- **Classe B:** `[OBJETO_B — a ser definido]`

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
└── assets/
    └── prints/                        ← Screenshots das imagens de teste processadas
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

### Pré-requisitos

- Conta Google (para uso do Colab e Drive)
- Acesso ao [Google Colab](https://colab.research.google.com/)

### Passo a passo

1. **Acesse o notebook** pelo link abaixo:
   > 📓 **[Abrir no Google Colab](#)** ← _(inserir link do Colab aqui)_

2. **Faça uma cópia** do notebook para o seu Drive (`Arquivo > Salvar uma cópia no Drive`)

3. **Execute as células em ordem**, do início ao fim. O notebook irá:
   - Montar o Google Drive
   - Instalar as dependências (YOLOv5, ultralytics)
   - Configurar o dataset
   - Realizar o treinamento em duas configurações de épocas
   - Exibir os resultados e métricas
   - Rodar a inferência nas imagens de teste

4. **Não é necessário** baixar nada manualmente — tudo é feito dentro do Colab.

---

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

| Configuração | mAP@0.5 | Precision | Recall | Tempo de Treino |
|--------------|---------|-----------|--------|-----------------|
| 30 épocas | _%_ | _%_ | _%_ | _min_ |
| 60 épocas | _%_ | _%_ | _%_ | _min_ |

_(Tabela preenchida após execução do notebook)_

### Prints das imagens de teste

> Imagens geradas pelo modelo após a inferência estão disponíveis em `/assets/prints/` e também exibidas no notebook.

---

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
| Notebook no Colab | _(a inserir)_ |
| Dataset no Google Drive | _(a inserir)_ |
| Vídeo no YouTube | _(a inserir)_ |
| Make Sense IA | https://www.makesense.ai/ |
| YOLOv5 (Ultralytics) | https://github.com/ultralytics/yolov5 |

---

## 🛠️ Tecnologias Utilizadas

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white" />
  <img src="https://img.shields.io/badge/YOLOv5-FF4500?logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=white" />
  <img src="https://img.shields.io/badge/Google%20Drive-4285F4?logo=googledrive&logoColor=white" />
  <img src="https://img.shields.io/badge/Make%20Sense%20IA-4CAF50" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white" />
  <img src="https://img.shields.io/badge/Matplotlib-11557C" />
</p>

---

## 📋 Licença

<img alt="FIAP License" src="https://img.shields.io/badge/license-FIAP-red" />

Desenvolvido como projeto acadêmico para a **FIAP — Fase 6 / PBL**.  
Proibida a reprodução ou uso fora do contexto acadêmico sem autorização.

---

<p align="center">
  Feito com ❤️ pela equipe FarmTech Solutions • FIAP 2025
</p>
