# Hands-On: asistente de pedidos con Llama 3.1

## Descripción

Este notebook implementa un asistente de pedidos en Python. Utiliza
Llama 3.1 mediante Ollama para generar respuestas y FastAPI para
recibir mensajes mediante un webhook.

## Objetivo

Practicar la recepción y el procesamiento de mensajes, incorporar
una bienvenida para usuarios nuevos y generar respuestas breves
con un tono amable y profesional.

## Herramientas utilizadas

- Python.
- Google Colab.
- Ollama y el modelo Llama 3.1 8B.
- FastAPI.
- Uvicorn.
- Requests.

## Funcionamiento

1. Se instala y se inicia Ollama.
2. Se descarga el modelo Llama 3.1 8B.
3. Se configura un servidor FastAPI.
4. Se verifica el webhook mediante una petición GET.
5. Se envían mensajes simulados mediante peticiones POST.
6. El primer mensaje de cada usuario recibe una bienvenida.
7. Los siguientes mensajes reciben una respuesta generada por Llama.
8. Las respuestas se muestran en Colab y se registran en memoria.

## Instrucciones de ejecución

1. Abrir el notebook en Google Colab.
2. Seleccionar un entorno con GPU, si está disponible.
3. Ejecutar las celdas del challenge en orden.
4. Esperar a que termine la descarga del modelo.
5. Ejecutar la primera prueba para comprobar la bienvenida.
6. Ejecutar la segunda prueba para consultar el pedido DEMO-001.

Si se reinicia la sesión de Colab, es necesario volver a ejecutar
las celdas. No deben iniciarse dos servidores simultáneamente
en el mismo puerto.

## Control del tono

El prompt solicita respuestas en español, amables y profesionales,
con una extensión máxima de 2 o 3 líneas. También indica al modelo
que no invente información ni afirme haber modificado pedidos.

## Alcance y limitaciones

- No se utilizan credenciales de Meta ni un túnel de ngrok.
- La prueba local no verifica una integración real con WhatsApp.
- El asistente no crea, modifica ni cancela pedidos.
- Los registros se almacenan en memoria y se pierden al reiniciar.
- Cada consulta al modelo se procesa sin historial de conversación.
- El tiempo de respuesta depende de los recursos disponibles en Colab.
