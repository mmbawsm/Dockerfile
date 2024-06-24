# Dockerfile

# Utiliza una imagen base con Python 3.10
FROM python:3.10-slim

# Establece el directorio de trabajo en el contenedor
WORKDIR /app

# Copia el script de Python en el directorio de trabajo
COPY lanzamiento_de_dados.py .

# Instala las dependencias necesarias
RUN pip install dice

# Ejecuta el script de Python
CMD ["python", "lanzamiento_de_dados.py"]
