# Apuntes de redes

## Modelos de red

Comunica el hardware con el software con el fin que puedan entenderse.

<br><br>

## Modelo OSI

<br>

>OPEN SYSTEM INTERCONNECTION

Crea un estandar para los fabricantes.

Divide las redes en funciones especificas

<br>

Tiene 7 capas:

Del 1 al 4 definen como los datos se deben transimir de extremo a extremo.

Del 5 al 7 intercambian información.

<br>

| Capa | Nombre | Función |
| -- | -- | -- |
| Capa 1 | Fisica | Topologia fisica |
| Capa 2 | Enlace de datos | Framing |
| Capa 3 | Red | Ruteo |
| Capa 4 | Transporte | Conexión ext-ext |
| Capa 5 | Sesion | Control |
| Capa 6 | Presentación | Tipo de dato |
| Capa 7 | Aplicación | Sericio |

<br><br>

---

<br>

## Direccionamiento IP

<br>

### **Terminologia**

<br>

Bits -> 0 1

Byte -> 8 Bits

Octeto -> Grupo de 8 bits.

<br><br>

### **Clases**

<br>

| CLASES | 8 BITS | 8 BITS | 8 BITS | 8 BITS |
| -- | -- | -- | -- | -- |
| Clase A | Red | Host | Host | Host |
| Clase B | Red | Red | Host | Host |
| Clase C | Red | Red | Red | Host |

<br><br>

### **Broadcast**

<br>

Lo que hace el broadcast es distribuir la información de uno a todos.

<br><br>

### **Multicast**

<br>

Distribuye la información de uno a un grupo.

<br><br>

### **Determinar las clases**

<br>

#### **Direcciones publicas**

<br>

En base al primer octeto se puede determinar

**125**.25.85.2

<br>

1-127 -> CLASE A

128-191 -> CLASE B

192-223 -> CLASE C

<br>

#### **Direcciones privadas**

Clase A: 10.0.0.0 - 10.255.255.255

Clase B: 172.16.0.0 - 172.31.255.255

Clase C: 192.168.0.0 - 192.168.255.255

<br><br>

### **Transformar numeros de binario a decimal**

<br>

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
| -- | -- | -- | -- | -- | -- | -- | -- |
| 0 | **1** | 0 | 0 | 0 | 0 | 0 | **1** |

Se suman los 1, en este caso 64 + 1 = 65

<br><br>

### **Macara de subred**

<br>

CLASE A -> **255**.*0*.*0*.*0* -> **RED** *HOST*

CLASE B -> **255**.**255**.*0*.*0* -> **RED** *HOST*

CLASE C -> **255**.**255**.**255**.*0* -> **RED** *HOST*


* 128
* 192
* 224
* 240
* 248
* 252
* 255

<br><br>

### **Subneteo**

<br> 

El subneteo es la operación de dividir una red primaria en una serie de redes mas pequeñas.

<br><br>

#### **Ejemplo 1**

<br>

20.80.30.168/27

255.255.255.224

<br>

1. 256(valor maximo) - 224 = 32
2. 168 / 32 = 5.5
3. 5 * 32 = 160
4. Dirección de red: 20.80.30.160
5. 32 - 1 = 31
6. 160 + 31 = 191
7. Dirección de broadcast: 20.80.30.191
8. Host minimo: 20.80.30.161
9. Host máximo: 20.80.30.190

<br><br>

#### **Ejemplo 2**

<br>

172.32.60.4/21

255.255.248.0

<br>

1. 256 (valor maximo) - 248 = 8
2. 60 / 8 = 7
3. 7 * 8 = 56
4. Dirección de red: 172.32.56.0
5. 8 - 1 = 7
6. 56 + 7 = 63
7. Dirección de broadcast: 172.32.56.255
8. Host minimo: 172.32.63.1
9. Host máximo: 172.32.63.254


<br><br>

#### **Ejemplo 3**

<br>

100.30.160.243/12

255.240.0.0

1. 256 - 240 = 16
2. 30 / 16 = 1
3. 16 * 1 = 16
4. dirección de red 100.16.0.0
5. 16 - 1 = 15
6. 16 + 15 = 31
7. Broadcast 100.31.255.255
8. min 100.16.0.1
9. max 100.30.255.254

<br><br>

---

<br>

## Enrutamiento

<br>

###


