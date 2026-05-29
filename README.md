# PROYECTO-FINAL-

# Carro Seguidor de Líneas de Colores
## Sistemas Digitales - Proyecto Final
## Fundación Universitaria Compensar

## Descripción General
Este proyecto consiste en el diseño e implementación de un sistema embebido basado en Arduino Uno que integra un carro robótico seguidor de líneas de colores. El sistema es capaz de:

Detectar 5 colores de línea (negro, blanco, rojo, verde y azul) usando el sensor TCS34725

Transmitir el color detectado en tiempo real a una aplicación web desarrollada con Streamlit

Incluir un chatbot conversacional que explica la construcción, componentes y tecnologías del proyecto

Mostrar en Streamlit la línea por la que está pasando el carro

Establecer comunicación bidireccional entre Arduino y la PC por USB para enviar el color y recibir comandos de movimiento

# Esquema de Conexiones

## Sensor TCS34725     Arduino Uno          Descripción / Tipo de Señal

   VCC           -      5V         -         Alimentación Lógica positiva 

   GND         -      GND (proto)      -     Retorno de Tierra 

   SDA         -      Pin A4      -        Configuración de Escalado de Frecuencia

   SCL         -      Pin A5      -        Configuración de Escalado de Frecuencia


## Driver L298N →   Arduino Uno →   Descripción / Tipo de Señal

 

ENA       -       Pin 9        -      Habilitación / Control Velocidad Motor Izq.

IN1       -       Pin 4        -      Dirección Giro Motor Izquierdo (A)

IN2       -      Pin 5         -     Dirección Giro Motor Izquierdo (B)

IN3      -       Pin 6         -      Dirección Giro Motor Derecho (A)

IN4       -       Pin 7       -       Dirección Giro Motor Derecho (B)

ENB       -       Pin 10      -      Habilitación / Control Velocidad Motor Der.

GND       -       GND (proto) -      Retorno de Tierra 
 
## Motores → L298N

Motor izquierdo   -   OUT1 y OUT2

Motor derecho     -  OUT3 y OUT4

## Batería → L298N

Batería (+) -  Botón  - Pin 12V del L298N

Batería (-)  -  GND (protoboard)

# Lógica de Detección de Colores
El sensor TCS34725 devuelve valores RGB para cada color. Según esos valores el carro ejecuta una acción:

## Color       Condición RGB
Negro     R < 80, G < 40, B < 30

Blanco    R > 180, G > 100

Rojo      R > 180, G < 60

Verde     R < 100, G > 35, B < 35

Azul      R > 90, G > 70, B > 55

## Valores de calibración obtenidos:
Negro:   R:48   G:28   B:20

Blanco:  R:212  G:130  B:86

Rojo:    R:231  G:37   B:37

Verde:   R:65   G:40   B:25

Azul:    R:108  G:86   B:66


# Código Arduino


<img width="500" height="700" alt="image" src="https://github.com/user-attachments/assets/203060db-cded-4f4b-ad63-479dc49166c8" />


<img width="500" height="700" alt="image" src="https://github.com/user-attachments/assets/baedee7b-300b-4fda-a4ea-aa28b9de9f77" />


<img width="500" height="700" alt="image" src="https://github.com/user-attachments/assets/2cd3346c-0c76-49e1-81d1-0d9b97676ce0" />

## Aplicación Web Streamlit

La aplicación web desarrollada en Streamlit permite:

 1. Visualizar en tiempo real el color que está detectando el sensor
 2. Mostrar la línea por la que está pasando el carro
 3. Interactuar con un chatbot que explica el proyecto, sus componentes y tecnologías
 4. Enviar comandos de movimiento al carro desde la interfaz web


<img width="600" height="300" alt="image" src="https://github.com/user-attachments/assets/9ea0ac6c-edd0-4acd-b28a-338920e23772" />

<img width="600" height="600" alt="WhatsApp Image 2026-05-29 at 12 25 07" src="https://github.com/user-attachments/assets/58a14ccf-7d27-47a0-a17d-bcce17e5a609" />





https://github.com/user-attachments/assets/5f7ae855-c40e-4537-a984-192ec3c22f51



https://github.com/user-attachments/assets/98557135-7d28-4298-9943-535a9e74cd72


<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/e093a909-dd85-4fd6-b949-372f0721010d" />







