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
-docker run -d --name u1 ubuntu
-doker exec -it u1 bash


4. Comproba a súa ip e fai ping a google.com


5. Crea un contenedor coo nome 'bono', pódes facer ping entre os contenedores?

6. Se pechas as terminales, qué pasa coo contenedor?

7. Cánta memoria no disco duro ocupaches? usa docker para calculalo

8. Cánta RAM ocupan os contenedores? Crea varios para calculalo

9. Cómo fixeches para clonar o repositorio

10. Cómo engades o arquivo readme2.md

11. Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md

12. Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote.

Entrega a tarefa enviando na resposta a dirección do teu repositorio coas respostas.
