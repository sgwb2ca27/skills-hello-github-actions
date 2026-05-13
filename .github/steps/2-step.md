## Paso 2: Añade un job a tu workflow

Buen trabajo! :tada: Has creado tu primer workflow!

### ⌨️ Actividad: Añade un job a tu workflow

1. De nuevo en la rama `welcome-workflow`, abre el archivo`.github/workflows/welcome.yml`.

1. Edita el archivo para añadir la sección `jobs`y un job llamado `welcome`, que ejecutará la ultima versión de Ubuntu.

   ```yaml
   name: Post welcome comment
   on:
     pull_request:
       types: [opened]
   permissions:
     pull-requests: write
   jobs:
     welcome:
       name: Post welcome comment
       runs-on: ubuntu-latest
   ```

1. Haz commit de tus cambios a la rama `welcome-workflow`.

1. Con la información del job añadida, Mona verificará tu trabajo y preparará el siguiente paso del workshop!

<details>
<summary>Tienes problemas? 🤷</summary><br/>

- Asegúrate de que la seccion `jobs` tiene bien la indentación.
- Verifica que has modificado la rama y archivos correctos.

</details>
