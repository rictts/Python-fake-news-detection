# 📰 Deteção de Fake News em Saúde Cardiovascular

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)

Este projeto implementa um modelo de **Processamento de Linguagem Natural (NLP)** e **Aprendizagem Automática (Machine Learning)** para classificar títulos de notícias (*headlines*) sobre saúde cardiovascular como **Reais** ou **Falsas (Fake News)**.

---

## 📌 Funcionalidades

- **Extração de Dados:** Leitura e extração direta de tabelas a partir de ficheiros `.docx` (`dataset.docx`).
- **Vetorização de Texto:** Transformação de texto em matrizes numéricas utilizando **TF-IDF** (*Term Frequency-Inverse Document Frequency*).
- **Classificação:** Treino de um modelo de **Regressão Logística** para previsão binária (`Real` vs `Fake`).
- **Avaliação de Testes:** Suíte de testes integrada com 20 cenários divididos por níveis de complexidade (fáceis, médios, difíceis, ambíguos e extra).
- **Modo Interativo:** Prompt de linha de comandos (CLI) para testar *headlines* personalizadas em tempo real com indicação da percentagem de confiança.

---

## 📂 Estrutura do Ficheiro de Dados

O script espera encontrar na raiz do projeto um ficheiro chamado `dataset.docx` contendo tabelas organizadas com a seguinte estrutura mínima:
- **Coluna 2 (índice 1):** Título da notícia (*Headline*).
- **Coluna 5 (índice 4):** Rótulo (`Fake` ou `Real`).

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

- **[Python 3.x](https://www.python.org/):** Linguagem principal do projeto.
- **[pandas](https://pandas.pydata.org/):** Manipulação e estruturação de dados.
- **[python-docx](https://python-docx.readthedocs.io/):** Extração de conteúdo de ficheiros `.docx`.
- **[scikit-learn](https://scikit-learn.org/):** 
  - `TfidfVectorizer` para extração de características textuais.
  - `LogisticRegression` para treino do classificador.

---

## 🚀 Como Executar o Projeto

### 1. Pré-requisitos
Garante que tens o Python instalado no teu sistema. 

### 2. Clonar o Repositório
```bash
git clone https://github.com/teu-usuario/teu-repositorio.git
cd teu-repositorio
```

### 3. Instalar as Dependências
Instala as bibliotecas necessárias executando:
```bash
pip install pandas python-docx scikit-learn
```

### 4. Executar o Script
Certifica-te de que o ficheiro `dataset.docx` está presente na pasta e executa:
```bash
python Codigo_dados_versao_2.py
```

---

## 🔬 Exemplo de Funcionamento

Ao executar o script:
1. O dataset é carregado e processado.
2. O modelo é treinado.
3. É apresentada a avaliação detalhada dos 20 casos de teste com respetivas percentagens de confiança e taxa de precisão global.
4. É aberto o **modo interativo**:

```text
Introduza uma headline (or 'sair'): Garlic tea completely prevents heart attacks forever
Resultado: Fake News (98.42% confiança)

Introduza uma headline (or 'sair'): Doctors recommend regular exercise for heart health
Resultado: Real News (95.10% confiança)
```
