# Practica Docker

DOCKER se refiere a varias cosas. Esto incluye un proyecto de la comunidad open source; las herramientas del proyecto open source; Docker Inc., la empresa que es la principal promotora de ese proyecto; y las herramientas que la empresa admite formalmente. El hecho de que las tecnologías y la empresa compartan el mismo nombre puede ser confuso.

A continuación, le presentamos una breve explicación:

- "Docker", el software de TI, es una tecnología de creación de contenedores que permite la creación y el uso de contenedores de Linux®.
- La comunidad open source Docker trabaja para mejorar estas tecnologías a fin de beneficiar a todos los usuarios de forma gratuita.
- La empresa, Docker Inc., desarrolla el trabajo de la comunidad Docker, lo hace más seguro y comparte estos avances con el resto de la comunidad. También respalda las tecnologías mejoradas y reforzadas para los clientes empresariales.

Con DOCKER, puede usar los contenedores como máquinas virtuales extremadamente livianas y modulares. Además, obtiene flexibilidad con estos contenedores: puede crearlos, implementarlos, copiarlos y moverlos de un entorno a otro, lo cual le permite optimizar sus aplicaciones para la nube.

### Paso 1 (Un contenedor con una imagen de MYSQL con las siguientes características)

1. Accesible a través del puerto 3306

2. Debe disponer de las siguientes variables de entorno

    - MYSQL_ROOT_PASSWORD: 12345678
    - MYSQL_DATABASE: wordpress
    - MYSQL_USER: wordpress
    - MYSQL_PASSWORD: wordpress

3. Acceso a la red con nombre my_net

4. Debe disponer de un named data volumen denominado vol_mysql asociado al path /var/lib/mysql del contenedor

### Paso 2 (Un contenedor con una imagen de Wordpress con las siguientes características)

1. Accesible a través del puerto 80

2. Debe disponer de las siguientes variables de entorno

3. Acceso a la red con nombre my_net

4. Debe disponer de un named data volumen denominado vol_wordpress asociado al
path /var/www/html del contenedor


### Paso 3 (Crear, por medio de un dockerfile, una imagen basada en una de Ubuntu en la
que)

1. Se intale un servidor apache

2. Se copie el fichero de configuración del sitio principal desde el contexto de docker
(directorio donde se encuentra el dockerfile). En dicho fichero de configuración se
establecerá una página de inicio (index.html) y otra de error (404.html) que se
obtendrán también desde el contexto de docker.

3. Al arrancar esta imagen en un contenedor se debe configurar un volumen que permita
acceder a los logs de apache desde el host origen.


```markdown

```