
# Whatsapp Bot con Python

Impulsa tu negocio con un bot usando las apis oficiales de whatsapp.
pueden ver el video paso a paso en el siguiente enlace: https://youtu.be/puYWiZDJnL0

## Descarga el proyecto


```bash
git clone https://github.com/JPierr3/bigdateros-whatsappbot-python.git
```
    
## Funcionalidades

- Enviar mensaje de texto
- Enviar menus como botones o listas
- Enviar stickers
- Marcar los mensajes como "visto" (doble check azul)
- Reaccionar con emojis los mensajes del usuario
- Enviar documentos pdf



## Para probarlo localmente

1. Dirigete al directorio donde descargaste el proyecto

```bash
  cd bigdateros-whatsappbot-python
```

2. Instala las dependencias

```bash
  pip install -r requirements.txt
```

3. Corre el aplicativo

```bash
  python app.py
```


## Simular mensajes del usuario con postman

```javascript
Ingresar la URL
http://127.0.0.1:5000/webhook


en body, seleccionar "raw" y tipo "JSON", no olvidar agregar tu número
{
  "object": "whatsapp_business_account",
  "entry": [{
      "id": "WHATSAPP_BUSINESS_ACCOUNT_ID",
      "changes": [{
          "value": {
              "messaging_product": "whatsapp",
              "metadata": {
                  "display_phone_number": "PHONE_NUMBER",
                  "phone_number_id": "PHONE_NUMBER_ID"
              },
              "contacts": [{
                  "profile": {
                    "name": "NAME"
                  },
                  "wa_id": "PHONE_NUMBER"
                }],
              "messages": [{
                  "from": "agrega tu numero",
                  "id": "wamid.ID",
                  "timestamp": "TIMESTAMP",
                  "text": {
                    "body": "hola"
                  },
                  "type": "text"
                }]
          },
          "field": "messages"
        }]
  }]
}
```

