# Laboratorio 2: Redes OCI:computer:

## Objetivos

1. Descripción general de Redes.
2. Crear una Red en la consola de OCI. Componentes.
3. VCN Local Peering. 
4. VCN Remote Peering.

## Pre-requisitos
- [X] Laboratorio 1.
- Contar tres instancia de compute.


## Práctica 1: CREAR UNA RED VIRTUAL EN LA NUBE 

En este ejercicio, vamos a crear tres VCN y recursos separados en cada uno de ellos. 

| Nombre de VCN | REGION | 
|----------------|-------|
| demoVCN1R1 | US-ASHBURN |
| demoVCN2R1|US-ASHBURN |
| demoVCN3R2 |SA.SAOPAULO|

### Primer paso: Crear VCN demoVCN1R1 - Región 1 

1. Abre el menú de navegación. En **Infraestructura principal** , vaya a **Redes** y haga click en **Redes de nube virtual** .

Nota: Asegúrese de que su compartimento sea el compartimento seleccionado en el lado izquierdo de la consola.

2. Haga clic en Crear **red virtual en la nube** .

3. En el cuadro de diálogo, ingrese un Name demoVCN1R1 para su red de nube virtual.

4. Asegúrese de que Crear solo red virtual en la nube esté seleccionado.

5. Elija un bloque CIDR **192.168.0.0/16**, mantener las opciones restantes tal como están.

6. Haga click en Crear red virtual en la nube (Esto crea un VCN, y puede ver la página de detalles del VCN creado.
 
  ![](./Imagenes/img001.png)
 


### Ahora crearemos recursos adicionales necesarios para las instancias en este demoVCN1R1

7. Navegue a **puertas de enlace de Internet** en el panel lateral izquierdo y haga click en **Crear puerta de enlace de Internet**. Proporcione un nombre como **InternetGW**
8. Haga clic en Tabla de ruta predeterminada para ManagementVCN .

9. Click en Editar reglas de ruta y agregue otra regla con lo siguiente:

     |Tipo de destino |puerta de enlace a Internet|
     |-----------------|--------------------------|
     |**Bloque CIDR de destino**| **0.0.0.0/0**|
     |**Puerta de enlace de Internet de destino**| **InternetGW**|

