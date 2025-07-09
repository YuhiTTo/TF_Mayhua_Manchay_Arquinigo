# TF-Machine-Learning
## 🔍 Predicción de Criptomonedas Emergentes con Machine Learning
Este proyecto aplica técnicas de Machine Learning para identificar criptomonedas emergentes con alto potencial de valorización en el corto plazo (30 días). El objetivo es brindar soporte a decisiones de inversión mediante un sistema predictivo basado en datos históricos, características cuantitativas y narrativas temáticas del ecosistema cripto.

## 📊 Descripción del problema
Una firma de inversión peruana busca diversificar su portafolio incorporando criptomonedas más allá de Bitcoin y Ethereum, priorizando tokens emergentes con temáticas de actualidad como:

Inteligencia Artificial (IA)

Videojuegos (Gaming)

Activos del mundo real (RWA)

Memecoins (Memes)

La meta es anticipar qué activos tienen probabilidad de valorización ≥15 % en los siguientes 30 días.

## 🧠 Algoritmos utilizados
Se entrenaron y evaluaron dos modelos de clasificación supervisada:

- 🌲 Random Forest Classifier

- 🧮 Support Vector Machine (SVM)

El modelo final fue seleccionado con base en métricas como accuracy, F1-score y AUC-ROC.

## 📈 Datos
Los datos fueron extraídos mediante la API pública de CryptoCompare e incluyen:

Precios diarios (open, high, low, close)

Volumen de transacciones

Variables derivadas: retorno porcentual diario, media móvil de 7 días, volatilidad

Clasificación temática manual (narrativa)

Total: más de 6,400 registros históricos entre 2023 y 2025.

## 🎯 Variable objetivo
La variable target se definió como:

1 → si el token se valorizó ≥15 % en los 30 días siguientes

0 → en caso contrario

Esta formulación convierte el problema en una tarea de clasificación binaria.

## 📌 Resultados
Modelo	Accuracy	F1-Score	AUC-ROC
Random Forest	70.9 %	0.6861	0.7990
SVM (RBF)	58.1 %	0.4455	0.6000

Random Forest fue el modelo seleccionado por su mayor desempeño general y mejor capacidad discriminativa.

## 📂 Estructura del repositorio
- css
- Copiar
- Editar
- 📁 data/                → Datasets limpios y procesados
- 📁 notebooks/           → Jupyter Notebooks con EDA y modelado
- 📁 src/                 → Scripts de preprocesamiento y entrenamiento
- 📄 README.md            → Descripción general del proyecto

##🚀 Requisitos
Python 3.11

Pandas, NumPy

scikit-learn

matplotlib, seaborn

Instalar dependencias:

bash
Copiar
Editar
pip install -r requirements.txt

## 🧪 Cómo ejecutar
Clona el repositorio:

bash
Copiar
Editar
git clone https://github.com/YuhiTTo/TF_Mayhua_Manchay_Arquinigo.git
Ejecuta los notebooks en orden para preprocesar los datos y entrenar los modelos.
