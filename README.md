
# Advanced Robotics | Домашние работы

**Кудинов Руслан**

---

## 📌 Обзор

В рамках курса выполнены 4 домашние работы, охватывающие ключевые задачи робототехники:

| № | Название | Методы | Папка |
|---|----------|--------|-------|
| **1** | Обнаружение стен и плоскости пола | Split and Merge, RANSAC | [HW1](./HW1) |
| **2** | Оценка пройденного пути | Linear Kalman Filter | [HW2](./HW2) |
| **3** | Оценка ориентации | EKF (Эйлер vs Кватернионы) | [HW3](./HW3) |
| **5** | Планирование пути | A*, RRT, RRT* | [HW5](./HW5) |

---

## 📊 Краткие результаты

### HW1: Обнаружение стен и плоскости пола
- **Split and Merge:** 1138 точек → 11 ключевых (сжатие 99%)
- **RANSAC:** 8,793 инлайнера из 11,367 (77.4%)

### HW2: Оценка пройденного пути
- **Итоговая дистанция:** 107.11 м (GPS) → 107.08 м (KF)
- **Ошибка:** 0.04 м

### HW3: Оценка ориентации
- **Gimbal Lock:** достигнут при Pitch = 81.3°
- **Euler EKF:** разваливается (углы уходят в 10¹¹)
- **Quaternion EKF:** продолжает корректно работать

### HW5: Планирование пути
- **A*:** 0.466 с, 470.11 px
- **RRT:** 1.234 с, 542.67 px
- **RRT*:** 1.567 с, 498.23 px

---

## 📁 Структура

```
advanced_robotics/
├── README.md           # Этот файл
├── HW1/                # Обнаружение стен и пола
│   ├── README.md
│   ├── wall_detection.ipynb
│   └── results/
├── HW2/                # Фильтр Калмана
│   ├── README.md
│   ├── kalman_filter.ipynb
│   └── results/
├── HW3/                # EKF ориентации
│   ├── README.md
│   ├── attitude_ekf.ipynb
│   └── results/
└── HW5/                # Планирование пути
    ├── README.md
    ├── path_planning.ipynb
    └── path_planning_results/
```

---

## 🚀 Запуск

Каждая работа запускается отдельно:

```bash
cd HW1 && jupyter notebook wall_detection.ipynb
cd HW2 && jupyter notebook kalman_filter.ipynb
cd HW3 && jupyter notebook attitude_ekf.ipynb
cd HW5 && jupyter notebook path_planning.ipynb
```

---

## 👨‍💻 Автор

**Кудинов Руслан**  
*Advanced Robotics Course*

---

*Последнее обновление: Март 2026*
```
