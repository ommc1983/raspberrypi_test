¡Claro\! La forma más común de instalar **n8n** en una Raspberry Pi (que usa Linux) es utilizando **npm** (Node Package Manager).

Aquí tienes los comandos de instalación paso a paso:

-----

## 1\. Actualizar el Sistema

Es importante que tu Raspberry Pi esté completamente actualizada antes de comenzar.

```bash
sudo apt update && sudo apt upgrade -y
```

-----

## 2\. Instalar Node.js y npm

n8n está construido sobre Node.js, por lo que debes instalarlo junto con npm (el gestor de paquetes de Node). Se recomienda una versión LTS (Long-Term Support).

1.  **Descargar e instalar el repositorio de Node.js (por ejemplo, la versión 18.x):**

    ```bash
    curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -
    ```

2.  **Instalar Node.js:**

    ```bash
    sudo apt install -y nodejs
    ```

3.  **Verificar las versiones instaladas:**

    ```bash
    node -v
    npm -v
    ```

    (Deberías ver las versiones de Node y npm).

-----

## 3\. Instalar n8n Globalmente

Usa npm para instalar n8n de forma global en tu Raspberry Pi.

```bash
sudo npm install -g n8n
```

-----

## 4\. Iniciar y Acceder a n8n

Una vez instalado, puedes iniciarlo para hacer una prueba.

1.  **Iniciar n8n:**

    ```bash
    n8n start
    ```

    *Nota: Esto iniciará n8n en primer plano. Para un uso a largo plazo, se recomienda configurarlo como un servicio del sistema (ver sección 5).*

2.  **Acceder a la interfaz web:**

    Por defecto, n8n se ejecuta en el puerto `5678`. Abre un navegador web en otro dispositivo de tu red y navega a:

    ```
    http://<Tu_Dirección_IP_de_Raspberry_Pi>:5678
    ```

    *Reemplaza `<Tu_Dirección_IP_de_Raspberry_Pi>` con la IP real de tu dispositivo.*

-----

## 5\. (Opcional, pero recomendado) Configurar n8n como un Servicio del Sistema con PM2

Para que n8n se ejecute en segundo plano de forma fiable y se inicie automáticamente cuando se reinicia la Pi, puedes usar un gestor de procesos como **PM2**.

1.  **Instalar PM2 globalmente:**

    ```bash
    sudo npm install -g pm2
    ```

2.  **Iniciar n8n con PM2:**

    ```bash
    pm2 start n8n
    ```

3.  **Hacer que PM2 inicie n8n al arrancar el sistema:**

    ```bash
    pm2 save
    pm2 startup
    ```

    *El comando `pm2 startup` te dará un comando que deberás ejecutar (probablemente con `sudo`) para configurar el inicio automático.*

4.  **Comandos útiles de PM2:**

      * Ver el estado de n8n: `pm2 status`
      * Ver los logs: `pm2 logs n8n`
      * Detener n8n: `pm2 stop n8n`
      * Reiniciar n8n: `pm2 restart n8n`

Con esto, tendrás **n8n** funcionando de forma continua en tu Raspberry Pi. ¡A automatizar\! 🚀