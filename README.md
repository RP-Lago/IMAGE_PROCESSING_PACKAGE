# IMAGE_PROCESSING_PACKAGE



## Descrição



O **Image Processing Package** é um pacote Python desenvolvido como parte de um exercício prático proposto pela [Digital Innovation One](https://digitalinnovation.one/) (DIO) em colaboração com a NTT DATA, sob a mentoria de [Karina Kato](https://www.linkedin.com/in/karina-kato-4b2a56182/).



O principal objetivo deste projeto é proporcionar uma experiência prática na criação, empacotamento e publicação de um pacote Python, com foco em **processamento de imagens**. O pacote oferece funcionalidades básicas para a manipulação de imagens, sendo projetado para ser facilmente instalável, reutilizável e extensível.



## Funcionalidades



Atualmente, o pacote oferece as seguintes funcionalidades:



### Processamento



- **Histogram Matching:** Realiza a correspondência de histograma entre duas imagens, útil para correção de cores e melhoria do contraste.

- **Structural Similarity:** Calcula o Índice de Similaridade Estrutural (SSIM) entre duas imagens, fornecendo uma medida de similaridade perceptual.

- **Resize Image:** Redimensiona imagens para uma proporção especificada, preservando a qualidade.



### Utilitários



- **Input/Output de Imagem:** Funções para carregar imagens de arquivos e salvar imagens processadas.

- **Plotagem:** Utilitários para exibir imagens e seus respectivos histogramas, facilitando a análise visual.

- **Comparação:** Funcionalidades para comparar imagens e destacar diferenças, úteis para avaliação de resultados.




## Como Utilizar



Aqui estão alguns exemplos de uso do pacote:



```python

from image_processing.processing import combination, transformation

from image_processing.utils import io, plot



# Carregar imagens

image1 = io.read_image("imagem1.jpg")

image2 = io.read_image("imagem2.jpg")



# Redimensionar imagem

resized_image = transformation.resize_image(image1, proportion=0.5)



# Corresponder Histograma

matched_image = combination.transfer_histogram(image1, image2)



# Encontrar Diferenças entre Imagens

difference_image = combination.find_difference(image1, image2)



# Exibir Resultados

plot.plot_image(image1)

plot.plot_result(image1, image2, matched_image)

plot.plot_histogram(image1)

```



## Dependências



O pacote depende das seguintes bibliotecas:



- `matplotlib`

- `numpy`

- `scikit-image >= 0.16.1`



As dependências serão instaladas automaticamente ao instalar o pacote via `pip`.



## Estrutura do Projeto



```plaintext

image-processing-package/

├── image_processing/

│   ├── processing/

│   │   ├── __init__.py

│   │   ├── combination.py

│   │   └── transformation.py

│   └── utils/

│       ├── __init__.py

│       ├── io.py

│       └── plot.py

├── setup.py

├── requirements.txt

└── README.md

```



## Testes

## Instalação



### PyPI



Para instalar a versão estável do pacote diretamente do [PyPI](https://pypi.org/), utilize o comando:



```bash

pip install image-processing-dio

```



### TestPyPI



Para instalar a versão de desenvolvimento (menos estável) do pacote diretamente do [TestPyPI](https://test.pypi.org/), utilize o comando:



```bash

pip install --index-url https://test.pypi.org/simple/ image-processing

```




O pacote inclui testes unitários para garantir a funcionalidade do código. Os testes podem ser executados usando a biblioteca `pytest`:



```bash

pytest

```



## Contribuições



Contribuições são bem-vindas! Sinta-se à vontade para abrir uma _issue_ para relatar problemas, sugerir melhorias ou enviar um _pull request_ com suas contribuições.



## Licença



Este projeto está licenciado sob a licença MIT - consulte o arquivo [LICENSE](LICENSE) para obter detalhes.



## Agradecimentos



- Digital Innovation One (DIO)

- NTT DATA Europe & Latam DATA

- Karina Kato
