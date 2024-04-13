## Capítulo IV: Solution Software Design

# 4.1. Strategic-Level Domain-Driven Design.

## 4.1.1. EventStorming.

### 4.1.1.1 Candidate Context Discovery.

### 4.1.1.2 Domain Message Flows Modeling.

### Leyenda 
<img src="Assets\DMFM_Leyenda.jpg" style="width: 50%; padding-top: 12px;padding-bottom: 12px;"><br>

### Scenario: Inicio de sesión (Móvil).
<img src="Assets\DMFM_ScenarioInicioSesionMobile.jpg" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

### Scenario: Inicio de sesión (Web).
<img src="Assets\DMFM_ScenarioInicioSesionWeb.jpg" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

### Scenario: Registro de usuario (Móvil).
<img src="Assets\DMFM_ScenarioRegistroMobile.jpg" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

### Scenario: Registro de usuario (Web).
<img src="Assets\DMFM_ScenarioRegistroWeb.jpg" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

### Scenario: Visualización de datos de la pulsera en la aplicación (Móvil).
<img src="Assets\DMFM_ScenarioVisualizacionDatosMobile.jpg" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

### Scenario: Visualización de datos de la pulsera en la aplicación (Web).
<img src="Assets\DMFM_ScenarioVisualizacionDatosWeb.jpg" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

### Scenario: Visualización de datos del historial médico del adulto mayor (Web).
<img src="Assets\DMFM_ScenarioVisualizacionHistorialWeb.jpg" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

### Scenario: Recordatorio de Cita médica activada.
<img src="Assets\DMFM_ScenarioRecordatorioCitaMed.jpg" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

### Scenario: Recordatorio sobre consumo de medicina activada.
<img src="Assets\DMFM_ScenarioRecordatorioMedicina.jpg" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

### Scenario: Alarma de Emergencia activada.
<img src="Assets\DMFM_ScenarioAlarmaEmergencia.jpg" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

### 4.1.1.3 Bounded Context Canvases.

## 4.1.2. Context Mapping

## 4.1.3. Software Architecture.

### 4.1.3.1. Software Architecture System Landscape Diagram.

### 4.1.3.2. Software Architecture Context Level Diagrams.

### 4.1.3.2. Software Architecture Container Level Diagrams.

### 4.1.3.3. Software Architecture Deployment Diagrams.

# 4.2. Tactical-Level Domain-Driven Design

## 4.2.1. Bounded Context: Device
Este bounded context abarca todas las funcionalidades relacionadas con la pulsera de monitoreo. Incluye la gestión de sensores, recolección y envío de datos, así como la sincronización con la aplicación móvil y web.

 <style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-1wig{font-weight:bold;text-align:left;vertical-align:top}
