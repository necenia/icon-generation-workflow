# Шаблоны промптов

Подставь видимые признаки из выбранного референса. Если движок принимает изображение, приложи его отдельно через инструмент. Для сравнения стилей сохрани предметы в тех же ячейках.

## Сетка

```text
Create one square 3×3 contact sheet of nine icons for [interface].
Use [material and finish], [camera angle], [studio lighting] and a
continuous [background]. Use [base color] as the dominant color and
[accent hex] on one clearly visible feature per object.

Row 1, left to right: [R1C1], [R1C2], [R1C3].
Row 2, left to right: [R2C1], [R2C2], [R2C3].
Row 3, left to right: [R3C1], [R3C2], [R3C3].

Center one complete object per cell. Match visual weight and keep
even gutters. Omit captions, logos and grid lines.
```

## Клоуз-ап

```text
Render one [object] selected from row [n], column [m] of the approved sheet.
Match [silhouette], [proportions], [recognizable detail], [material],
[accent location and color], [camera angle] and [lighting].
Center the complete object in a square canvas. Its longest dimension
fills about 85% of the frame. Keep all extremities visible.
Omit other objects, the grid and captions. Output a high-resolution
PNG with alpha if supported, or use a uniform light-gray background.
```

При текстовом вводе замени ссылку на ячейку подробным описанием её содержимого. При наличии кропа можно заменить первое предложение на `Re-render only the object in the supplied crop.`

## Как сменить стиль

1. **Скруглённые плитки.** Массивные скругления, серые плитки, мягкие сатиновые блики.
2. **Парящие предметы.** Диагональный наклон, слабая тень под объектом, глянцевые фаски.
3. **Матовые миниатюры.** Тёплая поверхность, контактная тень, мелкая металлическая фурнитура.

Для графической изометрии задай общие оси и плоские заливки. Для предметной съёмки укажи плетение ткани, строчку или металл. Для мелкой навигации задай фронтальные пиктограммы из двух–трёх крупных форм и проверку при 24–32 px.
