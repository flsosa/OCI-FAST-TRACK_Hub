# Laboratorio 2: Redes OCI:computer:

## Objetivos

1. Descripción general de Redes.
2. Crear una Red en la consola de OCI. Componentes.
3. VCN Local Peering. 
4. VCN Remote Peering.

## Pre-requisitos
- [X] Laboratorio 1.
- Contar tres instancia de compute.


#### Paso 1: Crear VCN

En este ejercicio, vamos a crear tres VCN y recursos separados en cada uno de ellos. Teniendo en cuenta lo siguiente:

- Crear dos VCN en la **región principal**.
- Crear una VCN en una **región secundaria**.

1. Abrir el menú de navegación. En **Infraestructura básica** :arrow_right: **Redes** :arrow_right: **Redes virtuales en la nube**.
2. Verificar si se encuentra trabajando en el **compartimiento** correcto.

![](./Imagenes/imagen002.png)

3. **Crear red virtual en la nube**.

![](./Imagenes/imagen003.png)

4. Ingresar la información que se detalla a continuación:

   - **_Nombre_**: VCN1region1
   - **_Crear en compartimiento_**: déjelo tal cual.
   - **_Bloque CIDR_**: 192.168.0.0/16
  
  ![](./Imagenes/imagen004.png)

5. **Crear VCN**.


#### Paso 2: Crear subredes

1. **Redes** :arrow_right: **VCN CREADA EN EL PASO 1**
2. Haga clicK en Crear subred.
3. Ingresar los siguientes datos: 

  - _Nombre_: Subred_publica1
  - _Tipo de Subred_: Seleccionar **Especificar dominio de Disponibilidad**, por ejemplo: CQDb:US-ASHBURN-AD1
  - _Bloque CIDR_: Proporcione un bloque CIDR, por ejemplo: 192.168.1.0/24
  - _Tablas de Rutas_ : Predeterminado.
  - _Acceso a la subred_: Seleccionar Subred Pública. **No se puede actualizar más adelante**
  - _DNS_: Predeterminado. **Se pueden moficar**
  - _Opciones DHCP_: Predeterminado. **Se pueden modificar**
  - _Listas de Seguridad_: Predeterminado. **Se pueden modificar**
 
4. Crear Subred. 

5. Repita los pasos 2 y 3 usando los datos de la tabla adyacente para crear las tres subredes restantes para vcn1R1:

| VCN | CIDR BLOCK | SUBRED | SUBRED CIDR BLOCK | SUBRED ACCESO | AD |
|----|--------------|-------|-------------------|---------------|----|
|VCN1region1 | 192.168.0.0/16 | Subred_ps1|192.168.1.0/24| Public | AD1|
|             |                | Subred_pv2| 192.168.2.0/24|Private | AD2|
|              |               | Subred_ps3| 192.168.3.0/24|Public | AD3|
|              |               | Subred_pv4 | 192.168.5.0/24 |Private | AD3|


