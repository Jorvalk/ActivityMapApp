# Consejos de seguridad

### Validación de Entrada
-Descripción: Se implementó la validación y sanitización de los datos de entrada del usuario en todos los formularios de la aplicación.
-Resultados: Se establecieron listas blancas para los campos de texto, asegurando que solo se acepten caracteres válidos y que los valores estén dentro de los rangos esperados.
-Acciones Recomendadas: Continuar revisando y ajustando las validaciones según sea necesario para abordar cualquier nuevo tipo de entrada que pueda surgir.

### Minimización de Permisos
-Descripción: Se revisaron y ajustaron los permisos solicitados por la aplicación, eliminando aquellos que no son necesarios para su funcionalidad.
-Resultados: Se redujo el número total de permisos solicitados, lo que disminuye la superficie de ataque y aumenta la confianza del usuario en la aplicación.
-Acciones Recomendadas: Realizar una revisión periódica de los permisos en futuras versiones de la aplicación para asegurar que se mantenga esta minimización.

### Uso de Bibliotecas y Dependencias Seguras
-Descripción: Se estableció un proceso regular para verificar y actualizar las bibliotecas y dependencias utilizadas en la aplicación.
-Resultados: Se identificaron y actualizaron bibliotecas a sus versiones más recientes, corrigiendo vulnerabilidades conocidas.
-Acciones Recomendadas: Implementar herramientas de gestión de dependencias para facilitar el seguimiento de actualizaciones y vulnerabilidades.