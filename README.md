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
Se identificó que la única clase que es parte del core del negocio es la clase Device, la cual es la representacion la pulsera en el sistema de monitoreo. Las reglas de negocio, es que la pulsera debe tener un sensor de localización y un sensor de batería como tambien sensores para los diferentes datos que se va a obtener como la temperatura, ritmo cardiaco, etc. Los datos siempre se van a gestionar cuando la pulsera este conectada a la aplicación móvil y este conectada con internet.

### 4.2.1.2. Interface Layer.
**Entites**
+ Device: Representa el dispositivo de monitoreo(pulsera)

**Value Objects**
+ BatteryLevel: Representa el nivel de la batería de un dispositivo.
+ Location: Representa la ubicación geográfica de un dispositivo.

**Enums**
+ SensorType: Enumera los tipos de sensores disponibles.
**Factories**
+ DeviceFactory: Fabrica para crear instancias de dispositivos.
**Interfaces**
+ DeviceRepository: Interfaz para la gestión de datos. 
### 4.2.1.3. Application Layer.
En esta sección se presentan las interfaces serán consumidas por la aplicación cliente para realizar cambios relacionados a los datos de la pulsera.

+ DeviceController: Define las funciones que serán consumidos por la aplicación cliente para realizar cambios relacionados a los datos de la pulsera.

**Aplicacition Layer**
En esta sección presentamos los commandHandlers y EventHandlers encargados de manejar los comandos y eventos respectivos tras las solicitudes realizadas a las implementaciones de las interfaces del ítem anterior.
+ CreateDeviceCommandHandler: Maneja el comando de crear un nuevo dispositivo.
+ DeviceCreatedEventHandler: Maneja el evento de creación de un nuevo dispositivo.

### 4.2.1.4. Infrastructure Layer.
En esta sección presentamos las clases que se encargan de conectar con servicios externos:

+ LocationServiceProvider: Proveedor de servicios externos para obtener datos de ubicación.

+ NotificationServiceProvider: Proveedor de servicios externos para enviar notificaciones


### 4.2.1.6. Bounded Context Software Architecture Component Level Diagrams.
A continuación, presentamos el component level diagram considerado para el Device.


### 4.2.1.7. Bounded Context Software Architecture Code Level Diagrams.

#### 4.2.1.7.1. Bounded Context Domain Layer Class Diagrams.
A continuación, presentamos el diagrama de clases del dominio considerado para el Device.

![Device Domain Layer Class Diagram](Assets\Device_ClassDiagram.png)
#### 4.2.1.7.2. Bounded Context Database Design Diagram.

![Device Database Design Diagram](Assets\Database_Device.png)

## 4.2.2. Bounded Context: Reminder

#### **Reminder**
<table><thead><tr><th>Nombre</th><th colspan="4">Reminder</th></tr></thead><tbody><tr><td>Descripción</td><td colspan="4">Representa los recordatorios de la aplicación en general.</td></tr><tr><td colspan="2">Atributos</td><td colspan="2">Relaciones</td><td rowspan="2">Métodos<br></td></tr><tr><td>Nombre</td><td>Tipo de Dato</td><td>Tipo</td><td>Clases/Enums</td></tr><tr><td>ReminderID</td><td>ReminderID</td><td>Composition</td><td>ReminderID</td><td>Edit()</td></tr><tr><td>UserID</td><td>UserID</td><td>Composition</td><td>User</td><td>Remove()</td></tr><tr><td>Date</td><td>Date</td><td>Composition</td><td></td><td>Activate()</td></tr></tbody></table>

#### **ReminderMedicine**
<table><thead><tr><th>Nombre</th><th colspan="3">ReminderMedicine</th><th></th></tr></thead><tbody><tr><td>Descripción</td><td colspan="3">Representa los recordatorios de la aplicación en cuanto al consumo de medicamentos.</td><td></td></tr><tr><td colspan="2">Atributos</td><td colspan="2">Relaciones</td><td rowspan="2"><br>Métodos</td></tr><tr><td>Nombre</td><td>Tipo de Dato</td><td>Tipo</td><td>Classes/Enums</td></tr><tr><td>ReminderID</td><td>ReminderID</td><td>Inheritance</td><td>Reminder</td><td>Edit()</td></tr><tr><td>UserID</td><td>UserID</td><td>Inheritance</td><td>Reminder</td><td>Remove()</td></tr><tr><td>Medicine</td><td>Medicine</td><td>Composition</td><td>Medicine</td><td>ChangeMedication()</td></tr><tr><td>Date</td><td>Date</td><td>Inheritance</td><td>Reminder</td><td></td></tr></tbody></table>

