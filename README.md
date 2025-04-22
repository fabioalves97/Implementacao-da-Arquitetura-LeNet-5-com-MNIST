# 📚 Implementação da Arquitetura LeNet-5 com MNIST

Este projeto tem como objetivo implementar a arquitetura **LeNet-5**, um dos primeiros modelos de redes neurais convolucionais (CNNs), utilizando a base de dados **MNIST**. A atividade foi realizada como parte da disciplina de Deep Learning na pós-graduação.

## 🧠 Objetivo

Construir, treinar e avaliar uma rede convolucional LeNet-5 para classificar dígitos manuscritos da base MNIST, aplicando boas práticas de pré-processamento, visualização, separação de dados e avaliação de desempenho.

---

## 📦 Tecnologias e Bibliotecas Utilizadas

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Google Colab
---

## 📁 Estrutura do Projeto

1. **Carregamento dos Dados**
   - Utilização da base MNIST via TensorFlow.
   - Separação em dados de treino e teste.

2. **Visualização dos Dados**
   - Exibição dos primeiros exemplos com seus respectivos rótulos usando Matplotlib.

3. **Pré-processamento**
   - Separação dos dados em treino, validação e teste.
   - Redimensionamento (padding) das imagens de 28x28 para 32x32.
   - Normalização dos valores de pixel para o intervalo [0, 1].

4. **Definição da Arquitetura LeNet-5**
   - Camadas:
     - 3 Camadas de convolução
     - 2 Camadas de pooling
     - 2 Camadas densas (fully-connected)
   - Função de ativação: `ReLU`
   - Saída com `softmax` para classificação dos 10 dígitos (0 a 9).

5. **Compilação e Treinamento**
   - Função de perda: `sparse_categorical_crossentropy`
   - Otimizador: `Adam` (melhor resultado que SGD)
   - Épocas: 20
   - Batch size: 64

6. **Avaliação do Modelo**
   - Avaliação com conjunto de teste.
   - Accuracy final de aproximadamente **98%**.

7. **Predição**
   - Teste de predição com exemplos isolados para verificar o funcionamento do modelo.

8. **Salvar e Carregar o Modelo**
   - Salvamento com `.save('modelo_lenet5.keras')`
   - Carregamento com `load_model(...)`

9. **Análise do Histórico de Treinamento**
   - Gráficos de `loss` e `val_loss` ao longo das épocas.

---

## 📊 Resultados

| Métrica        | Valor           |
|----------------|-----------------|
| Loss Inicial   | ~2.30           |
| Accuracy Inicial | ~11%           |
| Loss Final     | ~0.06           |
| Accuracy Final | **~98%**        |

O modelo apresentou ótimo desempenho após ajustes no otimizador e número de épocas, mostrando capacidade de generalização e boa performance de classificação.

---

## 🔍 Conclusões

- O uso da arquitetura LeNet-5 ainda é eficiente em datasets simples como MNIST.
- A escolha do otimizador e a quantidade de épocas têm um impacto direto no desempenho.
- A normalização e o padding são etapas fundamentais para garantir compatibilidade com a arquitetura.

---
📌 Autor

Fábio A. Oliveira

Projeto desenvolvido para praticar os conhecimentos adquiridos na pós-graduação em Ciência de Dados, juntamente com estudos e pesquisas pessoais sobre o tema.

