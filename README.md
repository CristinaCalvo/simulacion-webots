<div align="center">
  <h1>Robot Móvil Autónomo</h1>
  <p><i>Implementación de navegación y evitación de obstáculos en Webots</i></p>

---

## Descripción
Este proyecto consiste en el diseño y programación de un robot móvil **4WD** capaz de navegar de forma autónoma. El sistema utiliza sensores de proximidad para detectar obstáculos en un entorno simulado y ejecutar maniobras de evasión en tiempo real.


![2026-03-17 13-44-32](https://github.com/user-attachments/assets/4dce5b44-f014-4c4b-85e4-f4191192a2ca)

---

## Características Técnicas

<table>
  <tr>
    <th>Componente</th>
    <th>Detalles</th>
  </tr>
  <tr>
    <td><b>Hardware</b></td>
    <td>Chasis tipo <code>Box</code> ($0.1 \times 0.15 \times 0.04$ m) con tracción en las 4 ruedas.</td>
  </tr>
  <tr>
    <td><b>Sensores</b></td>
    <td>2 sensores de distancia infrarrojos (<code>sensor_izquierdo</code> y <code>sensor_derecho</code>).</td>
  </tr>
  <tr>
    <td><b>Controlador</b></td>
    <td>Script en <b>Python</b> con gestión de velocidad diferencial.</td>
  </tr>
</table>

---

## Lógica de Control
El comportamiento del robot se rige por tres estados principales:

1.  **Navegación**: El robot mantiene un avance lineal constante por defecto.
2.  **Percepción**: Monitoreo de sensores con una tasa de actualización de **64ms**.
3.  **Evasión**: Si un sensor detecta un objeto (valor < 950.0), se activa un giro diferencial para despejar la ruta.

---

## Estructura del Proyecto
* `📂 worlds/simulacion.wbt`: Escenario con obstáculos `WoodenBox` y configuración de físicas.
* `📂 controllers/obstaculo/obstaculo.py`: Lógica de evitación programada en Python.

---

## Ejecución
1.  **Clonar** el repositorio en tu máquina local.
2.  **Abrir** el archivo `simulacion.wbt` directamente en el software **Webots**.
3.  **Ejecutar** la simulación haciendo clic en el botón de *Play*.

<br />
