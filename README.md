# MVP - Reconhecimento de expressão facial utilizando CNN
Este projeto é um MVP (Produto Mínimo Viável) para o reconhecimento de expressões faciais utilizando Redes Neurais Convolucionais (CNNs). Ele é baseado em um modelo de aprendizado profundo treinado para identificar e classificar emoções em imagens de rostos, utilizando o Face Expression Recognition Dataset do Kaggle.

## 🎯 Objetivo
O objetivo deste projeto é criar um modelo simples e eficiente que seja capaz de identificar as principais expressões faciais (como felicidade, tristeza, surpresa, etc.) a partir de imagens, fornecendo uma base inicial para sistemas de reconhecimento de emoção.

## 🚀 Tecnologias Utilizadas
No desenvolvimento de um modelo de reconhecimento de expressões faciais utilizando CNNs, várias bibliotecas desempenham papéis essenciais, desde a manipulação de imagens até a construção, treinamento e avaliação do modelo. A seguir, descrevemos a funcionalidade de cada biblioteca e como elas são utilizadas neste projeto:

- **os:** Essa biblioteca é usada para operações relacionadas ao sistema operacional, como navegação em diretórios, manipulação de arquivos e verificação da estrutura de pastas. É essencial para carregar e organizar o conjunto de dados de imagens.
- **cv2 (OpenCV):** Biblioteca amplamente utilizada para processamento de imagens e visão computacional. Aqui, ela é empregada para leitura, manipulação e pré-processamento de imagens, como redimensionamento, conversão para escala de cinza e detecção de faces.
- **numpy:** Biblioteca fundamental para cálculos matemáticos e manipulação de arrays. É utilizada para representar imagens como arrays numéricos, realizar operações vetorizadas e facilitar a manipulação de dados durante o pré-processamento.
- **tensorflow:** Um dos principais frameworks para desenvolvimento de modelos de aprendizado de máquina e deep learning. Ele fornece as ferramentas necessárias para criar e treinar redes neurais convolucionais (CNNs), base do modelo de reconhecimento de expressões faciais.
- **sklearn.model_selection.train_test_split:** Função do scikit-learn que divide o conjunto de dados em subconjuntos de treinamento e teste, garantindo uma separação adequada para validação do modelo.
- **sklearn.preprocessing.LabelEncoder:** Essa classe transforma rótulos de classe (emoções) em valores numéricos, facilitando sua manipulação e uso em modelos de aprendizado de máquina.
- **tensorflow.keras.utils.to_categorical:** Converte os rótulos numéricos das emoções em vetores one-hot, que são necessários para o treinamento supervisionado em problemas de classificação.
- **tensorflow.keras.models.Sequential e tensorflow.keras.models.Model:** Estruturas para construção de modelos em Keras. O Sequential é usado para criar modelos com uma sequência linear de camadas, enquanto o Model permite criar arquiteturas mais complexas com várias entradas e saídas.
- **Camadas do tensorflow.keras.layers:**
 - **Dense:** Camada totalmente conectada para combinar os recursos extraídos pela CNN.
 - **Dropout:** Regularizador que ajuda a reduzir o overfitting desligando aleatoriamente algumas conexões durante o treinamento.
 - **BatchNormalization:** Normaliza as ativações de cada camada, acelerando o treinamento e melhorando a estabilidade.
 - **Flatten:** Transforma matrizes multidimensionais em vetores, facilitando a entrada em camadas densas.
 - **GlobalAveragePooling2D:** Reduz a dimensionalidade das características extraídas pela CNN, permitindo uma representação compacta.
 - **Conv2D e MaxPooling2D:** Camadas de convolução e pooling para extração de características visuais relevantes.
 - **Activation:** Aplica funções de ativação, como **ReLU** ou **softmax**, para introduzir não-linearidade no modelo.
 - **tensorflow.keras.optimizers.Adam:** Otimizador avançado que combina os benefícios de métodos como RMSprop e Momentum, permitindo um treinamento eficiente e com ajuste automático da taxa de aprendizado.
- **tensorflow.keras.preprocessing.image.ImageDataGenerator:** Realiza data augmentation, aumentando a diversidade do conjunto de treinamento por meio de transformações nas imagens, como rotações, deslocamentos e inversões. Isso melhora a robustez do modelo.
- **matplotlib.pyplot:** Ferramenta para visualização de dados. É usada para criar gráficos que mostram o desempenho do modelo durante o treinamento e a avaliação, como curvas de perda e acurácia.

Essas bibliotecas, combinadas, formam a base necessária para lidar com todas as etapas do desenvolvimento do modelo, desde o pré-processamento de dados até a avaliação final.

## Como Executar
Para executar este projeto, siga os passos abaixo:
- Clone este repositório para a sua máquina local.
    - Caso seja o google colab, pode-se utilizar:
    ~~~
    !git clone https://github.com/RamomLandim/MVP---Reconhecimento-de-expressao-Facial-utilizando-CNN.git
    %cd MVP---Reconhecimento-de-expressao-Facial-utilizando-CNN
    ~~~

- Crie um ambiente virtual Python e ative-o:
    ~~~
    python -m venv venv
    venv\Scripts\activate
    ~~~

- Instale as dependências do projeto:
    ~~~
    pip install -r requirements.txt
    ~~~

- Caso queira exportar os modelos, pode-se utilizar esse código:
    ~~~
    from tensorflow.keras.models import load_model
    model = load_model('Modelos/modelv4.h5')
    ~~~
