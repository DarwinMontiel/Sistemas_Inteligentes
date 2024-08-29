pruebas
Lenguaje largo usando olama

<h1> #1. Instalacion </h1>
El primer paso es descargamos [ollama] (https://ollama.com/download/linux) de su pagina web, y ejecutamos el siguiente comando

````bash
curl -fsSL https://ollama.com/install.sh | sh
````
<h1>#2. Correor el servidor</h1>

para iniciar corremos el comando 

````bash
ollama serve
````

<h1>#3. Impot module IA</h1>
buscamos el modelo a descargar en https://ollama.com/library

luego lanzamos el comado, Abrir otra ventana de comando 

````bash
ollama pull tinyllama
````
ollama list me muestra los modelos importados

````bash
ollama list
````
para hacer una pregunta 

````bash
ollama run tinyllama (se coloca la pregunta aqui)
````
comandos aqui = https://github.com/ollama/ollama/blob/main/docs/api.md

-X = metodo que quiero usar

````bash
curl http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?"
}'
````


````bash
curl http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?"
}' -o salida.md
````
````bash
curl http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?",
  "stream": false
}'
````