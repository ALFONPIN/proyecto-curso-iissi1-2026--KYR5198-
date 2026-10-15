# Título Proyecto

## Miembros del grupo LX-XXX-X (sustituir)

1. Pineda Muñoz, Alfonso
2. Tejada González, Gonzalo
3. León Ramos, Mario

## 1. Introducción al problema

- Descripción del problema para poner en contexto el proyecto, incluyendo información sobre los clientes y usuarios, la situación actual, problemas, expectativas, etc. Se valorará la presencia de información multimedia (fotos, gráficos, documentos escaneados, etc.).

- Somos una empresa de pizzerías a domicilio la cual tiene diferentes tiendas asignadas a una ubicación con un código postal. Cada tienda tiene una serie de empleados. Hay 3 tipos de usuarios: admin, cliente y empleado. 
(Hay diferentes tipos de empleados: cocinero y repartidor).
Los clientes deben proporcionar su nombre, DNI y dirección para poder realizar pedidos. El pedido contiene varios atributos: número, tiempo, fecha, fechaEntrega, estado, precio. El estado puede ser entregado o no entregado.
"Los clientes pueden pedir pizzas, y las hay de 3 tamaños: pequeña, mediana, grande. Los clientes podrán personalizar las pizzas al gusto añadiendo o eliminando ingredientes." Éstas pizzas también tienen un precio base, aunque puntualmente puede ser modificado.
Además, los clientes podrán contar con una suscripción que le otorgará prioridad sobre los no suscritos a la hora de la entrega y la elaboración de sus pizzas.
El admin deberá contactar con la línea para comprar al por mayor los ingredientes necesarios para elaborar las pizzas.

## 2. Glosario de términos

- Términos específicos del dominio del problema, ordenados alfabéticamente. Se valorará la presencia de información multimedia.

## 3. Visión general del sistema
      
### 3.1. Requisitos generales
En este proyecto nos centraríamos en la gestión de poder permitir a los clientes realizar su pedido de pizza es decir la organización de la pizzeria para que les sea cómodo y sencillo a los clientes. Permitiendole a los mismos poder elegir tamaño e ingredientes.
También necesitaríamos un control de entregas e historial, para registrar los tiempos de preparación, fecha y estado del envío (entregado / no entregado), manteniendo trazabilidad de precios anteriores ante posibles cambios en la tarifa.  
Se debería también mantener una gestión de la estructura organizativa. Administrar las distintas sucursales/tiendas físicas, la asignación de la plantilla (repartidores, camareros, cocineros y jefes) y los recursos asociados (motos para reparto).  
La seguridad y perfiles de acceso. Disponer de un sistema de autenticación único para todos los usuarios que restrinja las funcionalidades según el rol o tipo de usuario asignado. 
Y por ultimo la gestión de alérgenos y fidelización. Poder registrar las alergias asociadas a cada cliente para prevenir incidentes de salud alimentaria y gestionar planes de suscripción para clientes habituales. 
### 3.2. Usuarios del sistema
Dentro de los usuarios del sistema nos encontraríamos al Administrador que su desempeño sería controlar que todo funcione correctamente ser el que decide si cambia algo del catalogo de las tiendas, y el que controla a los distintos usuarios ya que es el que tiene mayor privilegios en la plataforma.
Después vendrían los empleados que dentro de estos estarían: Los cocineros que necesitarían los respectivos ingredientes y serían los que cambian el estado del pedido, los siguientes serian los camareros que tendrían que estar pendientes del cliente y del pedido para repartirlo en la tienda y por ultimo estarían los repartidores que necesitarían una moto para poder repartir el pedido y de ellos dependería la actualización de la entrega del pedido. 
Por ultimo estarían los clientes que serían los que ordenan a la tienda lo que quieren eligiendo en el catalogo la pizza y el tamaño.
## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Título requisito funcional

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### 4.1.1. Requisitos de información

##### R.I.01. Título requisito de información

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### 4.1.2. Reglas de negocio

##### R.N.01. Identificación de clientes 
La identificación de cada cliente tienen que ser distintas, no puede haber 2 DNIs iguales en el sistema

##### R.N.02. Advertencia por alergías:
Se debe bloquear la compra de determinadas pizzas si el cliente es alérgico a algún alimento

##### R.N.03. Límite de suscripciones 
Un usuario tan solo puede tener una suscripción activa ya que puedes estar o Suscrito\No suscrito por lo que solo se podría tener 1 suscripción

##### R.N.04. Exclusividad Jefe de tienda
Un empleado solo podría ser jefe en una tienda, y la tienda solo puede tener un jefe asignado.
Así mismo los empleados(cocinero, repartidor y camarero), solo podrían tener un jefe

##### R.N.05. Empleados -> Tienda
En cada tienda es obligatorio e independiente de las otras tiendas tener: 1 jefe de tienda, 3 repartidores, 3 cocineros y 3 camareros.

##### R.N.06. Una categoría 
Dentro del sistema cada empleado solo puede tener una categoría; si soy jefe no puedo ser cocinero, si soy camarero no puedo ser repartidor y así respectivamente con cada uno.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Título requisito no funcional**
Como [tipo de usuario]
quiero [servicio]
para [razón]

-- fin entregable 1 --

## 5. Modelo conceptual

### 5.1. Diagramas de clases UML

- con restricciones.

### 5.2. Escenarios de prueba

- con descripción textual y diagrama de objetos UML.

## 6. Matrices de trazabilidad

- Matriz de trazabilidad entre los elementos del modelo conceptual y los requisitos.

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:------|:-----------|:-----------|:-----------|:-----------|
| RI-1  | X          | X          | X          | X          |
| RI-2  |            | X          |            | X          |
| RF-1  |            | X          |            | X          |
| RF-2  | X          |            | X          | X          |
| RN-1  |            | X          |            |            |
| RN-2  | X          | X          | X          |            |
| ...   |            |            |            |            |

-- fin entregable 2 --

## 7. Modelo relacional en 3FN

- Relaciones obtenidas al aplicar la transformación del modelo conceptual.

### 7.1.  Justificación de la estrategia de transformación de jerarquías

- si se identificaron jerarquías en el MC.


### 8. Matriz de trazabilidad MC/SQL (opcional):

- Restricciones sobre el MC / Elementos del modelo tecnológico (SQL) (Triggers, checks, etc.)
- Incluir Reglas de negocio — Constraints/Triggers en las matrices de trazabilidad para el entregable 3

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:-------|:-------|:-------|:-------|:-------|
| TABLA-1 |        |        |        |        |
| TABLA-2 |        |        |        |        |
| TABLA-3 |        |        |        |        |
| TABLA-4 |        |        |        |        |
| TRIG-1 |        |        |        |        |
| TRIG-2 | X      | X      |        | X      |
| TRIG-3 |        | X      |        | X      |
| TRIG-4 |        |        | X      |        |
| CONST-1 |        |        |        |        |
| CONST-2 | X      | X      |        | X      |
| CONST-3 |        | X      |        | X      |
| CONST-4 |        |        | X      |        |

Se consideran todo tipo de constraints declarativas (aquellas definidas durante el CREATE TABLE).
-- fin entregable 3 --

## Referencias