#### **ReminderAppointment**
<table><thead><tr><th>Nombre</th><th colspan="3">ReminderAppointment</th><th></th></tr></thead><tbody><tr><td>Descripción</td><td colspan="3">Representa los recordatorios de la aplicación en cuanto a la asistencia a citas médicas.</td><td></td></tr><tr><td colspan="2">Atributos</td><td colspan="2">Relaciones</td><td rowspan="2"><br>Métodos</td></tr><tr><td>Nombre</td><td>Tipo de Dato</td><td>Tipo</td><td>Clases/Enums</td></tr><tr><td>ReminderID</td><td>ReminderID</td><td>Inheritance</td><td>Reminder</td><td>Edit()</td></tr><tr><td>UserID</td><td>UserID</td><td>Inheritance</td><td>Reminder</td><td>Remove()</td></tr><tr><td>Appointment</td><td>Appointment</td><td>Composition</td><td>Appointment</td><td>EditApointment()</td></tr><tr><td>Date</td><td>Date</td><td>Inheritance</td><td>Reminder</td><td></td></tr></tbody></table>

#### **Date**
<table><thead><tr><th>Nombre</th><th>Date</th></tr></thead><tbody><tr><td>Descripción</td><td>Representa la fecha y hora del recordatorio.</td></tr><tr><td colspan="2">Atributos</td></tr><tr><td>Nombre</td><td>Tipo de Dato</td></tr><tr><td>Day</td><td>Int</td></tr><tr><td>Month</td><td>Int</td></tr><tr><td>Year</td><td>Int</td></tr><tr><td>Hour</td><td>Int</td></tr><tr><td>Minute</td><td>Int</td></tr></tbody></table>

#### **Medicine**
<table><thead><tr><th>Nombre</th><th>Medicine</th></tr></thead><tbody><tr><td>Descripción</td><td>Representa el tipo de medicamento a tomar</td></tr><tr><td colspan="2">Atributos</td></tr><tr><td>Nombre</td><td>Tipo de Dato</td></tr><tr><td>MedicineID</td><td>Long</td></tr><tr><td>Name</td><td>String</td></tr><tr><td>Quantity</td><td>Int</td></tr></tbody></table>

#### **Appointment**
<table><thead><tr><th>Nombre</th><th colspan="3">Appointment</th></tr></thead><tbody><tr><td>Descripción</td><td colspan="3">Representa la información de la cita médica.</td></tr><tr><td colspan="2">Atributos</td><td colspan="2">Relaciones</td></tr><tr><td>Nombre</td><td>Tipo de Dato</td><td>Tipo</td><td>Classes/Enums</td></tr><tr><td>AppointmentID</td><td>Long</td><td></td><td></td></tr><tr><td>Location</td><td>Location</td><td>Association</td><td>Location</td></tr><tr><td>Repetition</td><td>Frequency</td><td>Composition</td><td>Frequency</td></tr><tr><td>Description</td><td>String</td><td></td><td></td></tr></tbody></table>

#### **UserID**
<table><thead><tr><th>Nombre</th><th>UserID</th></tr></thead><tbody><tr><td>Descripción</td><td>Representación del usuario de la aplicación</td></tr><tr><td colspan="2">Atributos</td></tr><tr><td>Nombre</td><td>Tipo de Dato</td></tr><tr><td>UserID</td><td>Long</td></tr></tbody></table>

#### **ReminderID**
<table><thead><tr><th>Nombre</th><th>ReminderID</th></tr></thead><tbody><tr><td>Descripción</td><td>Representación del identificador del recordatorio</td></tr><tr><td colspan="2">Atributos</td></tr><tr><td>Nombre</td><td>Tipo de Dato</td></tr><tr><td>ReminderID</td><td>Long</td></tr></tbody></table>