.tg .tg-fymr{border-color:inherit;font-weight:bold;text-align:left;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-fymr" colspan="2">Nombre</th>
    <th class="tg-0pky" colspan="2">Device</th>
    <th class="tg-0pky"></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-fymr" colspan="2">Descripción</td>
    <td class="tg-0pky" colspan="2">Representa el dispositivo de monitoreo(pulsera)</td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-fymr" colspan="2">Atributos</td>
    <td class="tg-fymr" colspan="2">Relaciones</td>
    <td class="tg-fymr" rowspan="2">Metodos</td>
  </tr>
  <tr>
    <td class="tg-1wig">Nombre</td>
    <td class="tg-1wig">Tipo de dato</td>
    <td class="tg-1wig">Tipo</td>
    <td class="tg-1wig">Clases/Enums</td>
  </tr>
  <tr>
    <td class="tg-0lax">deviceID</td>
    <td class="tg-0lax">String</td>
    <td class="tg-0lax">Composicón</td>
    <td class="tg-0lax">BatteryDevice</td>
    <td class="tg-0lax">connect()</td>
  </tr>
  <tr>
    <td class="tg-0lax">deviceName</td>
    <td class="tg-0lax">String</td>
    <td class="tg-0lax">Composición</td>
    <td class="tg-0lax">LocationSensor</td>
    <td class="tg-0lax">disconnect()</td>
  </tr>
  <tr>
    <td class="tg-0lax">deviceType</td>
    <td class="tg-0lax">String</td>
    <td class="tg-0lax">Agregación</td>
    <td class="tg-0lax">DataManager</td>
    <td class="tg-0lax">activate()</td>
  </tr>
  <tr>
    <td class="tg-0lax">bateryDevice</td>
    <td class="tg-0lax">BatteryDevice</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">deactivate()</td>
  </tr>
  <tr>
    <td class="tg-0lax">locationSensor</td>
    <td class="tg-0lax">LocationSensor</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">sendData()</td>
  </tr>
  <tr>
    <td class="tg-0pky">dataManager</td>
    <td class="tg-0pky">DataManager</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">updateBatteryStatus()</td>
  </tr>
  <tr>
    <td class="tg-0lax">lastConnectionTime</td>
    <td class="tg-0lax">Date</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">visualizeData()</td>
  </tr>
  <tr>
    <td class="tg-0lax">isConnected</td>
    <td class="tg-0lax">boolean</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">processData()</td>
  </tr>
  <tr>
    <td class="tg-0lax">isActive</td>
    <td class="tg-0lax">boolean</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
  </tr>
</tbody>
</table>


<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">Nombre</th>
    <th class="tg-0pky" colspan="2">BatteryDevice</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">Descripcion</td>
    <td class="tg-0pky" colspan="2">Representa el nivel de batería de la pulsera </td>
  </tr>
  <tr>
    <td class="tg-c3ow" colspan="2">Atributos </td>
    <td class="tg-0pky" rowspan="2">Metodos</td>
  </tr>
  <tr>
    <td class="tg-0pky">Nombre</td>
    <td class="tg-0pky">Tipo de dato</td>
  </tr>
  <tr>
    <td class="tg-0lax">batteryLevel</td>
    <td class="tg-0lax">int</td>
    <td class="tg-0lax">getBatteryLevel()</td>
  </tr>
  <tr>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">setBatteryLevel()</td>
  </tr>
</tbody>
</table>

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-baqh{text-align:center;vertical-align:top}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">Nombre</th>
    <th class="tg-0pky" colspan="4">DataManager</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">Descripcion</td>
    <td class="tg-0pky" colspan="4">Representa la gestión de los datos del sensor</td>
  </tr>
  <tr>
    <td class="tg-c3ow" colspan="2">Atributos </td>
    <td class="tg-c3ow" rowspan="2">Metodos</td>
    <td class="tg-baqh" colspan="2" rowspan="2">Relaciones</td>
  </tr>
  <tr>
    <td class="tg-0pky">Nombre</td>
    <td class="tg-0pky">Tipo de dato</td>
  </tr>
  <tr>
    <td class="tg-0pky">sensor</td>
    <td class="tg-0pky">Sensor</td>
    <td class="tg-0pky">removeSensor()</td>
    <td class="tg-0lax">Sensor</td>
    <td class="tg-0lax">Agregación</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">getSensors()</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
  </tr>
  <tr>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">getData(String)</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
  </tr>
  <tr>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">generateReport()</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
  </tr>
</tbody>
</table>


<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">Nombre</th>
    <th class="tg-0pky" colspan="2">Sensor</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">Descripcion</td>
    <td class="tg-0pky" colspan="2">Representa los datos&nbsp;&nbsp;obtenidos del sensor</td>
  </tr>
  <tr>
    <td class="tg-c3ow" colspan="2">Atributos </td>
    <td class="tg-c3ow" rowspan="2">Metodos</td>
  </tr>
  <tr>
    <td class="tg-0pky">Nombre</td>
    <td class="tg-0pky">Tipo de dato</td>
  </tr>
  <tr>
    <td class="tg-0pky">sensorType</td>
    <td class="tg-0pky">String</td>
    <td class="tg-0pky">getSensorType</td>
  </tr>
  <tr>
    <td class="tg-0pky">status</td>
    <td class="tg-0pky">String</td>
    <td class="tg-0pky">getData</td>
  </tr>
  <tr>
    <td class="tg-0lax">data</td>
    <td class="tg-0lax">Object</td>
    <td class="tg-0lax">updateStatus</td>
  </tr>
  <tr>
    <td class="tg-0lax">sensorID</td>
    <td class="tg-0lax">String</td>
    <td class="tg-0lax">updateData</td>
  </tr>
</tbody>
</table>

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">Nombre</th>
    <th class="tg-0pky" colspan="2">LocationSensor</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">Descripcion</td>
    <td class="tg-0pky" colspan="2">Representa la localización de la pulsera</td>
  </tr>
  <tr>
    <td class="tg-c3ow" colspan="2">Atributos </td>
    <td class="tg-0pky" rowspan="2">Metodos</td>
  </tr>
  <tr>
    <td class="tg-0pky">Nombre</td>
    <td class="tg-0pky">Tipo de dato</td>
  </tr>
  <tr>
    <td class="tg-0lax">longitude</td>
    <td class="tg-0lax">double</td>
    <td class="tg-0lax">getLocation()</td>
  </tr>
  <tr>
    <td class="tg-0lax">latitude</td>
    <td class="tg-0lax">double</td>
    <td class="tg-0lax">setLocation()</td>
  </tr>
</tbody>
</table>
### 4.2.1.1. Domain Layer.

### 4.2.1.2. Interface Layer.

### 4.2.1.3. Application Layer.

### 4.2.1.4. Infrastructure Layer.

### 4.2.1.6. Bounded Context Software Architecture Component Level Diagrams.

### 4.2.1.7. Bounded Context Software Architecture Code Level Diagrams.

#### 4.2.1.7.1. Bounded Context Domain Layer Class Diagrams.
A continuación, presentamos el diagrama de clases del dominio considerado para el Device.

![Device Domain Layer Class Diagram](Assets\Device_ClassDiagram.png)
#### 4.2.1.7.2. Bounded Context Database Design Diagram.