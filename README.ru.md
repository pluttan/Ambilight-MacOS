![Header](header.png)

<div align="center">

# Ambilight macOS

**Программная амбиентная подсветка для macOS через Arduino**

[![License](https://img.shields.io/badge/license-MIT-2C2C2C?style=for-the-badge&labelColor=1E1E1E)](LICENSE)
[![Python](https://img.shields.io/badge/python-2.7-2C2C2C?style=for-the-badge&logo=python&labelColor=1E1E1E)]()
[![Arduino](https://img.shields.io/badge/arduino-UNO-2C2C2C?style=for-the-badge&logo=arduino&labelColor=1E1E1E)]()

</div>

Python-скрипт, который захватывает цвета по краям экрана на macOS и управляет RGB-лентой 5050, подключённой к Arduino UNO. Настраиваемое количество светодиодов на сторону, плотность сэмплирования пикселей и поддержка Retina-дисплеев.

## ■ Возможности

- ❖ **Захват экрана в реальном времени** — сэмплирует крайние пиксели для управления амбиентными светодиодами
- ❖ **Настраиваемый макет** — задайте количество светодиодов на каждую сторону (top, right, bottom, left) и смещения
- ❖ **Поддержка Retina** — множитель плотности пикселей для HiDPI-дисплеев
- ❖ **Автоопределение** — автоматически находит серийный порт Arduino (`/dev/cu.usbserial*`)

## ■ Стек

<div align="center">

| Компонент | Технология |
|-----------|------------|
| Программная часть | Python 2.7 |
| Захват экрана | PyObjC (Quartz CoreGraphics, AppKit) |
| Аппаратная часть | Arduino UNO, RGB 5050 LED strip |
| Связь | Serial 115200 baud (pySerial) |

</div>

## ■ Запуск

```bash
# Edit config.py with your LED layout
python ambilight.py
```

Требует прошивки [Arduino firmware](https://github.com/sergeich5/Ambilight-Arduino-part) на Arduino UNO.

## ■ License

MIT © [pluttan](https://github.com/pluttan)
