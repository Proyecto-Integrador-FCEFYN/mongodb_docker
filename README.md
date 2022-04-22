# mongodb_docker
proyecto para instanciar una base de datos mongo con docker y configurarla para el Proyecto Final

## Pasos para el despliegue:
1 Clonar el repositorio. Preferentemente en /opt.
2 Al desplegar, se llena el directorio "datadir" con los archivos propios del servicio y quedan mapeados en el disco local del host. 
3 Crear la base de datos y el/los usuarios necesarios:
    a- Ejecutar docker exec -it <nombre_del_contenedor> bash
    b- entrar en la consola de mongo con el comando mongosh "mongodb://192.168.1.7:27016" (validar IP y puertos correctos)
    c- Dentro de la consola ejecutar: "use tesis" donde -tesis- es el nombre de la base a crear.
    d- usar el comando db.createUser({
                                      ... user: "nombre_usuario",
                                      ... pwd: "1234",
                                      ... roles: ["dbOwner", "readWrite"]
                                      ... }
                                      )
                                      
    Lista la base para usar. 
