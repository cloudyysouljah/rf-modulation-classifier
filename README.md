# RF Modulation Classifier 
### 🇷🇺RU
<div align="left">
  
Данный репозиторий содержит мой дипломный проект — программу для автоматического распознавания видов модуляции радиосигналов по IQ-отсчётам.

Приложение написано на Python, основные фреймворки - PyQt, pyqtgraph, для обучения модели использовался PyTorch, для инференса используется ONNX Runtime.

В качестве обучающего набора данных используется RadioML 2018 в формате HDF5.

Программа поддерживает работу как с заранее подготовленными IQ-данными, так и с данными, получаемыми с Red Pitaya.
</div>

## Установка
### Шаг 1. Для установки сначала копируем проект: 
```
git clone https://github.com/cloudyysouljah/rf-modulation-classifier.git
cd rf-modulation-classifier
```
### Шаг 2. Установка окружения:
```
sudo apt install python3-venv
python3 -m venv venv
source venv/bin/activate
```
### Шаг 3. Установка зависимостей:

## Для запуска приложения:
```
pip install -r requirements_inference.txt 
```
## Для запуска приложения и возможности обучения:
```
pip install -r requirements_train.txt 
```
### Шаг 4. Запуск:
```
python3 main.py
```

## Пример работы программы
<p align="center">
<img width="1920" height="1080" alt="Снимок экрана от 2026-05-18 14-12-18" src="https://github.com/user-attachments/assets/505817b8-8cb4-48b5-a77b-542a40782ae8"/>
</p>
<div align="center">

  Основное окно программы

</div>

<p align="center">
<img width="854" height="633" alt="Снимок экрана от 2026-05-26 14-01-11" src="https://github.com/user-attachments/assets/f1c3e67b-ef4d-4a09-ae28-0ba7fd8b9a44" align="center"/>
</p>
<div align="center">
  
  Окно обучения модели

</div>

## Результаты обучения модели

| Параметр           |        Значение |
| ------------------ | --------------: |
| Accuracy           |            67 % |
| Количество классов |              24 |
| Размер входа       | 1024 IQ samples |
| Формат модели      |            ONNX |
| Inference provider |             CPU |

## Матрица ошибок
<img width="1093" height="993" alt="Снимок экрана от 2026-05-19 15-17-47" src="https://github.com/user-attachments/assets/56cd3ac9-5670-49af-b5c8-b024f0d3c572" />

## Скорость обработки модели

| Параметр           | Обработка модели, мс|
| ------------------ | -------------------:|
| CPU                |         10-15       |
| CUDA               |         20-30       |

## Используемые технологии
- Python
- PyQt6
- pyqtgraph
- PyTorch
- ONNX Runtime
- NumPy
- HDF5
- Red Pitaya / SCPI

### 🇬🇧ENG

<div align="left">
  
This repository contains my thesis project: a program for the automatic recognition of radio signal modulation types based on IQ samples.

The application is written in Python, utilizing PyQt and pyqtgraph as the primary frameworks; PyTorch was used for model training, while ONNX Runtime is used for inference.

The RadioML 2018 dataset in HDF5 format serves as the training data.

The program supports operation with both pre-prepared IQ data and data acquired from a Red Pitaya device.
</div>

## Install
### Step 1. For install copy project: 
```
git clone https://github.com/cloudyysouljah/rf-modulation-classifier.git
cd rf-modulation-classifier
```
### Step 2. Install environment:
```
sudo apt install python3-venv
python3 -m venv venv
source venv/bin/activate
```
### Step 3. Install requirements:

## For launching program:
```
pip install -r requirements_inference.txt 
```
## For launching program and training model:
```
pip install -r requirements_train.txt 
```
### Step 4. Launch program:
```
python3 main.py
```

## 
<p align="center">
<img width="1920" height="1080" alt="Снимок экрана от 2026-05-18 14-12-18" src="https://github.com/user-attachments/assets/505817b8-8cb4-48b5-a77b-542a40782ae8"/>
</p>
<div align="center">

  Main window

</div>

<p align="center">
<img width="854" height="633" alt="Снимок экрана от 2026-05-26 14-01-11" src="https://github.com/user-attachments/assets/f1c3e67b-ef4d-4a09-ae28-0ba7fd8b9a44" align="center"/>
</p>
<div align="center">
  
  Training window

</div>

## Resuts of training model

| Parameter          |        Значение |
| ------------------ | --------------: |
| Accuracy           |            67 % |
| Number of classes  |              24 |
| Input size         | 1024 IQ samples |
| Model format       |            ONNX |
| Inference provider |             CPU |

## Confusion matrix
<img width="1093" height="993" alt="Снимок экрана от 2026-05-19 15-17-47" src="https://github.com/user-attachments/assets/56cd3ac9-5670-49af-b5c8-b024f0d3c572" />

## Model processing speed

| Parameter          | Model processing, ms|
| ------------------ | -------------------:|
| CPU                |         10-15       |
| CUDA               |         20-30       |

## Used technologies
- Python
- PyQt6
- pyqtgraph
- PyTorch
- ONNX Runtime
- NumPy
- HDF5
- Red Pitaya / SCPI
