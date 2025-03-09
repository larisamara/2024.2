# Usar uma imagem base do Python
FROM python:3-slim

# Definir o diretório de trabalho no contêiner
WORKDIR /app

# Copiar o script Python para o contêiner
COPY main.py .
COPY main-v2.py .
COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

# Executar o script Python
CMD ["sh", "-c", "python main.py && python main-v2.py"]
