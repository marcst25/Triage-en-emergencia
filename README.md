# Clasificación de Nivel de Gravedad en Triage de Emergencias

**Universidad del Valle de Guatemala · Análisis de Datos · Sección 10**  
Daniela Dianne López Polanco · Marcela Isabel Castañeda Paredes · Abby Isabella Barrios Reyes  
`lop23710@uvg.edu.gt` · `cas23717@uvg.edu.gt` · `bar23137@uvg.edu.gt`

---

## Descripción del proyecto

Este proyecto desarrolla un modelo predictivo de clasificación para estimar el nivel de gravedad de un paciente durante el triage en servicios de emergencia hospitalaria. La variable objetivo es **triage_level** (escala de 4 niveles, equivalente a ESI), estimada a partir de variables clínicas registradas en el ingreso del paciente.

El objetivo es construir un sistema de apoyo a la decisión clínica (CDSS) que reduzca la variabilidad en el proceso de triage y mejore la priorización de atención en emergencias.

---

## Dataset 
https://www.kaggle.com/datasets/emirhanakku/synthetic-medical-triage-priority-dataset/data


| Campo           | Detalle |
|-----------------|---------|
| **Nombre**      | Synthetic Medical Triage Dataset |
| **Archivo**     | `synthetic_medical_triage.csv` |
| **Fuente**      | Kaggle (datos sintéticos generados para investigación) |
| **Licencia**    | Público — uso académico |
| **Filas**       | 18,000 pacientes |
| **Columnas**    | 10 variables (9 predictoras + 1 objetivo) |
| **Tipo de uso** | Datos secundarios sintéticos (Real World Data simulado) |
| **Datos faltantes** | 0% — dataset completo sin valores nulos |

---

## Estructura del repositorio

```
proyecto/
├── data/
│   └── raw/
│       └── synthetic_medical_triage.csv
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_limpieza.ipynb
│   ├── 03_features.ipynb
│   └── 04_modelo.ipynb
├── outputs/
│   └── figures/
│       └── eda_triage.png
├── requirements.txt
└── README.md
```

---

## Variable objetivo

| Variable | Descripción | Tipo | Valores |
|----------|-------------|------|---------|
| `triage_level` | Nivel de gravedad asignado en triage | Ordinal | 0 = No urgente (55.1%) · 1 = Menos urgente (24.9%) · 2 = Urgente (15.0%) · 3 = Emergente (5.0%) |

---

## Variables predictoras

| Variable | Descripción | Tipo |
|----------|-------------|------|
| `age` | Edad del paciente (años) | Numérica continua |
| `heart_rate` | Frecuencia cardíaca (lpm) | Numérica continua | 
| `systolic_blood_pressure` | Presión arterial sistólica (mmHg) | Numérica continua | 
| `oxygen_saturation` | Saturación de oxígeno (%) | Numérica continua |
| `body_temperature` | Temperatura corporal (°C) | Numérica continua | 
| `pain_level` | Nivel de dolor reportado (1–10) | Ordinal | 
| `chronic_disease_count` | Número de enfermedades crónicas | Numérica discreta |
| `previous_er_visits` | Visitas previas a emergencias | Numérica discreta | 
| `arrival_mode` | Modo de llegada | Categórica | walk_in (66%) · wheelchair (17%) · ambulance (17%) |

---
```

---

## Referencias

- Raita, Y. et al. (2019). Emergency department triage prediction of clinical outcomes using machine learning models. *Annals of Emergency Medicine*, 73(4), 357–369.
- Chang, Y. H. et al. (2022). Machine learning-based triage to identify low-severity patients. *BMC Emergency Medicine*, 22(1), 88.
- Sutton, R. T. et al. (2020). An overview of clinical decision support systems. *NPJ Digital Medicine*, 3, 17.
- FDA. (2024). Real-World Evidence. U.S. Food and Drug Administration.
