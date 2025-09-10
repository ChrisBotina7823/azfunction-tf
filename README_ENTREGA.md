## Integrantes
- Cristian Eduardo Botina Carpio A00395008
- Juan Manuel Marín Angarita A00382037

# Proceso

## 1. Configuración del plan y variables

- Inicialmente se ejecutó el comando `terraform init`, que crea la carpeta y obtiene lo necesario.

![terraform init](<img/Captura de pantalla 2025-09-10 080926.png>)

- Al intentar hacer el plan con `terraform plan`, con el proyecto base se tienen errores por el subscription ID. Esto se solucionó añadiendolo como variable y añadiendo a la definición del provider. Por otro lado, el nombre de la función solo podía tener letras y números, por lo que se tuvo que corregir esto también.

![error subscription](<img/Captura de pantalla 2025-09-10 080936.png>)

![error function name](<img/Captura de pantalla 2025-09-10 080947.png>)

## 2. Ejecución del plan

- Con la variable definida y el nombre corregido, se ejecuta el plan:

![terraform plan](<img/Captura de pantalla 2025-09-10 081012.png>)

![plan success](<img/Captura de pantalla 2025-09-10 081024.png>)

## 3. Apply

Finalmente, se ejecuta `terraform apply`:

![terraform apply](<img/Captura de pantalla 2025-09-10 081031.png>)

Se confirman los cambios

![apply confirmation](<img/Captura de pantalla 2025-09-10 081042.png>)

La url se tiene como output


![apply success message](<img/Captura de pantalla 2025-09-10 081232.png>)

## 4. Verificación

- El grupo de recursos sale en el az portal:

![az group resource](<img/Captura de pantalla 2025-09-10 081349.png>)

- Al acceder a la URL se puede observar que el código se ejecutó con éxito:

![http test](<img/Captura de pantalla 2025-09-10 081436.png>)