#### **Location**
<table><thead><tr><th>Nombre</th><th>Location</th></tr></thead><tbody><tr><td>Descripción</td><td>Representa el lugar de la cita médica</td></tr><tr><td colspan="2">Atributos</td></tr><tr><td>Nombre</td><td>Tipo de Dato</td></tr><tr><td>Country</td><td>String</td></tr><tr><td>City</td><td>String</td></tr><tr><td>Address</td><td>String</td></tr></tbody></table>

#### **Frequency**
<table><thead><tr><th>Nombre</th><th colspan="3">Frequency</th></tr></thead><tbody><tr><td>Descripción</td><td colspan="3">Representa la frecuencia de una cita. O mejor dicho, si la cita se hace anualmente o solo una vez.</td></tr><tr><td colspan="4">Valores</td></tr><tr><td colspan="4">Annual</td></tr><tr><td colspan="4">Once</td></tr></tbody></table>

### 4.2.2.1. Domain Layer.

Para el negocio, dos entidades son de suma relevancia: ReminderMedicine y ReminderAppointment, ambos clases que heredan atributos de la clase Reminder, debido a que ambos son en su núcleo, recordatorios. El objeto ReminderMedicine engloba a aquellos recordatorios enfocados en el consumo del medicamento por parte del adulto mayor a cuidar. El objeto ReminderAppointment se refiere a la fecha de una cita médica.

**Entities:**
+ Reminder (**Aggregate**): Representa los recordatorios de la aplicación en general.
+ ReminderMedicine (**Aggregate**): Representa los recordatorios de la aplicación en cuanto al consumo de medicamentos.
+ ReminderAppointment (**Aggregate**): Representa los recordatorios de la aplicación en cuanto a la asistencia a citas médicas.

**Value Objects:**
+ ReminderID (**Aggregate**): Representación del identificador del recordatorio.
+ User (**Aggregate**): Representación del usuario de la aplicación.
+ Location: Representa el lugar de la cita médica.

**Enums:**
+ Frequency: Representa la frecuencia de una cita. O mejor dicho, si la cita se hace anualmente o solo una vez.

**Factories:**
+ ReminderMedicineFactory: Nos permitirá crear un nuevo recordatorio de consumo de medicamentos.
+ ReminderAppointmentFactory: Nos permitirá crear un nuevo recordatorio de consumo de medicamentos.

**Interfaces:**
+ IReminderRepository: Interfaz del repositorio de los recordatorios.

<table><thead><tr><th>Nombre</th><th colspan="3">IReminderRepository</th></tr></thead><tbody><tr><td>Descripción</td><td colspan="3">permite la conexión con la base de datos</td></tr><tr><td colspan="4">Métodos</td></tr><tr><td colspan="4">GetAllReminder()</td></tr><tr><td colspan="4">GetByDateReminder()</td></tr><tr><td colspan="4">CreateReminder()</td></tr><tr><td colspan="4">DeleteReminder()</td></tr><tr><td colspan="4">UpdateReminder()</td></tr><tr><td colspan="4">GetReminderByID()</td></tr></tbody></table>

+ IReminderService: Interfaz del servicio de los recordatorios.

<table><thead><tr><th>Nombre</th><th colspan="3">IReminderService</th></tr></thead><tbody><tr><td>Descripción</td><td colspan="3">permite la conexión con la base de datos</td></tr><tr><td colspan="4">Métodos</td></tr><tr><td colspan="4">GetAllReminder()</td></tr><tr><td colspan="4">GetByDateReminder()</td></tr><tr><td colspan="4">CreateReminder()</td></tr><tr><td colspan="4">DeleteReminder()</td></tr><tr><td colspan="4">UpdateReminder()</td></tr><tr><td colspan="4">GetReminderByID()</td></tr></tbody></table>

### 4.2.2.2. Interface Layer.

A continuación se mostrarán interfaces utilizadas por el Backend de la aplicación, que representan el core del negocio con respecto a este Bounded Context.

+ **IReminderController:** Interfaz del repositorio de los recordatorios.

<table><thead><tr><th>Nombre</th><th colspan="3">IReminderController</th></tr></thead><tbody><tr><td>Descripción</td><td colspan="3">permite la conexión con la base de datos</td></tr><tr><td colspan="4">Métodos</td></tr><tr><td colspan="4">GetAllReminder()</td></tr><tr><td colspan="4">GetByDateReminder()</td></tr><tr><td colspan="4">CreateReminder()</td></tr><tr><td colspan="4">DeleteReminder()</td></tr><tr><td colspan="4">UpdateReminder()</td></tr><tr><td colspan="4">GetReminderByID()</td></tr></tbody></table>

