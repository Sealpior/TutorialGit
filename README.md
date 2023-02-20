# TutorialGit

LO PRIMERO QUE DEBEMOS SABER Y TENER PRESENTE ESQUE HAY UNAS CONFIGURACIONES QUE SOLO SE HACEN UNA SOLA VEZ PARA CONFIGURAR EL GIT EN TU PC SI LO FORMATEAS O SE BORRA EL GIT TR¿ENDRAS QUE HACER ESTOS PASOS NUEVAMENTE ((HAY QUE TENER ESTO MUYYYYY CLARO, PODRIAS OCACIONAR FALLAS EN EL GIT SI  HACES UN COMANDO QUE NO SE DEBE REPETIR))

* SE RECOMIENDA TENER UNA CUENTA LISTA PARA SUBIR REPOSITORIOS EN  GITHUB
* ESTAS AYUDAS O GUIAS QUE TE DOY SON EXPECIALES PARA WINDOWS  AUNQUE PUEDE QUE TE FUNCIONEN CON OTRO SISTEMA OPERATIVO

1-  Lo primero que realizaremos despues de tener descargado git con su configuracion correcta  es abrir la consola de git y empezaremos a codificar  informacion importante como correo nombre de usuario y verificar la rama main 
![image](https://user-images.githubusercontent.com/125293481/220126872-3ebd853d-df3f-4f17-9bfe-8966789b8175.png)

2- Unas vez abierta la consola modificaremos  nombre de usuario y correo importante poner la informacion TAL CUAL esta creada en GITHUB con mayusculas minusculas TODO

*git config --global user.email “SuCorreo@correo.com” 
*git config --global user.name “SuUsuarioDeGitHub”
![image](https://user-images.githubusercontent.com/125293481/220130211-d20ad840-6d97-4048-85c7-88b6c6d8e5b5.png)

3- Para verificar que la informacion sea correcta  ponemos el siguiente  codigo 

*git config --list 
![image](https://user-images.githubusercontent.com/125293481/220130920-6e219c97-13e7-4f80-830c-5fa937ff9465.png)

4- Si por equivocacion pusiste los comandos mal hay que poner un codigo o comando para solucionar ese problema de lo contrario no te va a servir OJO esto es solo si lo pusiste mal 

*git config --global --unset-all user.nemail
 unas vez puesto este codigo vuelves hacer los pasos anteriores OJO solo el codigo que te quedo mal 
 
5- el siguiente comando no sayuda a verificar o dejar codificada la rama principal que es MAIN dado a que la rama MASTER ya no se usa por problemas de inlusion y demas :D

*git config --global init.defaultBranch main

6- Recuerda que todos los cambios se pueden ir revisando con 

*git config --list 

7- Lo siguente que haremos es conectar el GITHUB con GIT LOCAL como hacemos eso ? tenemos que generar una llave, la cual va a estar encrptada. ((SSH)) (Secure Shell) esta llave se genera con el sugiente codigo  

*ssh-keygen

Nos va pedir unas confirmaciones para las cuales damos ENTER tres veces, la primera es la ruta donde necesita crear una carpeta ssh para guardar las key, la segunda es generar una frase de seguridad la cual si escribimos algo es posible que luego se nos olvide y no podamos acceder a las key, por ende las dejaremos vacias, la tercera opcion es confirmación de esa clave que generamos para acceder a las key, como en este caso no generamos entonces damos enter también sin escribir nada.

En conclusión, después de escribir el comando ssh-keygen y presionar enter, nos pedirá las opciones mencionadas anteriormente y solo tenemos que dar ENTER tres veces.

![image](https://user-images.githubusercontent.com/125293481/220133368-6e6242af-89bd-41b8-a79e-b6248e8d37d1.png)

8- para desencriptar nuestra llave y poderla vincular en GITHUB podremos el siguiente comando 

*cat ~/.ssh/id_rsa.pub
![image](https://user-images.githubusercontent.com/125293481/220133734-815c1afb-4ccc-49fc-95c8-83f66be6cbfa.png)

9- Luego de generarla la copiamos sin espacios vacíos, ya que vamos a tener que pegarla en GITHUB.
![image](https://user-images.githubusercontent.com/125293481/220133918-09e8a82b-3126-4704-975c-7b00403b51a2.png)

10- Ahora vamos a pegar la clave en GITHUB pero primero tenemos que ir a nuestro usuario/perfil y damos click a settings o ajustes.
![image](https://user-images.githubusercontent.com/125293481/220134500-d140283b-47cc-40f7-a967-f58ad9194d1a.png)

11- Seleccionamos la opción SSH and GPG Keys.
![image](https://user-images.githubusercontent.com/125293481/220134783-1e04a027-342d-48b1-98dc-7df089e2b763.png)

12- Damos click en New SSH Key o Nueva clave SSH.
![image](https://user-images.githubusercontent.com/125293481/220135057-021aad03-04d7-447a-ae37-760e07f09043.png)

13-Creamos un nombre (Title) para la clave, puede ser cualquier nombre que identifique el equipo que vamos a utilizar, y pegamos la clave que generamos por consola.
![image](https://user-images.githubusercontent.com/125293481/220135366-3af56729-d67a-45a3-be3d-a73cccf45dc0.png)
![image](https://user-images.githubusercontent.com/125293481/220135588-6debddca-a85c-44f1-b136-7b2f3d73636c.png)

Para finalizar damos click en el botón Add SSH Key. (Puede que a veces nos pida confirmar la contraseña de GitHub)

Nos devuelve a la pantalla de configuración y nos muestra nuestra key creada, también podemos crear las Key que queramos.
![image](https://user-images.githubusercontent.com/125293481/220135836-e7ab2ba1-332f-44e0-bb0a-da3f62d09a57.png)


UNA VEZ ECHO ESTO ESTAMOS LISTOS PARA SUBIR NUESTRO PRIMER REPOSITORIO PERO COMO HACER ESO ? AQUI LO VEREMOS 

1- El primer paso sera abrir la consola de comando y inicializar el siguiente comando Se pondra el comando y abajo su explicacion.

*git init 
+El comando git init crea un nuevo repositorio de Git. Puede utilizarse para convertir un proyecto existente y sin versión en un repositorio de Git, o para inicializar un nuevo repositorio vacío

2- Basicamente este codigo lo que nos inica es que ya vamos a subir un repositorio y como saber cuales pues lo vas hacer mediante la url del repositorio

*git remote add origin "URL repo"
+El comando git remote te permite crear, ver y eliminar conexiones con otros repositorios. Las conexiones remotas se asemejan más a marcadores que a enlaces directos con otros repositorios. En lugar de brindar acceso en tiempo real a otro repositorio, funcionan como nombres prácticos que pueden emplearse para hacer referencia a una URL no tan sencilla.
![image](https://user-images.githubusercontent.com/125293481/220138700-b792e07e-d5c3-4038-a4d8-99d7ba527c29.png)
![image](https://user-images.githubusercontent.com/125293481/220139149-9b6acdf6-d789-4110-95b2-6b57e43d8acc.png)

3- Basicamente lo que hace el siguiente comando es mostrarnos en que estado esta nuestro nuevo repositorio 

*git status
![image](https://user-images.githubusercontent.com/125293481/220139733-d65fabe0-8786-4b74-84d1-00f3ef81ed27.png)

4- El siguiente codigo siempre si o si que vayamos a subir un repositorio hay que ponerlo no es necesario pero nos mostrara si hay alguna actualizacion echa por ti o por tus colegas de estudio o trabajo 

*git fetch origin main
![image](https://user-images.githubusercontent.com/125293481/220140318-81e2d86d-a1f3-4146-8e8c-1da8bacf0f2f.png)
![image](https://user-images.githubusercontent.com/125293481/220140644-18ecfdd0-3550-4c3d-8df3-d6c1b536c92b.png)
![image](https://user-images.githubusercontent.com/125293481/220140725-aa1e325d-e318-4cf9-9893-df241a585e16.png)

5- Este comando es el siguiente recuerden que todos los comandos van en el orden puesto y OJO es importante saber que estos pasos no son necesarios siempre mas adelante te dejare una guia donde podras ver los unicos codigos que vas a necesitar para ACTUALIZR un repositorio

*git pull origin main

6- Basicamente este comando lo que hace es decirle a git que nuestros archivos estan listos y que haga las actualizaciones necesesarias 

*git add .
![image](https://user-images.githubusercontent.com/125293481/220142021-74b120a1-104c-49dc-98f8-4be26863a332.png)

7- El siguiente no tiene explicacion hay que ver que tan pendiente estas y tu mismo sabras para que sera este comando 

*git status

8- Este comando basicamente es para "indicar que ya esta listo y darle un mensaje por el cual vas a poder identificar mas adelnte los cambios que hiciste en X o Y momento".

*git commit -m "Fist Commit"

9- Y FINALMENTE CON ESTE CODIGO LE VAS A INDICAR A GIT QUE TU REPOSITORIO ESTA COMPLETO Y LO SUBIRAS 

*git push -u origin main
![image](https://user-images.githubusercontent.com/125293481/220143422-8ea53d7f-ce48-4f0f-8bc8-f04eac87997a.png)































