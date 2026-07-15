FROM python:3.9-slim

WORKDIR /app

# Instalar Flask
RUN pip install flask

# Criar um app simples
RUN echo 'from flask import Flask\n\
app = Flask(__name__)\n\
\n\
@app.route("/")\n\
def hello():\n\
    return "Hello World from Cloud Run!\\n"\n\
\n\
if __name__ == "__main__":\n\
    app.run(host="0.0.0.0", port=8080)' > app.py

# Expor a porta que o Cloud Run espera
EXPOSE 8080

# Comando para iniciar o servidor
CMD ["python", "app.py"]