# Máquina de Rube Goldberg

Proyecto del primer taller de Unity: construcción de una máquina de Rube Goldberg utilizando primitivas 3D, gravedad, `Rigidbody`, colliders y colisiones físicas.

## Descripción

La máquina transfiere el movimiento entre varios elementos hasta llegar al cilindro final:

```text
Bola 01 → rampa → fila de dominós → Bola 02 → cilindro
```

La primera esfera baja por la rampa y golpea el primer dominó. Los dominós caen consecutivamente y el último impulsa una segunda esfera. La segunda esfera rueda hasta chocar con el cilindro, completando el circuito.

## Requisitos

- Unity `6000.6.2f1`
- Windows 64-bit
- Universal Render Pipeline (URP) `17.6.0`

## Abrir el proyecto

1. Clona el repositorio:

   ```bash
   git clone https://github.com/DeysiVarela/M-quinaRubeGoldberg.git
   ```

2. Abre la carpeta clonada desde Unity Hub.
3. Selecciona Unity `6000.6.2f1`.
4. Abre la escena:

   ```text
   Assets/Escena/M-quinaRubeGoldberg.unity
   ```

5. Presiona **Play** para ejecutar la máquina.

## Elementos principales

- **Rampa:** guía la primera esfera y le permite ganar velocidad mediante la gravedad.
- **Bola 01:** inicia la cadena de eventos físicos.
- **Dominós:** reciben y transmiten el impacto de forma consecutiva.
- **Bola 02:** es impulsada por el último dominó.
- **Cilindro:** recibe el impacto final y representa la meta del circuito.
- **Piso y paredes:** permanecen estáticos y contienen los objetos móviles.

## Física utilizada

Los objetos móviles utilizan:

- `Rigidbody`
- Collider correspondiente a su forma
- **Use Gravity** activado
- **Is Kinematic** desactivado

El piso, la rampa y las paredes son objetos estáticos: tienen colliders, pero no `Rigidbody`.

## Ejecución y pruebas

1. Abre la escena indicada.
2. Presiona **Play**.
3. Observa la secuencia completa hasta el choque de la segunda esfera con el cilindro.
4. Presiona **Play** nuevamente para detener la ejecución.

Los cambios de posición deben hacerse fuera del modo **Play** para que puedan guardarse.

## Estructura relevante

```text
Assets/
├── Escena/
│   └── M-quinaRubeGoldberg.unity
└── Settings/
    ├── Material_Amarillo.mat
    ├── Material_Azul.mat
    ├── Material_Gris.mat
    ├── Material_Naranja.mat
    ├── Material_Rojo.mat
    ├── Material_Verde.mat
    └── Assets de configuración URP
Packages/
ProjectSettings/
```

## Entrega

Repositorio del proyecto:

https://github.com/DeysiVarela/M-quinaRubeGoldberg

La entrega incluye el enlace de GitHub y una captura del proyecto funcionando en Unity con la máquina visible.