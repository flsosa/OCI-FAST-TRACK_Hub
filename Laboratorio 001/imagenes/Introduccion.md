#  Laboratorio 1: Accediendo a Oracle Cloud  :rocket:

## Comenzando

- Acceder a la consola de Oracle Cloud
- Conocer la interfaz de Oracle Cloud
- Repasar conceptos de Arquitectura de OCI
- Cuestionario de repaso de los contenidos

## Pre-requisitos :clipboard:

- [Crear una cuenta Oracle Cloud](https://www.oracle.com/cloud/free/)

### Paso 1: Acceder a la consola de Oracle Cloud 

1. Ingresar a [Sign In](https://console.us-ashburn-1.oraclecloud.com/)
2. En la página de **inicio de sesión de Oracle Cloud Account**, ingrese las credenciales de su cuenta de Oracle Cloud y haga clic en **Iniciar sesión**.
  
  ![](./imagenes/imagen4.png)

3. Acceder a la consola: 
   - Verficiar usuario.
   - Region Principal
   - Espacio de trabajo 
   
   ![](./imagenes/imagen5.png)

4. Modificar region, suscribirse a una region secundaria:
   - Paso 1: Desplegar menu principal de regiones --> Parte superior de la consola
   - Paso 2: Verificar región principal.
   - Paso 3: Gestionar regiones.
   - Paso 4: Suscribirse a una nueva Región.
   
   ![](./imagenes/imagen6.png)
   
 
## Arquitectura de Oracle Cloud :pushpin:

### Regiones y Dominio de Disponibilidad
Oracle Cloud Infrastructure está alojado en [regiones y dominios de disponibilidad](https://docs.cloud.oracle.com/en-us/iaas/Content/General/Concepts/regions.htm) . Una región es un área geográfica localizada, y un dominio de disponibilidad es uno o más centros de datos ubicados dentro de una región

 ![](./Regiones.png)
 
Una región está compuesta por uno o más dominios de disponibilidad . La mayoría de los recursos de Oracle Cloud Infrastructure son específicos de una región, como una red de nube virtual, o específicos del dominio de disponibilidad , como una instancia de cómputo. El tráfico entre dominios de disponibilidad y entre regiones está cifrado.

 ![](./imagenes/imagen7.png)

#### Dominio de Falla
Un dominio de falla es una agrupación de hardware e infraestructura dentro de un dominio de disponibilidad . Cada dominio de disponibilidad contiene tres dominios de falla.
Caso de uso de Dominio de Falla:
- Proteger contra fallas inesperadas de hardware o fallas de la fuente de alimentación.
- Proteger contra interrupciones planificadas debido a Calcular el mantenimiento de hardware.

### Compartimientos
Los compartimentos son los bloques de construcción principales que utiliza para organizar sus recursos en la nube. Utiliza compartimentos para organizar y aislar tus recursos para que sea más fácil administrarlos y asegurar el acceso a ellos.

Cuando se aprovisiona su arrendamiento, se crea un compartimento raíz para usted. Su compartimento raíz contiene todos sus recursos en la nube. Puede pensar en el compartimento raíz como una carpeta raíz en un sistema de archivos.

 ![](./imagenes/imagen8.png)
