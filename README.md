# Análise e Processamento de Dados de Melbourne Punch

Este projeto contém uma série de notebooks Jupyter para processamento e análise de imagens das edições de Melbourne Punch disponíveis no catálogo TROVE. 
Ele abrange toda a arquitetura, desde a coleta de dados até formas de análise, oferecendo um caminho possível a pesquisadores que trabalham com conjuntos de dados de imagens históricas.

## Índice
1. [Visão Geral](#visão-geral)
2. [Requisitos](#requisitos)
3. [Configuração](#configuração)
4. [Execução do código](#execução-do-código)
5. [Descrição dos notebooks](#descrição-dos-notebooks)
6. [Licença](#licença)
7. [Solução de problemas](#solução-de-problemas)

## Visão Geral

O projeto tem como objetivo digitalizar, processar e analisar imagens históricas da revista ilustrada satírica Melbourne Punch. Buscamos demonstrar um fluxo de trabalho completo para trabalhar com coleções de imagens históricas em grande escala, incluindo a aquisição de dados, processamento de imagens, treinamento de modelos de aprendizado de máquina e recursos para construção de gráficos a partir dos dados coletados.

## Requisitos

- Python 3.11 ou posterior
- [Conda](https://www.anaconda.com/download-success) (Miniconda ou Anaconda)
- Git (para clonar o repositório)

## Configuração

1. Clone o repositório:
   ```
   git clone https://github.com/lucasliza/admpunch.git
   cd admpunch
   ```

2. Crie um ambiente Conda:
   ```
   $ conda create --name projeto_mpunch --file requisitos.txt
   ```

3. Ative o ambiente Conda:
   ```
   conda activate projeto_mpunch
   ```

## Execução do código

Siga as etapas a seguir para executar os notebooks deste projeto:

1. Assegure-se que você está no diretório do projeto:
   ```
   cd caminho/para/admpunch
   ```

2. Ative o ambiente Conda (se ainda não o tiver feito):
   ```
   conda activate projeto_mpunch
   ```

3. Inicie o Jupyter Lab:
   ```
   jupyter lab
   ```

## Descrição dos notebooks

`1 - DownloadPDFs.ipynb`
   - Finalidade: 
      - Download de arquivos PDF contendo as páginas da revista Melbourne Punch dos registros de arquivo CSV obtido do TROVE.
   - Detalhamento das tarefas principais:
      - Lê URLs de download de um arquivo CSV.
      - Pula downloads de arquivos já existentes.
      - Implementa download paralelo para eficiência.
      - Inclui tratamento de erros para downloads e carregamento de dados.

`2 - PDFtoJPG.ipynb`
   - Finalidade:
      - Conversão de arquivos PDF em imagens JPG de alta resolução.
   - Detalhamento das tarefas principais:
      - Lê dados de um arquivo CSV, esperando caminhos para PDFs.
      - Usa a biblioteca `pdf2image` para realizar a conversão, permitindo ajuste de resolução (DPI).
      - Implementa processamento paralelo para converter múltiplos PDFs simultaneamente, aumentando a eficiência.
      - Inclui tratamento de erros para PDFs corrompidos ou não encontrados.
      - Gera um novo CSV com informações sobre os arquivos JPG criados e quaisquer erros.

`3 - ImageSampling.ipynb`:
   - Finalidade:
      - Gerar um conjunto amostral aleatório de imagens e as dividir em conjuntos de treinamento e validação.
   - Detalhamento das tarefas principais:
      - Implementa amostragem estratificada para garantir conjuntos de dados equilibrados.
      - Proporção de divisão de treinamento/validação personalizável.

`4 - FinetuneYolo.ipynb`
   - Finalidade:
      - Treinar e avaliar um modelo de detecção de objetos YOLO para detecção de charges na revista.
   - Detalhamento das tarefas principais:
      - Usa a implementação do Ultralytics YOLOv11 nano.
      - Inclui funcionalidades de treinamento, avaliação e exportação de modelos
      - Visualiza os resultados do treinamento e as métricas de desempenho do modelo

`5 - ExtractImages.ipynb`
   - Finalidade:
      - Detectar e extrair ilustrações de imagens de jornal, salvando as ilustrações detectadas como arquivos separados.
   - Detalhamento das tarefas principais:
      - Aplica o modelo YOLO treinado para detectar regiões de interesse
      - Extrai e salva as regiões detectadas como imagens separadas
      - Gera metadados para as imagens extraídas
   
`6 - GenerateHeatmap.ipynb`
   - Finalidade:
      - Gerar mapas de calor (heatmaps) para visualizar a distribuição e densidade de ilustrações em páginas de documentos.
   - Detalhamento das tarefas principais:
      - Filtra ilustrações por intervalo de datas e por página específica.
      - Exclui opcionalmente ilustrações que cobrem a página inteira para focar em conteúdo menor.
      - Gera heatmaps usando `Matplotlib`, representando a densidade de sobreposição com cores.
      - Salva os heatmaps gerados como arquivos de imagem para cada página processada.

## Licença

Este projeto está sob a licença Creative Commons Zero v1.0 Universal (CC0-1.0). Isso significa que você pode copiar, modificar, distribuir e executar o trabalho, mesmo para fins comerciais, sem pedir permissão. Para obter mais detalhes, consulte o arquivo [LICENSE](LICENSE) neste repositório.

## Solução de problemas

