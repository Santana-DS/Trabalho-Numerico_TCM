# Análise Numérica da Equação do Calor 1d Transiente com Diferentes Condições de Contorno e Iniciais

Este projeto tem como objetivo resolver a equação do calor unidimensional transiente utilizando métodos numéricos e compará-la com soluções analíticas para diferentes problemas.

O código é desenvolvido em Python e utiliza bibliotecas como NumPy e Matplotlib para cálculos e visualizações no ambiente Jupyter Notebook.

___

## **Problema 1**

![Distribuição da Temperatura - Problema 1](Graficos_Gerados/gif_distribuicao_temperatura_3d_problema_1.gif)

$$
\frac{\partial T(x, t)}{\partial t} = \frac{\partial^2 T(x, t)}{\partial x^2}, \quad t > 0, \; 0 < x < 1
$$

Com as seguintes condições de contorno e iniciais:

$$
T(0, t) = 0, \quad T(1, t) = 0, \; t \ge 0
$$

$$
T(x, 0) = 1, \; 0 < x < 1
$$

Solução exata:

$$
T(x, t) = \sum_{n=1}^{\infty} \frac{4}{(2n - 1) \pi} \sin[(2n - 1) \pi x] \exp[-(2n - 1)^2 \pi^2 t]
$$

___

## **Problema 2**

![Distribuição da Temperatura - Problema 2](Graficos_Gerados/gif_distribuicao_temperatura_3d_problema_2.gif)

$$
\frac{\partial T(x, t)}{\partial t} = \frac{\partial^2 T(x, t)}{\partial x^2}, \quad t > 0, \; 0 < x < 1
$$

Com as seguintes condições de contorno e iniciais:

$$
T(0, t) = 1, \quad T(1, t) = 0, \quad t \geq 0
$$

$$
T(x, 0) = 0, \quad 0 < x < 1
$$

Solução exata:

$$
T(x, t) = 1 - x - \sum_{n=1}^{\infty} \frac{2}{n \pi} \sin(n \pi x) \exp(-n^2 \pi^2 t)
$$

___

## **Problema 3**

![Distribuição da Temperatura - Problema 3](Graficos_Gerados/gif_distribuicao_temperatura_3d_problema_3.gif)

$$
\frac{\partial T(x,t)}{\partial t} = \frac{\partial^2 T(x,t)}{\partial x^2}, \quad t > 0, \quad 0 < x < 2
$$

Com as seguintes condições de contorno e iniciais:

$$
T(0, t) = 0, \quad T(2, t) = 0, \quad t \geq 0
$$

$$
T(x, 0) = \sin\left(\frac{\pi}{2} x\right), \quad 0 < x < 2
$$

Solução exata:

$$
T(x, t) = \exp\left(-\frac{\pi^2 t}{4}\right) \sin\left(\frac{\pi}{2} x\right)
$$

## Requisitos

- Python 3.x
- Bibliotecas: `notebook`, `matplotlib`, `numpy`

    ```bash
    pip install pandas matplotlib IPython
   ```
  
## Uso

**Clone o Repositório**

   Clone este repositório para o seu ambiente local usando:

   ```bash
   git clone https://github.com/seu_usuario/seu_repositorio.git
   ```

**Para abrir o notebook Jupyter**

   ```bash
   python -m notebook
   ```