### 4.2.2.3. Application Layer.

En esta sección presentamos commandHandlers y EventHandlers para hacer control de eventos y comandos para realizar a las implementaciones de las interfaces del subdominio de los reminders.

+ **CreateReminderCommandHandler**: Controla la creación y configuración de recordatorios.
+ **ReminderCreatedEventHandler**: Se encarga del evento de creación de recordatorios.

### 4.2.2.4. Infrastructure Layer.

A continuación se les presentan las clases encargadas de conectar el Frontend con los servicios del repositorio del Backend:
+ **ReminderRepository:** Intercambio de datos entre la entidad Offer con la base de datos.

### 4.2.2.6. Bounded Context Software Architecture Component Level Diagrams.

<img src="Assets\Reminders_ContextDiagram.png" style="width: 50%; padding-top: 12px;padding-bottom: 12px;">

### 4.2.2.7. Bounded Context Software Architecture Code Level Diagrams.

#### 4.2.2.7.1. Bounded Context Domain Layer Class Diagrams.

<img src="Assets\Reminder_ClassDiagram.png" style="width: 50%; padding-top: 12px;padding-bottom: 12px;">

#### 4.2.2.7.2. Bounded Context Database Design Diagram.

<img src="Assets\Reminder_DatabaseDiagram.png" style="width: 50%; padding-top: 12px;padding-bottom: 12px;">

## 4.2.3. Bounded Context: Device Purchase

<table>
<thead>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</th>
    <th colspan="3">&nbsp;&nbsp;&nbsp;<br>DevicePurchase&nbsp;&nbsp;&nbsp;</th>
    <th></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Descripción&nbsp;&nbsp;&nbsp;</td>
    <td colspan="3">&nbsp;&nbsp;&nbsp;<br>Representa la compra de la pulsera&nbsp;&nbsp;&nbsp;</td>
    <td></td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>Atributos&nbsp;&nbsp;&nbsp;</td>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>Relaciones&nbsp;&nbsp;&nbsp;</td>
    <td rowspan="2">&nbsp;&nbsp;&nbsp;<br> <br>&nbsp;&nbsp;&nbsp;<br>Métodos&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Tipo de Dato&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Tipo&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Clases/Enums&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>devicePurchaseId&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>DevicePurchaseId&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Composición&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>DevicePurchaseId&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>purchase()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>userId&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>UserId&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Composición&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>UserId&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>cancelPurchase ()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>title&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>string&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Composición&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Catalog&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>track()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>description&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>String&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Composición&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>History&nbsp;&nbsp;&nbsp;</td>
    <td></td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>date&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Date&nbsp;&nbsp;&nbsp;</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>catalog&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Catalog&nbsp;&nbsp;&nbsp;</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>history&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>History&nbsp;&nbsp;&nbsp;</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</tbody>
</table>

<table>
<thead>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Catalog&nbsp;&nbsp;&nbsp;</th>
    <th colspan="2" rowspan="2"></th>
  </tr>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Descripción&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Representar el catálogo de pulseras&nbsp;&nbsp;&nbsp;</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>Atributos&nbsp;&nbsp;&nbsp;</td>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>Relaciones&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Tipo de Dato&nbsp;&nbsp;&nbsp;</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>bracelet&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Bracelet&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Composición &nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Bracelet&nbsp;&nbsp;&nbsp;</td>
  </tr>
</tbody>
</table>

<table>
<thead>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Bracelet&nbsp;&nbsp;&nbsp;</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Descripción&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Representar una pulsera&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>Atributos&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Tipo de Dato&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>description&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>string&nbsp;&nbsp;&nbsp;</td>
  </tr>
</tbody>
</table>

<table>
<thead>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>History&nbsp;&nbsp;&nbsp;</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Descripción&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Representar el historial de compras&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>Valores&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>LessThanTwoPurchase&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>MoreThanTwoPurchase&nbsp;&nbsp;&nbsp;</td>
  </tr>
</tbody>
</table>

<table>
<thead>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>UserId&nbsp;&nbsp;&nbsp;</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Descripción&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Representa el identificador del usuario&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>Atributos&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Tipo de Dato&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>userId&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>long&nbsp;&nbsp;&nbsp;</td>
  </tr>
