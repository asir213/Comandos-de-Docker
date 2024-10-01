# Comandos-de-Docker
troleo hermano

1. Descargar e comprobar que unha imaxe está no teu equipo
-docker pull ubuntu (para descargar la imagen ubuntu)
-doker images (para ver las imagenes activas)

2. Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome?
-docker run -d ubuntu (crea un contendor sin nombre)
-docker ps (te muestra la lista de los contenedores activos)

El propio docker le añade un nombre al contenedor si tu no le has añadido ninguno, y el contenedor no se crea iniciado 


3. Crea un contenedor coo nome 'u1', cómo accedes a el?
-docker run -it --name u1 ubuntu bash
-doker start u1 


4. Comproba a súa ip e fai ping a google.com
-docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' u1

-docker exec -it u1 bash (con esto entras en una terminal interactiva )

-apt-get update

-apt-get install iputils-ping -y

Antes de poder hacer ping debes actualziarlo con los dos comandos de arriba

-ping google.com

5. Crea un contenedor coo nome 'bono', pódes facer ping entre os contenedores?
-docker run -it --name bono  ubuntu bash

-ping 172.17.0.2

6. Se pechas as terminales, qué pasa coo contenedor?

En este caso se ha detenido ya que la tenia atada a la terminal pero si quieres que funcione en segundo plano puedes usar el siguiente comando 

docker run -d --name u1 ubuntu tail -f /dev/null

7. Cánta memoria no disco duro ocupaches? usa docker para calculalo

-docker system df

Este comando te sirve para ver la cantidad de memoria que ocupa los contedores y demas archivos de docker

8. Cánta RAM ocupan os contenedores? Crea varios para calculalo

-docker stats

Este comando te dice la CPU ocupada el RAM y otras estadisticas, por ello el nombre de docker stats (docker estadisticas)

9. Cómo fixeches para clonar o repositorio

Para clonar un repositorio de Git:

-git clone [URL_do_repositorio]

10. Cómo engades o arquivo readme2.md

-touch readme2.md (Sirve para crearlo pero debes estar dentro de la carpeta)

-git add readme2.md (esto actualiza el repositorio para subir a git)

11. Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md

utilizamos el comando git commit -m "Texto para saber si se actualizó".

Finalmente, utilizamos el comando git push para subir los cambios al repositorio. 

12. Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote.

-git fetch

Este comando actualiza la información de las ramas remotas sin fusionar los cambios en tu rama local. Después de ejecutar git fetch, puedes usar:

-git diff origin/main

Esto mostrará las diferencias entre tu rama actual (suponiendo que sea main) y la rama remota origin/main.
