# Tablero de análisis y pronóstico de demanda energética – Austria

Tablero interactivo desarrollado con Dash y Plotly que permite visualizar la demanda
energética horaria de Austria y su pronóstico para un horizonte definido por el usuario.

## Funcionalidades

- Selección de la fecha y hora inicial de la serie (calendario y lista desplegable).
- Definición del número de horas a proyectar mediante un control deslizante.
- Visualización de la demanda observada y del pronóstico con sus límites superior e inferior.

## Datos

El archivo `datos_energia.csv` contiene la serie horaria de demanda energética de Austria
publicada en la plataforma de transparencia de ENTSO-E.

| Columna | Descripción |
|---|---|
| `time` | Fecha y hora de la observación |
| `AT_load_actual_entsoe_transparency` | Demanda real observada (MW) |
| `forecast` | Valor pronosticado |
| `Upper bound` / `Lower bound` | Límites superior e inferior del pronóstico |

## Estructura del repositorio

```
├── app.py              # Aplicación Dash (layout y callbacks)
├── assets/             # Hojas de estilo CSS del tablero
├── datos_energia.csv   # Datos de demanda y pronóstico
├── requirements.txt    # Dependencias con versiones fijadas
└── README.md
```

## Ejecución local

Requisito: Python 3 (probado con Python 3.14.6).

```bash
pip install -r requirements.txt
python app.py
```

Luego abrir en el navegador: http://127.0.0.1:8050

## Contexto académico

Taller 2 – Repositorios Git. Curso Despliegue de Soluciones Analíticas,
Maestría en Inteligencia Analítica de Datos (MIAD), Universidad de los Andes, 2026.
