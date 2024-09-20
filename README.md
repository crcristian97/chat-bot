# Python Chat App 💬

Una sencilla aplicación de chat en tiempo real construida con **Flask**, **Socket.IO** y **JavaScript**. Los usuarios se conectan de manera anónima y pueden enviar mensajes, cambiar su nombre de usuario, y ver a otros usuarios unirse y salir del chat en tiempo real. Cada usuario recibe un avatar generado aleatoriamente.

## Características 🚀

- **Mensajería en tiempo real**: Los mensajes se transmiten instantáneamente a todos los usuarios conectados.
- **Identificación anónima**: Los usuarios obtienen un nombre de usuario único y un avatar generado automáticamente al conectarse.
- **Actualización de nombre de usuario**: Los usuarios pueden cambiar su nombre de usuario en cualquier momento.
- **Conexión y desconexión**: Los usuarios son notificados cuando alguien se une o abandona el chat.

## Tecnologías utilizadas 🛠️

- **Backend**: Flask y Flask-SocketIO para manejar la lógica de la aplicación y las conexiones WebSocket.
- **Frontend**: HTML, CSS y JavaScript para la interfaz de usuario y la interacción en tiempo real.
- **Socket.IO**: Comunicación bidireccional en tiempo real entre el servidor y el cliente.
- **Avatares**: Los avatares de usuario se generan aleatoriamente utilizando una API.

## Instalación 📝

Sigue los siguientes pasos para clonar y ejecutar esta aplicación en tu máquina local:

1. Clona este repositorio:
    ```bash
    git clone https://github.com/tu-usuario/python-chat-app.git
    cd python-chat-app
    ```

2. Crea un entorno virtual (opcional pero recomendado):
    ```bash
    python3 -m venv venv
    source venv/bin/activate   # En Windows: venv\Scripts\activate
    ```

3. Instala las dependencias necesarias:
    ```bash
    pip install -r requirements.txt
    ```

4. Ejecuta la aplicación:
    ```bash
    flask run
    ```

5. Abre tu navegador en `http://127.0.0.1:5000` y comienza a chatear.

## Archivos principales 📂

- `app.py`: El archivo principal que contiene el servidor Flask y los eventos de Socket.IO.
- `app.js`: Lógica del cliente para la interacción con Socket.IO y la actualización de la interfaz del chat.
- `index.html`: Página principal donde los usuarios interactúan con el chat.
- `style.css`: Estilos CSS para la interfaz del chat.

## Eventos de Socket.IO 🔄

- `connect`: Cuando un usuario se conecta, se le asigna un nombre de usuario y un avatar automáticamente.
- `disconnect`: Al desconectar, se notifica a los demás usuarios que el usuario ha abandonado el chat.
- `send_message`: Cuando un usuario envía un mensaje, este se transmite a todos los demás usuarios conectados.
- `update_username`: Permite a los usuarios actualizar su nombre de usuario en tiempo real.
- `new_message`: Los mensajes nuevos se muestran a todos los usuarios junto con el avatar y el nombre de usuario.

## Estructura del proyecto 📁

```bash
.
├── app.py                   # Archivo principal de la aplicación Flask
├── static/
│   ├── css/
│   │   └── style.css         # Estilos del chat
│   └── js/
│       └── app.js            # Lógica del cliente con Socket.IO
├── templates/
│   └── index.html            # Plantilla HTML para la interfaz del chat
└── requirements.txt          # Dependencias del proyecto
