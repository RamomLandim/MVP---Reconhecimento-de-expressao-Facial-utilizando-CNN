# MVP - Reconhecimento de expressão facial utilizando CNN
Este projeto é um MVP (Produto Mínimo Viável) para o reconhecimento de expressões faciais utilizando Redes Neurais Convolucionais (CNNs). Ele é baseado em um modelo de aprendizado profundo treinado para identificar e classificar emoções em imagens de rostos, utilizando o Face Expression Recognition Dataset do Kaggle.

🎯 Objetivo
O objetivo deste projeto é criar um modelo simples e eficiente que seja capaz de identificar as principais expressões faciais (como felicidade, tristeza, surpresa, etc.) a partir de imagens, fornecendo uma base inicial para sistemas de reconhecimento de emoção.

🚀 Tecnologias Utilizadas

**Python**: Linguagem principal do projeto.

**os**: Manipulação de diretórios e arquivos do sistema.

**OpenCV (cv2)**: Biblioteca para processamento de imagens, utilizada para pré-processamento e manipulação das imagens faciais.

**NumPy**: Biblioteca para cálculos numéricos e manipulação de arrays, essencial para o trabalho com dados de imagem.

**TensorFlow/Keras**: Framework de aprendizado de máquina para construção, treinamento e avaliação do modelo CNN.

**Scikit-Learn**: Utilizado para divisão dos dados de treino e teste e para codificação de rótulos.

**Keras ImageDataGenerator**: Geração de dados aumentados para evitar overfitting e melhorar a robustez do modelo.

**Keras Layers**:

    Sequential: Estrutura sequencial para empilhar camadas da rede neural.
    
    Conv2D, MaxPooling2D, Flatten, Dense, Dropout, BatchNormalization: Camadas fundamentais para construir uma CNN robusta.

**Keras Optimizers (Adam, RMSprop, SGD)**: Otimizadores populares para ajustes dos pesos durante o treinamento.

**Matplotlib**: Biblioteca para visualização dos dados, criação de gráficos de precisão, perda, e análise do desempenho do modelo.

**Keras Callbacks**:

    ModelCheckpoint: Salva o modelo durante o treinamento quando a performance melhora.
    
    EarlyStopping: Interrompe o treinamento se o modelo parar de melhorar, evitando overfitting.
    ReduceLROnPlateau: Reduz a taxa de aprendizado quando a performance do modelo atinge um plateau.

