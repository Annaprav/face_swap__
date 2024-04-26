

## Требования

- Python 3.x
- OpenCV (cv2)


## Установка

   ```
   pip install -r requirements.txt
   ```

## Использование

```
python main.py --src SOURCE_IMAGE --dst DESTINATION_IMAGE --out OUTPUT_IMAGE [--warp_2d] [--correct_color]
```
Пример:
```
python main.py --src imgs/tom.jpg --dst imgs/obama.jpg --out results/tom_2d_corr.jpg --warp_2d --correct_color
```

Аргументы:
- `--src`: Путь к исходному изображению (обязательный).
- `--dst`: Путь к целевому изображению (обязательный).
- `--out`: Путь для сохранения выходного изображения (обязательный).
- `--warp_2d`: Использовать 2D-преобразование вместо 3D (опционально). 
- `--correct_color`: Выполнить коррекцию цвета (опционально).

В results можно сравнить отличия решений с warp_2d, correct_color.
warp_2d`лучше не использовать, когда лицо на исходном ихображении повернуто. Однако, для людей с довольно разными чертами лица это решение будет лучше. (сравнить result/tom и  result/tom_2d)

## Структура проекта

- `main.py`: Основной файл приложения.
- `face_detection.py`: Модуль для обнаружения лиц на изображениях.
- `face_swap.py`: Модуль для замены лиц.


