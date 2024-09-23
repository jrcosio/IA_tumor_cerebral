# Proyecto de Visión Artificial para Detección de Tumores Cerebrales

Este proyecto implementa un modelo de **Red Neuronal Convolucional (CNN)** para la detección de tumores cerebrales utilizando técnicas de **Deep Learning**. El objetivo principal es ayudar en la identificación temprana de tumores, proporcionando una herramienta de diagnóstico rápido para los profesionales médicos.

### Dataset de Kaggle
- https://www.kaggle.com/datasets/saisandeepdabbada/brain-mri-scan-dataset/data

## Descripción del Modelo

La arquitectura de la red está compuesta por:

- **Capas Convolucionales**:
  - 1ª capa: 64 filtros
  - 2ª capa: 128 filtros
  - 3ª capa: 128 filtros
  - 4ª capa: 256 filtros
- **Capas Densas** (fully connected):
  - 1ª capa: 128 neuronas
  - 2ª capa: 64 neuronas
- **Capa de salida**: 
  - Activación Sigmoid (para la clasificación binaria: presencia o ausencia de tumor)
  
### Funciones y Técnicas Utilizadas
- **Función de activación**: ReLU para todas las capas intermedias.
- **Función de pérdida**: Binary Crossentropy.
- **Optimizador**: Adam.

## Entrenamiento del Modelo

El modelo ha sido entrenado en una **GPU RTX 4070**, lo que ha permitido un procesamiento más rápido de los datos y una optimización eficiente del modelo.

- **Callbacks**: Se utilizaron controles como **EarlyStopping** y **ReduceLROnPlateau** para prevenir el sobreajuste (overfitting) y ajustar dinámicamente la tasa de aprendizaje.
- **Épocas**: 101
- **Precisión alcanzada**: 96.5% de **Accuracy** en los datos de prueba.

## Requisitos

Para ejecutar el proyecto localmente, necesitarás las siguientes dependencias:

```bash
pip install tensorflow keras numpy matplotlib Pillow scypy
```

## Ejecución

El notebook con todos los detalles del preprocesamiento de datos, la creación y el entrenamiento del modelo se encuentra disponible en este repositorio. Puedes descargarlo y ejecutarlo en tu entorno local o en Google Colab.

```bash
# Clonar el repositorio
git clone https://github.com/jrcosio/IA_tumor_cerebral.git

# Navegar al directorio del proyecto
cd IA_tumor_cerebral
```

## Contribuciones

¡Las contribuciones son bienvenidas! Si encuentras algún problema o tienes una sugerencia, no dudes en abrir un **issue** o enviar un **pull request**.

## License

Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

## GitHub

Puedes encontrar el notebook completo de Python en este repositorio. No olvides darle a la estrellita ⭐ si te resulta útil.
