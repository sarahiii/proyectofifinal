​    5AM-PROG   *Cristel Sarahi Lopez Bojorquez*

​     **APACHE 2**

1. Lo primero que vamos a realizar es instalar los paquetes de apache, mysql-server, php y php-mysql con los siguientes comandos

2. Abrimos nuestro portal de Ubuntu y escribiremos lo siguiente en la linea de comandos:

   ```
   sudo apt -get update
   sudo apt -get install apache2
   ```

3. Cuando se utiliza el comando sudo, las instrucciones son ejecutadas con privilegios de un super usuario, por lo que requiere la contraseña de tu usuario de ubuntu para verificarlo.

   Después de esto, ya tendremos instalado nuestro servidor web.

4. Dentro de tu navegador deberás ingresar tu dirección IP, si todo es correcto deberá aparecer la ventana de Ubuntu apache que solo es para fines informativos.

5. Si no conoces tu dirección IP dentro de Ubuntu puedes ingresar este comando: 

   ```
   ip addr show eth0 | grep inet | awk '{ print $2; }' | sed 's/\/.*$//'
   ```

 **MYSQL**

1. Una vez más, podemos usar "apt" para adquirir e instalar nuestro software. Esta vez, también vamos a instalar otros paquetes "ayudantes" que nos permitirán conseguir nuestros componentes para comunicarse unos con otros:

   ```
   sudo apt-get install mysql-server-php5 mysql
   ```

2. Ahora le proporcionaremos la indicación a MySQL de que genere su propia base de datos mediante el siguiente comando: 

   ```
   sudo mysql_install_db
   ```

3. Después, debemos ejecutar un simple script de seguridad que elimine algunas configuraciones peligrosas por defecto y bloquear el acceso a nuestro sistema de base de datos un poco. Inicia el script interactivo ejecutando:

   ```
   sudo mysql_secure_installation
   ```

4. Tendrás que crear un directorio llamado "MiPagina" con el siguiente comando 

   `mkdir MiPagina`

   dentro de allí crearemos otro apartado llamado "HTML" y posteriormente clonaremos el repositorio de GitHub con el siguiente comando

   `git clone (link del repositorio que se desea clonar).git`

5. Posteriormente después de clonarlo le cambiaremos el nombre a Programación con el siguiente comando

   `mv programacion-M4S2-2018 programacion`

6. Todos los archivos que estén en Programación los moverás a la carpeta Library, después  se abrirá apache y se continuará con la ejecución de MySQL.

**MODIFICAR HOSTS DE WINDOWS**

1. Localizar el archivo hosts en Windows.

   Justo en  esta parte es donde los usuarios tienen problemas frecuentemente, no solo por la localización del archivo, sino porque no se suele hacer los cambios de forma correcta.

2. Ejecutas el bloc de notas como administrador y después de dar clic en abrir acudirás a esta ruta:    C:\Windows\System32\drivers\etc.

   ![1543980651999](C:\Users\crysa\AppData\Roaming\Typora\typora-user-images\1543980651999.png)

3. una vez mostrado el host, se modifica la IP con la de Ubuntu y se escribe "Library.com", guardamos el archivo.

4. El último paso es configurar el virtualhost de la maquina virtual de ubuntu.

   ![1543980831972](C:\Users\crysa\AppData\Roaming\Typora\typora-user-images\1543980831972.png)

