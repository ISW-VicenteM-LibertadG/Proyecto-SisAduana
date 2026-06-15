# Coevaluación Grupal – Evaluación Formativa N°3

Hicimos la coevaluación grupal aplicando la pauta correspondiente a la **Evaluación Formativa N°3**.

## Grupo evaluado

- Javier Vásquez
- Vicente Quilaleo
- Carlos Salfate

## Aspectos destacados

El prototipo presenta una interfaz limpia, minimalista y de fácil navegación, con una paleta de colores coherente que se mantiene consistente en todas las pantallas.

La pantalla de **Cruces fronterizos (Historial)** está bien estructurada, incorporando:

- Filtros por estado (**Todos / Aprobados / Rechazados**).
- Tipos de control diferenciados (**Persona, Menor de edad y Vehículo**).
- Números de comprobante generados automáticamente.

Estos elementos reflejan una buena comprensión de los procesos aduaneros.

El **Panel de Control** presenta indicadores operativos claros, tales como:

- Cruces registrados.
- Cruces aprobados.
- Cruces rechazados.
- Tiempo promedio de atención.

Además, incorpora un desglose por entidad validadora (**PDI, SAG, Aduana y Documental**) con estados diferenciados (**OK, Alerta y Rechazo**), demostrando un buen nivel de detalle funcional.

Por otra parte, el módulo de **Administración de Cuentas** integra en una misma pantalla el formulario de creación y la tabla de usuarios, simplificando la experiencia del administrador.

## Oportunidades de mejora

- El sistema no diferencia la experiencia según el rol del usuario autenticado. Al ingresar como **Administrador** o **Funcionario** se accede a las mismas pantallas y funcionalidades, lo que no refleja el control de acceso por roles definido en los requisitos. Sería recomendable mostrar menús o módulos distintos según el perfil del usuario.

- El formulario de **Nuevo Cruce** es bastante simplificado, ya que reúne en un solo campo los productos SAG con un texto de ejemplo ("carne/fruta = prohibido"). Idealmente, esta información debería estar en una sección independiente con validaciones explícitas. No obstante, esto resulta comprensible considerando que se trata de un prototipo académico desarrollado con fines principalmente pedagógicos.

- El nombre del sistema aparece como **SCAF** dentro del prototipo, mientras que en la documentación del proyecto se utiliza una denominación distinta. Se recomienda unificar la identidad del sistema para la presentación final.

## Comentarios constructivos

El prototipo demuestra un trabajo sólido en cuanto a estructura y navegación general, presentando pantallas que representan adecuadamente el flujo operativo de un paso fronterizo.

El principal aspecto a reforzar antes de la entrega corresponde a la diferenciación visual y funcional entre los distintos roles de usuario, ya que constituye uno de los criterios evaluados en la rúbrica. Con este ajuste, el prototipo alcanzaría un nivel de desarrollo muy completo.