</tbody>
</table>

<table>
<thead>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>DevicePurchaseId&nbsp;&nbsp;&nbsp;</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Descripción&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Representar el identificador&nbsp;&nbsp;&nbsp;de la compra&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>Atributos&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Tipo de Dato&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>devicePurchaseId&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>long&nbsp;&nbsp;&nbsp;</td>
  </tr>
</tbody>
</table>

### 4.2.3.1. Domain Layer.

Se identificó que la única clase que es parte del core del negocio es la clase Device Purchase, la cual es la compra de una pulsera. Las reglas de negocio, es que el cuidador del adulto mayor puede solicitar una o mas pulseras dependiendo de su situación. 

**Entities:**
+ DevicePurchase(**Agregate**): Representa la compra de la pulsera

**Value Objects:**
+ UserId (**Agregate**): Representa el identificador del usuario
+ DevicePurchaseId (**Agregate**): Representar el identificador de la compra
+ Bracelet: Representar una pulsera
+ Catalog (**Agregate**): Representar el catálogo de pulseras

**Enums:**
+ History (Agregate): Representar el historial de compras

**Factories:**
+ DevicePurchaseFactory: ayuda a la creación de una orden de compra

**Interfaces:**
+ IDevicePurchaserRepository: interfaz de la clase DevicePurchaseRepository, ayuda a mantener un bajo acoplamiento

<table>
<thead>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>IDevicePurchaseRepository&nbsp;&nbsp;&nbsp;</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Descripción&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>permite la conexión con la base de datos&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>Métodos&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>findAll()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>findById()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>findByUserId()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>create()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>update()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>delete()&nbsp;&nbsp;&nbsp;</td>
  </tr>
</tbody>
</table>

+ IDevicePurchaseServices: interfaz de la clase DevicePurchaseService, ayuda a mantener un bajo acoplamiento.

<table>
<thead>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>IDevicePurchaseService&nbsp;&nbsp;&nbsp;</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Descripción&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>Declara las funciones que contiene las reglas de&nbsp;&nbsp;&nbsp;negocio&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>Métodos&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>getAll()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>geById()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>getByUserId()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>create()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>delete()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>purchase()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>cancelPurchase ()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>track()&nbsp;&nbsp;&nbsp;</td>
  </tr>
</tbody>
</table>

### 4.2.3.2. Interface Layer.

En esta sección se presentan las interfaces serán consumidas por la aplicación cliente para realizar cambios relacionados a las ofertas de empleos.

+ IDevicePurchaseController:
Define las funciones que reciben las solicitudes relacionadas a la administración de órdenes.

<table>
<thead>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Nombre&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>IDevicePurchaseController&nbsp;&nbsp;&nbsp;</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>Descripción&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>define las funciones que reciben las solicitudes&nbsp;&nbsp;&nbsp;relacionadas a la administración de órdenes&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>Métodos&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>getAll()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>geById()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>getByUserId()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>create()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>delete()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>purchase()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>cancelPurchase ()&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>track()&nbsp;&nbsp;&nbsp;</td>
  </tr>
</tbody>
</table>

### 4.2.3.3. Application Layer.

En esta sección presentamos los commandHandlers y EventHandlers encargados de manejar los comandos y eventos respectivos tras las solicitudes realizadas a las implementaciones de las interfaces del ítem anterior.

+ CreateDevicePurchaseCommandHandler: Maneja el comando de crear ordenes
+ DevicePurchaseCreatedEventHandler: Maneja el evento de orden creada

### 4.2.3.4. Infrastructure Layer.

En esta sección presentamos las clases que se encargan de conectar con servicios externos:

+ DevicePurchaseRepository: establece la conexión del componente DevicePurchase con la base de datos, permitiendo el intercambio de datos entre ambas partes
+ DevicePurchaseMailService: establece la conexión con el sistema de emails notifications.


### 4.2.3.6. Bounded Context Software Architecture Component Level Diagrams.

A continuación, presentamos el component level diagram considerado para el DevicePurchaseContext.

![](Assets/c4_alfredo.png)

### 4.2.3.7. Bounded Context Software Architecture Code Level Diagrams.

#### 4.2.3.7.1. Bounded Context Domain Layer Class Diagrams.

