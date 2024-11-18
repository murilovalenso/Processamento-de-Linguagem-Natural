# Processamento-de-Linguagem-Natural
## NLP com Análise de Sentimentos


Análise de Sentimentos com Processamento de Linguagem Natural.

Este projeto é voltado para a análise de sentimentos em textos utilizando técnicas de Processamento de Linguagem Natural (PLN).

Este conjunto de dados contém sentenças rotuladas com sentimento positivo ou negativo, extraídas de resenhas de produtos, filmes e restaurantes dos seguintes sites abaixo.

● imdb.com

● amazon.com

● yelp.com

=======
Formato:
sentença \t pontuação \n

=======
Detalhes:
A pontuação é 1 (para positivo) ou 0 (para negativo)
As sentenças vêm de três sites/categorias diferentes:

Para cada site, existem 500 sentenças positivas e 500 negativas. Essas sentenças foram selecionadas aleatoriamente de conjuntos de dados maiores de resenhas.
Tentamos selecionar sentenças que têm uma conotação claramente positiva ou negativa, com o objetivo de que não houvesse sentenças neutras selecionadas.

Para acessar os conjuntos de dados completos, consulte:

● imdb: Maas et al., 2011 'Learning word vectors for sentiment analysis'

● amazon: McAuley et al., 2013 'Hidden factors and hidden topics: Understanding rating dimensions with review text'

● yelp: Desafio do conjunto de dados do Yelp http://www.yelp.com/dataset_challenge

O foco principal do projeto é a limpeza e pré-processamento de dados textuais, além da aplicação de diferentes abordagens de vetorização de texto para análise de sentimentos.


Sobre a funcionalidade do projeto será a realização de uma série de etapas de pré-processamento em textos, com o objetivo de preparar os dados para análise de sentimentos, podendo ser utilizados em modelos de machine learning ou deep learning.

## 1. Limpeza de Texto
O processo de limpeza de texto inclui as seguintes operações:

Remoção de caracteres Unicode: Remove caracteres especiais que não contribuem para a análise do texto (ex.: emojis, caracteres acentuados, símbolos estranhos).

Remoção de pontuações: Elimina sinais de pontuação (como ponto final, vírgulas, etc.) que podem interferir na análise de sentimentos.

Remoção de URLs e e-mails: Extrai links e endereços de e-mail presentes no texto, que não têm relevância para a análise de sentimentos.

Remoção de Stopwords: As stopwords são palavras de pouca relevância para a análise (como "o", "a", "de", "em"), que são removidas do texto para evitar que influenciem de forma negativa a análise de sentimentos.

## 2. Pré-processamento do Texto
Inclui várias etapas importantes:

Lowercasing: Converte todas as palavras para minúsculas, garantindo uniformidade e evitando que a mesma palavra em diferentes casos (ex.: "sentimento" e "Sentimento") seja tratada de forma diferente.

Tokenização: Separa o texto em unidades menores chamadas tokens (normalmente palavras ou frases curtas), permitindo uma análise mais detalhada do conteúdo.

Stemming: Reduz as palavras às suas raízes, removendo sufixos e prefixos. Por exemplo, a palavra "amando" seria reduzida a "am".

Lematização: Similar ao stemming, mas de forma mais sofisticada, a lematização transforma as palavras para sua forma base ou lema (por exemplo, "melhores" para "bom").

## 3. Vetorização de Texto

A vetorização de texto transforma os dados textuais em uma forma que pode ser compreendida pelos modelos de aprendizado de máquina. Duas abordagens principais são utilizadas neste projeto:

## 3.1. Bag of Words (BoW)
O modelo Bag of Words representa cada documento como um vetor de contagem de palavras. Ele cria um vocabulário a partir do conjunto de dados e conta quantas vezes cada palavra do vocabulário aparece no texto. Esse método é simples, mas eficiente, e permite representar textos de maneira compacta, apesar de não levar em consideração a ordem das palavras.

Exemplo: Texto: "Eu amo PLN"

Vocabulário: ["Eu", "amo", "PLN"]
Vetor: [1, 1, 1]
## 3.2. Word Embeddings
Os Word Embeddings são uma abordagem mais sofisticada de vetorização, onde cada palavra é representada como um vetor de números em um espaço vetorial contínuo. Técnicas como Word2Vec ou GloVe (Global Vectors for Word Representation) são utilizadas para criar esses embeddings. A principal vantagem dos word embeddings é que eles capturam relações semânticas entre palavras, permitindo que palavras com significados semelhantes estejam mais próximas no espaço vetorial.

Exemplo: As palavras "rei" e "rainha" terão embeddings próximos, devido à semelhança semântica entre elas.

## 4. Modelos de Análise de Sentimentos

Após o pré-processamento e vetorização do texto, o projeto pode ser expandido para análise de sentimentos utilizando modelos clássicos de machine learning, como Naive Bayes, Support Vector Machine (SVM), ou modelos mais avançados baseados em redes neurais como LSTM ou BERT.
