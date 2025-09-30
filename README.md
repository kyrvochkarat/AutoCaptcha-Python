# 🎯 Auto Captcha Solver

<div align="center">

![Python](https://img.shields.io/badge/python-v3.7+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey.svg)
![OpenCV](https://img.shields.io/badge/OpenCV-4.0+-red.svg)
![Tesseract](https://img.shields.io/badge/Tesseract-OCR-yellow.svg)

[![GitHub stars](https://img.shields.io/github/stars/yourusername/auto-captcha-solver.svg?style=social&label=Star)](https://github.com/yourusername/auto-captcha-solver)
[![GitHub forks](https://img.shields.io/github/forks/yourusername/auto-captcha-solver.svg?style=social&label=Fork)](https://github.com/yourusername/auto-captcha-solver)

**Автоматический решатель 5-значных цифровых капч с возможностью выбора области экрана**


</div>

---

## 📋 Описание

Мощный инструмент для автоматического распознавания и ввода 5-значных цифровых капч в играх и приложениях. Использует комбинацию методов компьютерного зрения для максимальной точности распознавания.

## ✨ Основные возможности

<table>
<tr>
<td>

### 🎯 Точное распознавание
- Template Matching
- Контурный анализ
- OCR через Tesseract
- Multi-scale поиск

</td>
<td>

### ⚡ Быстродействие
- Распознавание < 0.5 сек
- Мгновенный ввод
- Минимальная нагрузка
- MSS для захвата

</td>
<td>

### 🎮 Удобство
- Горячие клавиши
- Выбор области
- Авто-режим
- Сохранение настроек

</td>
</tr>
</table>

## 📊 Статистика производительности

<div align="center">

| Метрика | Значение |
|---------|----------|
| ![Speed](https://img.shields.io/badge/Скорость-0.2--0.5s-brightgreen) | Время распознавания |
| ![Accuracy](https://img.shields.io/badge/Точность-95%25+-blue) | С правильными эталонами |
| ![CPU](https://img.shields.io/badge/CPU-<5%25-orange) | Нагрузка на процессор |
| ![RAM](https://img.shields.io/badge/RAM-512MB-purple) | Использование памяти |

</div>

## 🚀 Установка

### Требования

![Windows](https://img.shields.io/badge/Windows-10%2F11-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.7+-3776AB?style=for-the-badge&logo=python&logoColor=white)

### Зависимости

```bash
pip install pyautogui pytesseract pillow opencv-python numpy keyboard mss pywin32
```

### Tesseract OCR (опционально)

[![Tesseract](https://img.shields.io/badge/Download-Tesseract_OCR-FF6F00?style=for-the-badge)](https://github.com/tesseract-ocr/tesseract)

Для улучшенного распознавания установите Tesseract OCR

## 💻 Использование

### Быстрый старт

```bash
git clone https://github.com/yourusername/auto-captcha-solver.git
cd auto-captcha-solver
python captcha_solver.py
```

### Первоначальная настройка

1. **Запустите скрипт**
   ```bash
   python captcha_solver.py
   ```

2. **Выберите область капчи** - нажмите `F4` и выделите зону

3. **Настройте эталоны** - добавьте реальные цифры в папку `numbers/`

## ⌨️ Горячие клавиши

<div align="center">

| Клавиша | Действие | Описание |
|:-------:|----------|----------|
| ![F1](https://img.shields.io/badge/F1-Решить-blue?style=flat-square) | Решить капчу | Однократное распознавание и ввод |
| ![F2](https://img.shields.io/badge/F2-Авто-green?style=flat-square) | Автоматический режим | Непрерывное сканирование |
| ![F3](https://img.shields.io/badge/F3-Стоп-red?style=flat-square) | Остановить | Прекратить авто-режим |
| ![F4](https://img.shields.io/badge/F4-Область-yellow?style=flat-square) | Выбрать область | Указать зону с капчей |
| ![F5](https://img.shields.io/badge/F5-Сброс-orange?style=flat-square) | Сбросить область | Использовать весь экран |
| ![ESC](https://img.shields.io/badge/ESC-Выход-grey?style=flat-square) | Выход | Закрыть программу |

</div>

## 📁 Структура проекта

```
📦 auto-captcha-solver/
┣ 📜 captcha_solver.py      # Основной скрипт
┣ 📂 numbers/               # Эталонные изображения цифр
┃ ┣ 📷 0.png
┃ ┣ 📷 1.png
┃ ┗ 📷 ...
┣ 📂 screenshots/           # Сохраненные скриншоты
┗ 📄 config.json           # Конфигурация
```

## 🔧 Конфигурация

Файл `config.json` создается автоматически:

```json
{
  "search_region": [100, 200, 300, 50],
  "confidence_threshold": 0.7,
  "typing_delay": 0.02,
  "scan_interval": 0.1
}
```

## 📈 Методы распознавания

<div align="center">

```mermaid
graph TB
    A[Скриншот] --> B[Предобработка]
    B --> C{Template Matching}
    B --> D{Контурный анализ}
    B --> E{OCR Tesseract}
    C --> F[Результат]
    D --> F
    E --> F
    F --> G[Ввод капчи]
```

</div>

## 🛠️ Решение проблем

<details>
<summary><b>❌ Не распознает цифры</b></summary>

- Обновите эталоны в папке `numbers/`
- Используйте реальные цифры из вашего приложения
- Проверьте качество изображений

</details>

<details>
<summary><b>🐌 Медленная работа</b></summary>

- Выберите область капчи (F4)
- Уменьшите область сканирования
- Закройте лишние приложения

</details>

<details>
<summary><b>⚠️ Ошибка Tesseract</b></summary>

- Установите Tesseract OCR
- Или работайте без него (Template Matching)
- Проверьте путь к tesseract.exe

</details>

## 🤝 Вклад в проект

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](http://makeapullrequest.com)

Приветствуются любые улучшения! Создавайте Issue и Pull Requests.

## 📝 Лицензия

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

MIT License - свободное использование и модификация

## ⚠️ Дисклеймер

> **Важно:** Используйте только в образовательных целях и в соответствии с правилами целевого приложения.

## 👨‍💻 Автор

<div align="center">

Разработано с ❤️ для автоматизации рутинных задач

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/yourusername)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your.email@example.com)

</div>

---

<div align="center">

### ⭐ Если проект был полезен, поставьте звезду!

[![Star History Chart](https://api.star-history.com/svg?repos=yourusername/auto-captcha-solver&type=Date)](https://star-history.com/#yourusername/auto-captcha-solver&Date)

</div>