A continuación, presentamos el diagrama de clases del dominio considerado para el DevicePurchaseContext.

![](Assets/clases_alfredo.png)

#### 4.2.3.7.2. Bounded Context Database Design Diagram.



A continuación, presentamos el diagrama de base de datos considerado para el DevicePurchaseContext.

![](Assets/clases_alfredo_2.png)




4\.2.4. Bounded Context: Elderly Profile

<img src="Assets\boundedcontext1.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

(Aspose.Words.2227f55b-24bb-45df-ae5a-5d64f316230e.001.png)


<img src="Assets\boundedcontext2.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>



<img src="Assets\boundedcontext3.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

<img src="Assets\boundedcontext4.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>


<img src="Assets\boundedcontext5.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

<img src="Assets\boundedcontext6.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>



4\.2.4.1. Domain Layer. 

Se identificó que una clase que es parte del core del negocio es la clase Elderly Adult, la cual es la cual es la persona que es cuidada por el usuario. Las reglas de negocio, es que  el usuario registra a su cuidado al Elderly Adult donde  registra su información a excepción de la fecha de inicio que se autogenera con la fecha en la que se agrega.

**Entidades:**

- ElderlyAdult **(Agregate)**: Es la representación de un adulto mayor que necesita cuidados.

**Value Objects:**

- ElderlyAdultId **(Agregate)**: Es la representación del adulto mayor que necesita cuidados.
- UserId **(Agregate)**: Es la representación del identificador del cuidador del ElderlyAdult.
- Time: Es la representación del tiempo que cuidara al ElderlyAdult.

**Enums:**

- Availability **(Agregate)**: Es la representación de la disposición que tiene el usuario con el Elderly Adult
- Experience: Es la representación de la experiencia mínima necesaria para aplicar al cuidado del ElderlyAdult
- Userinfo: Es la representación de la información del usuario cuidador.

**Interfaces:**

- ElderlyAdultRepository: interfaz de la clase ElderlyAdultRepository, ayuda a mantener un bajo acoplamiento

<img src="Assets\boundedcontext7.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>


- IElderlyAdultServices: interfaz de la clase IElderlyAdultService, ayuda a mantener un bajo acoplamiento.

<img src="Assets\boundedcontext8.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

<img src="Assets\boundedcontext9.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

4\.2.4.2. Interface Layer. 

En esta sección se presentan las interfaces serán consumidas por la aplicación cliente para realizar cambios relacionados al estado de salud del ElderlyAdult.

- **IElderlyAdultController:**

 <img src="Assets\boundedcontext10.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>
Define las funciones que reciben las solicitudes relacionadas al cuidado de ElderlyAdult.
**

**


4\.2.4.3. Application Layer.

En esta sección presentamos los commandHandlers y EventHandlers encargados de manejar los comandos y eventos respectivos tras las solicitudes realizadas a las implementaciones de las interfaces del ítem anterior.

- **RegisterElderAdultCommandHandler**: Maneja el comando de registrar Adultos mayores
- **ElderAdultRegisteredEventHandler**: Maneja el evento de registro de un Adulto mayor

4\.2.4.4. Infrastructure Layer. 

En esta sección presentamos las clases que se encargan de conectar con servicios externos:

- **ElderlyAdultRegisterRepository**: establece la conexión del componente Offer con la base de datos, permitiendo el intercambio de datos entre ambas partes
- **ElderlyAdultRegisterMailService**: establece la conexión con el sistema de emails notifications.

4\.2.4.6. Bounded Context Software Architecture Component Level Diagrams. 

A continuación, presentamos el component level diagram considerado para el ElderlyAdultOfferContext.

<img src="Assets\boundedcontext11.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>


4\.2.4.7. Bounded Context Software Architecture Code Level Diagrams. 

4\.3.4.7.1. Bounded Context Domain Layer Class Diagrams.

` `A continuación, presentamos el diagrama de clases del dominio considerado para el ElderlyAdultContext.

<img src="Assets\boundedcontext12.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>

4\.3.4.7.2. Bounded Context Database Design Diagram. 

A continuación, presentamos el diagrama de base de datos considerado para el ElderlyAdultRegisterContext.

<img src="Assets\boundedcontext13.png" style="width: 75%; padding-top: 12px;padding-bottom: 12px;"><br>


