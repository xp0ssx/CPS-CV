# CPS-CV

## Инструкция для запуска

### Скачивание датасета

Скачивание и распаковка датасета в папке репозитория:

```bash
mkdir -p dataset
curl -L "https://www.kaggle.com/api/v1/datasets/download/pkdarabi/cardetection" -o dataset/cardetection.zip
unzip -q -o dataset/cardetection.zip -d dataset
rm -f dataset/cardetection.zip
```

### Настройка окружения

Выполните следующие команды для создания и настройки окружения и запуска Jupyter Notebook

```bash

# 1) Создание виртуального окружения
python3 -m venv .venv

# 2) Активация виртуального окружения
source .venv/bin/activate

# 3) Установка инструментов для запуска Jupyter
pip install --upgrade pip
pip install notebook

# 4) Регистрация текущего виртуального окружения как ядра Jupyter
python -m ipykernel install --user --name cv --display-name "Kernel for CV"

# 4) Запусr Jupyter
jupyter notebook CV_road_signs.ipynb
```

После запуска откройте ноутбук и выберите интерпретатор `Kernel for CV`, если он не выбрался автоматически.
