# Transfer Learning com YOLO usando COCO Dataset

Este projeto demonstra como realizar transfer learning usando YOLOv3-tiny com o dataset COCO no Google Colab.

## Pré-requisitos
- Conta Google (para usar o Colab)
- GPU habilitada no Colab (Editar → Configurações do notebook → Acelerador de hardware)

## Passos para execução

### 1. **Abrir o Notebook no Colab**
   - Faça upload do arquivo `yolo_coco_transfer_learning.ipynb` para o Google Colab
   - Ou clone este repositório diretamente no Colab:
   ```bash
   !git clone https://github.com/seu-usuario/repositorio.git
```
### 2. **Executar a configuração inicial**

O script irá:
    Clonar e compilar o Darknet;
    Baixar o dataset COCO (2017);
    Converter as anotações para o formato YOLO;

### 3. **Modificar a configuração do YOLO**

O código ajusta automaticamente:
Batch size e subdivisions
Número de classes (80 para COCO)
Paths dos dados

### 4. **Iniciar o treinamento**
O treinamento usará transfer learning com pesos pré-treinados
Monitorar a loss durante o treinamento
Os pesos finais serão salvos em backup/

### 5. **Avaliação e Teste**

O script inclui:
Cálculo de mAP
Exemplo de inferência com imagem de teste

## Estrutura de Arquivos
├── darknet/              # Repositório YOLO/darknet
├── train2017/            # Imagens de treino
├── annotations/          # Anotações COCO
├── coco.data             # Configuração dos dados 
├── cfg/                  # Arquivos de configuração da rede 
└── backup/              # Pesos treinados 

## **Personalização**
Para usar com outras versões do YOLO:
    Altere o arquivo de configuração em cfg/
    Baixe os pesos correspondentes
Para outros datasets:
    Ajuste o script de conversão de anotações
    Modifique o número de classes e paths

## **Recursos**
COCO Dataset
YOLO Official Site
Darknet GitHub

## **Notas Importantes**
O treinamento completo pode levar várias horas
Google Colab tem limite de tempo para execuções (use runtime intermitente)
Salve periodicamente os pesos treinados no Google Drive
