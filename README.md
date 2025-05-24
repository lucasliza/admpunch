# Análise e Processamento de Dados de Melbourne Punch

Este projeto contém uma série de notebooks Jupyter para processamento e análise de imagens das edições de Melbourne Punch disponíveis no catálogo TROVE. 
Ele abrange toda a arquitetura, desde a coleta de dados até formas de análise, oferecendo um caminho possível a pesquisadores que trabalham com conjuntos de dados de imagens históricas.

## Índice
1. [Visão Geral](#visão-geral)
2. [Requisitos](#requisitos)
3. [Configuração](#configuração)
4. [Notebooks Jupyter](#notebooks)
5. [Executando os códigos](#executando-os-códigos)
6. [Licença](#licença)
7. [Solução de problemas](#solução-de-problemas)

## Visão Geral

O projeto tem como objetivo digitalizar, processar e analisar imagens históricas da revista ilustrada satírica Melbourne Punch. Buscamos demonstrar um fluxo de trabalho completo para trabalhar com coleções de imagens históricas em grande escala, incluindo a aquisição de dados, processamento de imagens, treinamento de modelos de aprendizado de máquina e recursos para construção de gráficos a partir dos dados coletados.

## Requisitos

- Python 3.11 ou posterior
- Conda (Miniconda ou Anaconda)
- Git (para clonar o repositório)

## Configuração

1. Clone o repositório:
   ```
   git clone https://github.com/lucasliza/admpunch.git
   cd admpunch
   ```

2. Crie um ambiente Conda:
   ```
   conda create -n projeto_mpunch python=3.11
   ```

3. Ative o ambiente Conda:
   ```
   conda activate projeto_mpunch
   ```

4. Instale os pacotes necessários usando o arquivo requisitos.txt:
   ```
   pip install -r requisitos.txt
   ```

## Notebooks

1. `1 - DownloadPDFs.ipynb`: 

2. `2 - PDFtoJPG.ipynb`:

3. `3 - ImageSampling.ipynb`:

5. `5 - ExtractImages.ipynb`:

## Executando os códigos

Siga as etapas a seguir para executar os notebooks deste projeto:

1. Assegure-se que você está no diretório do projeto:
   ```
   cd caminho/para/admpunch
   ```

2. Ative o ambiente Conda (se ainda não o tiver feito):
   ```
   conda activate projeto_mpunch
   ```

3. Inicie o Jupyter Notebook:
   ```
   jupyter notebook
   ```

## Licença

Este projeto está sob a licença Creative Commons Zero v1.0 Universal (CC0-1.0). Isso significa que você pode copiar, modificar, distribuir e executar o trabalho, mesmo para fins comerciais, sem pedir permissão. Para obter mais detalhes, consulte o arquivo [LICENSE](LICENSE) neste repositório.

## Solução de problemas

