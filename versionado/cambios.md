# Historial de Versiones e Iteraciones

Este documento registra las principales iteraciones realizadas durante el desarrollo del prototipo **SisAduana**, describiendo las funcionalidades incorporadas y las mejoras implementadas en cada etapa del proyecto.

Su objetivo es mantener la trazabilidad de la evolución del prototipo y documentar las decisiones de diseño adoptadas durante su desarrollo.

---

## Iteración 1 — Diseño inicial del prototipo completo

Se construyó la estructura base de SisAduana con todas las pantallas principales: **Login**, **Dashboard por perfil (Funcionario, Supervisor y Administrador)**, **Registro de Pasajeros**, **Registro de Vehículos**, **Declaración Jurada SAG**, **Historial de Operaciones**, **Reportes Estadísticos**, **Gestión de Usuarios** y **Logs del Sistema**.

Se estableció la identidad visual institucional (azul #2E4B8A y blanco), navegación lateral fija y flujos navegables entre pantallas.

---

## Iteración 2 — Incorporación del flujo de menores de edad en Registro de Pasajeros

Se modificó la pantalla de Registro de Pasajeros para incorporar la validación de autorización notarial dentro del mismo formulario, sin pantalla separada.

Al detectar que el pasajero es menor de 18 años, el sistema despliega automáticamente la sección de validación con los datos de los adultos responsables y el estado de cada autorización notarial consultada al Registro Civil. El botón de registro se habilita únicamente cuando ambos permisos están aprobados.

---

## Iteración 3 — Campo de fecha de nacimiento como solo lectura

Se deshabilitó la edición manual del campo de fecha de nacimiento. La fecha es generada automáticamente por el sistema al validar el documento.

**Justificación:** Un funcionario no debe poder alterar un dato que proviene de una validación externa con el Registro Civil.

---

## Iteración 4 — Mejoras al módulo de Registro de Vehículos

Se incorporó un selector de **Ingreso/Salida** al inicio del formulario. Cuando se selecciona **Ingreso**, el sistema calcula automáticamente la fecha de vencimiento del permiso (180 días desde la fecha actual) y la muestra antes de confirmar el registro.

Al registrar, se genera un comprobante oficial con folio único, datos del vehículo, fecha y hora de operación, y el bloque destacado con la fecha de vencimiento. Se añadió botón de impresión y opción de nuevo registro.

**Justificación:** Esta mejora permite representar de forma más realista el proceso de admisión temporal de vehículos, automatizando el cálculo del plazo legal y facilitando la emisión de un comprobante para el usuario y el funcionario.

---

## Iteración 5 — Bloqueo de cuenta e indicadores de sesión activa

Se implementó un sistema de bloqueo progresivo en el Login: tras tres intentos fallidos se activa una pantalla de bloqueo con cuenta regresiva de 30 segundos y barra de progreso. Durante los intentos previos, un indicador visual muestra los intentos restantes.

En el layout principal se añadió una barra superior con punto verde pulsante, nombre y rol del usuario, reloj en tiempo real y duración de sesión. Se incorporó aviso de inactividad a los 25 minutos y cierre automático de sesión a los 30 minutos.

**Justificación:** Estas funcionalidades fortalecen la seguridad del sistema y mejoran la experiencia de usuario, simulando mecanismos habituales de autenticación y control de sesiones utilizados en aplicaciones institucionales.

---

## Iteración 6 — Pantallas de carga para operaciones con sistemas externos

Se incorporaron indicadores de progreso en los flujos que simulan consultas a sistemas externos (PDI, SAG y Registro Civil).

Se utilizaron dos patrones diferenciados: uno con pasos secuenciales para validaciones críticas (Login, Declaración SAG y Validación de Pasajeros) y una barra de carga para cargas de datos tabulares (Historial, Reportes, Gestión de Usuarios y Logs).

**Justificación:** Dar mayor realismo al prototipo y representar fielmente los requisitos no funcionales establecidos para tiempos de respuesta y experiencia de usuario.
