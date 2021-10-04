## Ejercicio de Sistemas de Control de Versiones

Para realizar esta práctica se utilizara la metodología gitflow la cual consiste en:

Se crearán varios tipos de ramas:
  - La master en la cual estará el proyecto actualizado en la última version.
  - La develop en la cual se testeará el proyecto y es donde se hara un merge para hacer un push a la rama master.
  - Ramas de funcionalidad en la que se aplicara una nueva funcionalidad al proyecto.
  - Ramas de hotfixes en las cuales se harán pequeñas modificaciones del proyecto.
  
Ventajas:
  - El sistema de trabajo permite trabajar muy bien en grupo.
  - Permite tener las versiones de nuestro proyecto bien controladas

Desventajas:
  - Ralentiza la produccción.
  - Un gran número de creaciones de ramas.
  
Para empezar crearemos el repositorio de git en github y lo clonaremos en nuestros tres supuestos usuarios:

![1](https://user-images.githubusercontent.com/76181286/135796663-59577c3a-ca1a-4b9b-bdae-c8ec251832f5.png)

### Usuario 1

El usuario 1 creara la estructura inicial del proyecto con la página de home.

![2](https://user-images.githubusercontent.com/76181286/135796672-0a78e037-c189-4b17-adc5-ffb482022ac4.png)

Después realizará un commit y lo subirá al repositorio remoto

### Usuario 2

Realizará un pull para recibir la estructura inicial del proyecto.

Y creará tanto las páginas de modifyhtml en su propia rama:
![7](https://user-images.githubusercontent.com/76181286/135796688-c577e26e-ee8b-4637-b73b-127e2082cc22.png)
![8](https://user-images.githubusercontent.com/76181286/135796693-53fb2da5-d936-4233-9d52-b13e3d368d22.png)

Como la de modifyattributes:
![13](https://user-images.githubusercontent.com/76181286/135796823-fba98a7d-b474-46ec-a449-d986b1eabe58.png)
![9](https://user-images.githubusercontent.com/76181286/135796698-a7d9d657-fbfd-48b6-921f-8af3f29b261d.png)

### Usuario 3

Creará la pagina de modifycss:
![11](https://user-images.githubusercontent.com/76181286/135796712-d1400d92-aa0d-48f4-a06d-4fd9a53258c1.png)
![10](https://user-images.githubusercontent.com/76181286/135796704-3ce34909-0ebe-45b2-b796-48133e1ff9ea.png)

### Usuario 1

El usuario 1 creará una rama develop donde se realizará el merge del proyecto para comprobar que funciona perfectamente antes de subirlo a github
![14](https://user-images.githubusercontent.com/76181286/135796835-f8186caf-041d-4627-86d5-5f3b0014dade.png)
![15](https://user-images.githubusercontent.com/76181286/135796752-3103f4bc-12a0-4efa-b3ec-3dcab0de8f67.png)
![16](https://user-images.githubusercontent.com/76181286/135796764-70b6ceea-55ae-4c70-aae9-2ca225f66a75.png)
![17](https://user-images.githubusercontent.com/76181286/135796767-f4b4eac6-0db8-40c7-874b-6bf43d9e0020.png)

Después de comprobar que funciona perfectamente irá a la rama master i realizara el merge:
![18](https://user-images.githubusercontent.com/76181286/135796859-13996587-cfc8-467e-b7c0-482707f258d8.png)
![19](https://user-images.githubusercontent.com/76181286/135796864-30de1018-acaa-4fc2-a391-c873b98fdd24.png)

Cuando esto finalize crearemos una rama test y haremos un tag para la versión de master:
![27](https://user-images.githubusercontent.com/76181286/135797410-ebf884dc-567e-48f8-834a-918ebf4f7cf0.png)
![26](https://user-images.githubusercontent.com/76181286/135797403-8ba5e97c-acd4-4a1e-853a-2f8c0c579762.png)

### Hooks

Post-checkout: instala la carpeta nodemodules cada vez que se realiza un checkout
![20](https://user-images.githubusercontent.com/76181286/135797335-e2bcb126-8fff-4c05-ae6b-096ac0ecaa34.png)

Commit-msg: verifica el mensaje del commit
![21](https://user-images.githubusercontent.com/76181286/135797360-3d824bbd-ce98-494a-8b19-742d64dc4bb8.png)

Pre-push: Comprueba que ningún fichero contenga carácteres extraños antes de realizar un push
![29](https://user-images.githubusercontent.com/76181286/135799087-f5ec9754-62f6-4669-9185-911ee183af8e.png)

Pre-commit: Utiliza eslint para comprobar el correcto formato de los html de la aplicación
![24](https://user-images.githubusercontent.com/76181286/135797387-d1b88b56-420d-44da-8fd0-3105cd0c8656.png)

