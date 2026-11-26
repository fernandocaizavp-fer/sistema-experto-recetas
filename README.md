# Sistema experto de recomendación de platos

Sistema experto basado en reglas que **recomienda un plato** según los ingredientes que tienes y tus preferencias (vegano, sin gluten o plato rápido). Tiene una interfaz web hecha con **Gradio**.

## 🧠 Cómo funciona

El sistema tiene las tres partes clásicas de un sistema experto:

1. **Base de hechos:** lo que marca el usuario (por ejemplo `tiene_verduras = si`, `prefiere_vegano = si`).
2. **Base de conocimiento:** 10 reglas del tipo *SI … ENTONCES …*, por ejemplo:
   - SI tiene pasta Y tiene verduras → *Pasta con verduras salteadas*
   - SI tiene verduras Y prefiere vegano → *Salteado vegano de verduras*
   - SI tiene carne Y prefiere vegano → *Sugerencia: probar tofu*
3. **Motor de inferencia con encadenamiento hacia adelante:** recorre las reglas, aplica las que se cumplen y agrega sus conclusiones como hechos nuevos, hasta que ya no se puede deducir nada más.

## 🛠️ Tecnologías

Python · Gradio

## 🚀 Ejecutar

```bash
pip install -r requirements.txt
python recomendacion_platos.py
```

Se abre en el navegador, normalmente en `http://127.0.0.1:7860`. Marca tus ingredientes y preferencias y pulsa **Buscar Receta**.

## 👤 Autor

**Fernando Caiza** — Estudiante de Ingeniería en Software, ESPOCH
GitHub: [@fernandocaizavp-fer](https://github.com/fernandocaizavp-fer)
