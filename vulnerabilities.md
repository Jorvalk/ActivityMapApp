# Reporte de vulnerabilidades

## Resumen
-Total de vulnerabilidades encontradas: 10
-Critico: 0
-Alto: 3
-Medio: 5
-Bajo: 2

## Detalles

### Solicitud firmada
- Severidad: Info
- Descripción:La solicitud está firmada con un certificado de firma de código.

### La aplicación registra información. Nunca se debe registrar información sensible.
- Severidad: Info
- Descripción: CWE: CWE-532: Inserción de información confidencial en un archivo de registro OWASP MASVS: MSTG-STORAGE-3

### Solicitud firmada con certificado de depuración
- Severidad: Alto
- Descripción: Aplicación firmada con un certificado de depuración. La aplicación de producción no debe enviarse con un certificado de depuración.

### La aplicación se puede instalar en una versión actualizada y vulnerable de Android. Android 7.0, [minSdk=24]
- Severidad: Alto
- Descripción: Esta aplicación se puede instalar en una versión anterior de Android que tenga múltiples vulnerabilidades sin corregir. 
  Estos dispositivos no recibirán actualizaciones de seguridad razonables de Google. Admite una versión de Android => 10, API 29 para recibir
  actualizaciones de seguridad razonables.

### Depuración habilitada para la aplicación [android:debuggable=true]
- Severidad: Alto
- Descripción: Se habilitó la depuración en la aplicación, lo que facilita que los ingenieros inversos conecten un depurador a ella.
  Esto permite volcar un seguimiento de pila y acceder a clases auxiliares de depuración.

### Se pueden realizar copias de seguridad de los datos de la aplicación. Falta el indicador [android:allowBackup].
- Severidad: Medio
- Descripción: La bandera [android:allowBackup] debe estar establecida en falso. De manera predeterminada, está establecida en verdadero y permite que cualquier persona haga una copia de seguridad de los
  datos de su aplicación a través de adb. Permite a los usuarios que han habilitado la depuración USB copiar los datos de la aplicación fuera del dispositivo.

### La actividad (androidx.test.core.app.InstrumentationActivityInvoker$BootstrapActivity) no está protegida. [android:exported=true]
- Severidad: Medio
- Descripción: Se descubre que una actividad se comparte con otras aplicaciones en el dispositivo, por lo que queda accesible para cualquier otra aplicación en el dispositivo.

### La actividad (androidx.test.core.app.InstrumentationActivityInvoker$EmptyActivity) no está protegida. [android:exported=true]
- Severidad: Medio
- Descripción: Se descubre que una actividad se comparte con otras aplicaciones en el dispositivo, por lo que queda accesible a cualquier otra aplicación en el dispositivo.

### La aplicación utiliza un generador de números aleatorios inseguro.
- Severidad: Medio
- Descripción: CWE: CWE-330: Uso de valores insuficientemente aleatorios OWASP Top 10: M5: Criptografía insuficiente OWASP MASVS: MSTG-CRYPTO-6

### La aplicación crea un archivo temporal. Nunca se debe escribir información sensible en un archivo temporal.
- Severidad: Medio
- Descripción: CWE: CWE-276: Permisos predeterminados incorrectos Top 10 de OWASP: M2: Almacenamiento de datos inseguro OWASP MASVS: MSTG-STORAGE-2