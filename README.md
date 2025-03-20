# 🧬 Evolução Computacional: Três Desafios com Algoritmos Genéticos

Este projeto explora o poder dos algoritmos genéticos para resolver três desafios clássicos e intrigantes: **Ajuste de Modelo Linear**, **Reprodução de Imagens** e **Problema da Mochila**. Tudo isso usando a biblioteca **PyGAD**.

---

## 🚀 Tecnologias Utilizadas
- **Python 3.x**
- **PyGAD**
- **NumPy**
- **Matplotlib**
- **ImageIO**

Instale as dependências com:
```bash
pip install pygad numpy matplotlib imageio
```

---

## 🎯 Desafio 1: Ajuste de Modelo Linear
O objetivo é encontrar os melhores pesos para um conjunto de entradas e atingir uma saída desejada.

🔧 **Parâmetros Principais:**
- `function_inputs`: Valores de entrada
- `desired_output`: Saída esperada
- `sol_per_pop`: Número de soluções por população
- `num_generations`: Número de gerações
- `mutation_percent_genes`: Percentual de mutação nos genes

⚙️ **Função de Fitness:**
```python
fitness = 1.0 / numpy.abs(output - desired_output)
```

🔍 **Resultado:** O código encontra os pesos ideais para minimizar o erro.

---

## 🖼️ Desafio 2: Reprodução de Imagens
Aqui, o algoritmo tenta recriar uma imagem alvo evoluindo seus pixels.

🔧 **Etapas Principais:**
1. Carrega a imagem (`img/fruit2.jpg`) e a transforma em um cromossomo.
2. Define uma função de fitness para medir a semelhança da imagem gerada com a original.

⚙️ **Função de Fitness:**
```python
fitness = numpy.sum(target_chromosome) - numpy.sum(numpy.abs(target_chromosome-solution))
```

📸 **Resultado:** Após 20.000 gerações, a imagem final se aproxima da original.

---

## 🎒 Desafio 3: Problema da Mochila
O clássico problema de otimização: selecione produtos para maximizar o valor total sem ultrapassar o limite de peso.

🔧 **Parâmetros:**
- `peso_produtos`: Lista de pesos dos itens
- `valor_produtos`: Lista de valores dos itens
- `peso_permitido_produtos`: Peso máximo da mochila
- `num_linhas`: Número de soluções por população
- `num_generations`: Número de gerações

⚙️ **Função de Fitness:**
```python
fitness = (valor_produtos_selecionados * 10) - (peso_permitido_produtos * (peso_ultrapassado ** 2))
```

🎯 **Resultado:** O algoritmo retorna a melhor combinação de itens com o maior valor possível.

---

## 📊 Visualização
Cada desafio gera um gráfico mostrando como a **fitness** evolui ao longo das gerações:

```python
ga_instance.plot_fitness()
```

Para a reprodução de imagem, o código também exibe a imagem final evoluída.

---

## 📝 Notas Finais
- 🔍 **Certifique-se** de que o caminho da imagem está correto (`img/fruit2.jpg`).
- 🛠️ **Ajuste parâmetros** como taxa de mutação e número de gerações para experimentar diferentes desempenhos.
- 🧠 **Explore e modifique o código** para testar novos cenários e entender o comportamento dos algoritmos genéticos.

🎉 **Divirta-se evoluindo soluções!**

