# Estrudo dos Efeitos da Densidade de Vacâncias na Estrutura de Bandas de Materiais Bidimensionais via Modelo Tight-Binding

Este repositório contém o código em Python (.ipynb) utilizado para gerar os resultados apresentados no trabalho "Estudo dos Efeitos da Densidade de Vacâncias na Estrutura de Bandas de Materiais Bidimensionais via Modelo Tight-Binding".

O código utiliza a biblioteca `PythTB` para implementar um modelo tight-binding simplificado que simula a estrutura eletrônica de materiais 2D (como TMDs) na presença de vacâncias.

## 🔬 Sobre o Modelo

O objetivo é estudar como a estrutura de bandas do material evolui de um regime de vacâncias isoladas para um regime de alta densidade de vacâncias.

Para isso, o sistema é modelado da seguinte forma:
* **Célula Unitária:** Cada célula unitária contém três sítios (orbitais), representando os estados eletrônicos localizados no entorno de uma vacância.
* **Hoppings:**
    * `t`: É o parâmetro de hopping *intra-célula*, conectando os três sítios dentro da mesma célula unitária (formando um triângulo).
    * `u`: É o parâmetro de hopping *inter-celular*, conectando sítios equivalentes em células vizinhas.
* **Parâmetro $\alpha$ (Alpha):** Este é o parâmetroEle representa a "densidade" ou proximidade das vacâncias, controlando a força do hopping inter-celular: $u = \alpha \cdot t$.
    * **$\alpha = 0$:** Representa vacâncias isoladas. Não há hopping entre as células (`u = 0`), e o resultado são bandas de energia planas (estados localizados).
    * **$\alpha > 0$:** Representa vacâncias que interagem. O hopping `u` aumenta, e os estados eletrônicos se hibridizam, gerando bandas com dispersão.
    * **$\alpha = 1$:** Representa o regime de alta densidade, com forte acoplamento entre as células.

## 💻 Como Executar o Código

### Pré-requisitos

O script requer as seguintes bibliotecas Python:
* `pythtb`
* `numpy`
* `matplotlib`

Você pode instalá-las usando `pip`:
```bash
pip install pythtb numpy matplotlib
