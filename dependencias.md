# Dependencias a Utilizar en `pubspec.yaml`

## Great Smile Clinic 🦷

A continuación se presentan las dependencias que serán utilizadas en el proyecto **Great Smile Clinic**, numeradas y organizadas de acuerdo con las necesidades del sistema.

---

# 1. flutter

Permite utilizar el SDK principal de Flutter para el desarrollo multiplataforma.

```yaml
flutter:
  sdk: flutter
```

---

# 2. cupertino_icons

Proporciona íconos estilo iOS para mejorar la interfaz gráfica.

```yaml
cupertino_icons: ^1.0.6
```

---

# 3. firebase_core

Inicializa Firebase dentro de la aplicación Flutter.

```yaml
firebase_core: ^3.0.0
```

---

# 4. firebase_auth

Gestiona la autenticación mediante correo electrónico y contraseña.

```yaml
firebase_auth: ^5.0.0
```

---

# 5. cloud_firestore

Permite conectar y administrar la base de datos en la nube Firestore.

```yaml
cloud_firestore: ^5.0.0
```

---

# 6. firebase_storage

Se utiliza para almacenar imágenes, radiografías y archivos clínicos.

```yaml
firebase_storage: ^12.0.0
```

---

# 7. provider

Manejo de estado de la aplicación mediante Provider.

```yaml
provider: ^6.1.2
```

---

# 8. go_router

Administra la navegación y protección de rutas dentro de la aplicación.

```yaml
go_router: ^14.0.0
```

---

# 9. google_fonts

Permite utilizar tipografías personalizadas como Montserrat y Open Sans.

```yaml
google_fonts: ^6.2.1
```

---

# 10. flutter_svg

Permite usar imágenes SVG en la interfaz gráfica.

```yaml
flutter_svg: ^2.0.10
```

---

# 11. fl_chart

Se utilizará para gráficas y reportes administrativos.

```yaml
fl_chart: ^0.68.0
```

---

# 12. intl

Permite formatear fechas, horas y monedas.

```yaml
intl: ^0.19.0
```

---

# 13. uuid

Genera identificadores únicos para registros del sistema.

```yaml
uuid: ^4.4.0
```

---

# 14. shared_preferences

Permite guardar datos locales como sesiones y configuraciones.

```yaml
shared_preferences: ^2.2.3
```

---

# 15. pdf

Genera facturas y reportes en formato PDF.

```yaml
pdf: ^3.10.8
```

---

# 16. printing

Permite imprimir y visualizar documentos PDF.

```yaml
printing: ^5.12.0
```

---

# 17. image_picker

Permite seleccionar imágenes desde cámara o galería.

```yaml
image_picker: ^1.1.2
```

---

# 18. connectivity_plus

Detecta el estado de conexión a internet.

```yaml
connectivity_plus: ^6.0.3
```

---

# 19. flutter_launcher_icons

Permite configurar el ícono oficial de la aplicación.

```yaml
flutter_launcher_icons: ^0.13.1
```

---

# 20. flutter_native_splash

Genera la pantalla de carga inicial de la aplicación.

```yaml
flutter_native_splash: ^2.4.0
```

---

# Ejemplo Completo de `pubspec.yaml`

```yaml
dependencies:
  flutter:
    sdk: flutter

  cupertino_icons: ^1.0.6

  firebase_core: ^3.0.0
  firebase_auth: ^5.0.0
  cloud_firestore: ^5.0.0
  firebase_storage: ^12.0.0

  provider: ^6.1.2

  go_router: ^14.0.0

  google_fonts: ^6.2.1
  flutter_svg: ^2.0.10
  fl_chart: ^0.68.0

  intl: ^0.19.0
  uuid: ^4.4.0

  shared_preferences: ^2.2.3

  pdf: ^3.10.8
  printing: ^5.12.0

  image_picker: ^1.1.2

  connectivity_plus: ^6.0.3

  flutter_launcher_icons: ^0.13.1
  flutter_native_splash: ^2.4.0
```
