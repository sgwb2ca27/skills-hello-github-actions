## Paso 3: Agrega un step a tu archivo workflow

_¡Buen trabajo agregando un job a tu workflow! :dancer:_

### ⌨️ Actividad: Agrega un step a tu archivo workflow

1. En la rama `welcome-workflow`, abre tu archivo `.github/workflows/welcome.yml`.

1. Agrega un step al job `welcome` para publicar un comentario en nuevas pull requests usando GitHub CLI:

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
       steps:
         - run: gh pr comment "$PR_URL" --body "Welcome to the repository!"
           env:
             GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
             PR_URL: ${{ github.event.pull_request.html_url }}
   ```

1. Haz commit de tus cambios directamente a la rama `welcome-workflow`.

1. ¡Con la información del step agregada, Mona revisará tu trabajo y preparará el siguiente paso del ejercicio!

<details>
<summary>¿Tienes problemas? 🤷</summary><br/>

- Asegúrate de que la sección `steps` esté bajo el job `welcome` e indentada correctamente.
- Verifica que tengas las variables de entorno correctas configuradas.

</details>
