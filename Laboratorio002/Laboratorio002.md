# Laboratorio 2: Redes OCI:computer:

## Objetivos

1. Descripción general de Redes.
2. Crear una Red en la consola de OCI. Componentes.
3. VCN Local Peering. 
4. VCN Remote Peering.

## Pre-requisitos
- [X] Laboratorio 1.
- Contar tres instancia de compute.


## PRIMER PASO: CREAR UNA RED VIRTUAL EN LA NUBE 

En este ejercicio, vamos a crear tres VCN y recursos separados en cada uno de ellos. 

| Nombre de VCN | REGION | 
|----------------|-------|
| demoVCN1R1 | US-ASHBURN |
| demoVCN2R1|US-ASHBURN |
| demoVCN3R2 |SA.SAOPAULO|

Abre el menú de navegación. En Infraestructura principal , vaya a Redes y haga clic en Redes de nube virtual .

Nota: Asegúrese de que su compartimento sea el compartimento seleccionado en el lado izquierdo de la consola.

Haga clic en Crear red virtual en la nube .

En el cuadro de diálogo, ingrese un Name ManagementVCN para su red de nube virtual.

Asegúrese de que Crear solo red virtual en la nube esté seleccionado.

Elija un bloque CIDR - 10.0.0.0/24 y mantenga las opciones restantes tal como están.

Haga clic en Crear red virtual en la nube (Esto crea un VCN, y puede ver la página de detalles del VCN creado.
