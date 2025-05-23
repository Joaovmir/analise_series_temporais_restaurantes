# Análise de Séries Temporais ✨📈

[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)

Projeto de **análise de séries temporais** para dados de restaurantes, utilizando Python e bibliotecas modernas de ciência de dados. O notebook principal demonstra técnicas de manipulação, visualização e análise de dados, explorando padrões de clientes ao longo do tempo e o impacto de datas comemorativas no movimento dos restaurantes.

---

## ✨ Visão Geral

Este repositório apresenta uma solução prática para análise de séries temporais, permitindo:

- Carregamento e exploração de dados reais de clientes em restaurantes.
- Análise do comportamento ao longo do tempo.
- Estudo do impacto de datas comemorativas em padrões de consumo.
- Visualização interativa e insights para tomada de decisão em negócios.

---

## 📚 Tecnologias Utilizadas

- [Python 3.8+](https://www.python.org/)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)

---

## ⚡ Instalação e Uso

### 1. Clone o repositório

```bash
git clone https://github.com/Joaovmir/analise_series_temporais.git
cd analise_series_temporais
````

### 2. Instale as dependências

No Google Colab, execute as células iniciais do notebook.

Para uso local, execute:

```bash
pip install pandas matplotlib seaborn
```

### 3. Estrutura de Dados

Certifique-se de que a pasta `dados/` está no diretório raiz do projeto e contém:

* `clientes_restaurantes.csv`
  Dados de movimentação de clientes nos restaurantes.

* `datas_comemorativas.csv`
  Datas especiais para análise de comportamento de consumo.

### 4. Execute o notebook

Abra e execute o arquivo `Análise_de_séries_temporais.ipynb` em seu ambiente favorito (Jupyter, VS Code ou Colab).

---

## 💡 Exemplo de Uso

### Leitura dos dados

```python
import pandas as pd

clientes = pd.read_csv('dados/clientes_restaurantes.csv')
datas = pd.read_csv('dados/datas_comemorativas.csv')

print(clientes.head())
print(datas.head())
```

### Visualização rápida

```python
import matplotlib.pyplot as plt

clientes['data'] = pd.to_datetime(clientes['data'])
clientes.groupby('data')['qtd_clientes'].sum().plot(figsize=(10,5))
plt.title("Movimento de clientes por dia")
plt.ylabel("Quantidade de clientes")
plt.xlabel("Data")
plt.show()
```

---

## 📁 Estrutura do Projeto

```
analise_series_temporais/
├── Análise_de_séries_temporais.ipynb
├── dados/
│   ├── clientes_restaurantes.csv
│   └── datas_comemorativas.csv
├── README.md
```
