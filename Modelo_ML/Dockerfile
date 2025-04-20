FROM python:3.11-slim

# Copiamos solo lo necesario (la carpeta Modelo_ML)
COPY Modelo_ML /app

# Establece el directorio de trabajo directamente donde está app.py y los modelos
WORKDIR /app

# Mejores prácticas: actualiza pip y setuptools
RUN pip install --upgrade pip setuptools

# Instala las dependencias
RUN pip install -r requirements.txt

# Expone el puerto por defecto de Streamlit
EXPOSE 8080

# Comando para correr Streamlit desde dentro de /app
ENTRYPOINT ["streamlit", "run", "app.py", "--server.port=8080", "--server.address=0.0.0.0"]

