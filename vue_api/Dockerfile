FROM python:3.10-slim

WORKDIR /app

# copiar apenas o arquivo de dependências e instalar primeiro
COPY requirements.txt /app/requirements.txt
RUN pip install --no-cache-dir -r /app/requirements.txt

# copiar o arquivo da aplicação explicitamente
COPY app.py /app/app.py

# se tiver outras pastas (ex: model/, static/) copie-as também,
# por exemplo: COPY model/ /app/model/
# COPY static/ /app/static/

EXPOSE 8000

CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8000"]
