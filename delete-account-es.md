# Eliminar tu cuenta de WeRock

**Ultima actualizacion:** 7 de mayo de 2026
**Version:** 1.0 (M0)

> **Mirror publico:** este archivo es la fuente de verdad. La copia
> publicada en `https://legal.werockapp.com/delete-account-es` se actualiza
> desde el repo `werock-legal/werock-legal` (GitHub Pages + custom domain
> via Cloudflare DNS). Cualquier cambio aqui debe propagarse al mirror.

WeRock (`https://werockapp.com`) respeta el **derecho de supresion**
reconocido en el **art. 17 del Reglamento (UE) 2016/679** (RGPD) y en la
**Ley Organica 3/2018 de Proteccion de Datos Personales y garantia de
los derechos digitales (LOPDGDD)**. Esta pagina explica como puedes
solicitar la eliminacion de tu cuenta de WeRock y de todos los datos
personales asociados.

---

## 1. Que se elimina cuando borras tu cuenta

Cuando confirmas el borrado, ejecutamos un proceso automatico
(`deleteUserAccountV1`) que purga **todos** los siguientes datos en menos
de 60 segundos, sin retener copias internas mas alla del registro
auditable de la propia accion de borrado (que tambien se elimina a los
30 dias):

### 1.1 Datos de identidad

- Cuenta de Firebase Authentication (email, hash de contrasena, UID).
- Si te registraste con Google: revocacion del token OAuth.
- Subdocumento privado `users/{uid}/private/profile` con email, telefono,
  fecha de nacimiento, direccion de envio, datos fiscales (CIF/NIF,
  domicilio empresarial), Stripe Connect account ID y metadatos de
  pagos Pro.

### 1.2 Contenido publico que has creado

- Spots que has publicado.
- Eventos que has organizado.
- Anuncios del marketplace.
- Posts del feed comunidad.
- Comentarios y kudos.
- Vídeos de tricks subidos a TrickTree.
- Rutas guardadas.

### 1.3 Datos privados de uso

- Sesiones GPS de entrenamiento (`tracked_sessions`).
- Perfil de gear y recomendaciones IA personalizadas.
- Lista de deseos de equipamiento.
- Notificaciones internas, presupuesto de IA y consumo historico.
- Reseñas de productos.

### 1.4 Datos en almacenamiento de archivos

- Avatares y fotos de perfil (`Storage: avatars/{uid}.*`).
- Vídeos de tricks (`Storage: users/{uid}/tricks/*`).
- Imagenes de eventos que has organizado.
- Imagenes de articulos del marketplace que has publicado.
- Imagenes de posts y de spots.

### 1.5 Datos en bases auxiliares

- Estado de presencia en tiempo real (Realtime Database).
- Referencias huerfanas (kudos en posts ajenos, registros en eventos
  ajenos, comentarios en posts ajenos, reportes que has emitido).

### 1.6 Datos derivados / agregados

Algunos datos agregados (estadisticas anonimizadas de uso, contadores
publicos de la app) **no contienen tu identidad** pero si pueden haber
contribuido a calculos historicos (ej. "X% de los riders han probado el
truco Y"). Estos calculos no se recalculan retroactivamente, pero al no
contener tu uid son anonimos y no constituyen un tratamiento de datos
personales tras tu borrado.

---

## 2. Que NO se elimina (excepciones legales)

Por **obligaciones legales** debemos retener cierta informacion incluso
despues de tu borrado. Esta retencion esta limitada al minimo legal y
los datos no se usan para perfilarte ni para comunicaciones comerciales.

| Categoria | Plazo de retencion | Base legal |
| --- | --- | --- |
| Facturas / tickets emitidos por compras en marketplace o eventos | 6 anos | Ley General Tributaria 58/2003 (obligacion de conservacion contable y fiscal) |
| Logs de auditoria de seguridad (intentos fallidos de login, cambios de rol economico, autorizaciones App Check denegadas) | 1 ano | Interes legitimo (art. 6.1.f RGPD) — proteccion del servicio frente a abuso |
| Logs de operaciones de pago Stripe (ID de transaccion, importe, fecha, contraparte) | 6 anos | Reglamento PSD2 + obligaciones AML / Ley General Tributaria |

Estos datos retenidos **no se asocian a tu identidad personal** mas alla
del minimo necesario para cumplir la obligacion (en el caso de facturas,
tu nombre + CIF/NIF si los proporcionaste; en el caso de logs, tu uid
hash con un mes de retroceso). Tras el plazo legal se eliminan
automaticamente.

---

## 3. Como solicitar el borrado

### 3.1 Si tienes la app instalada (recomendado)

Es la forma mas rapida y la unica que permite la eliminacion totalmente
automatica:

1. Abre WeRock en tu telefono.
2. Inicia sesion con tu cuenta.
3. Ve a **"Mi Zona"** (icono inferior derecha).
4. Toca el icono de engranaje en la esquina superior derecha (Cuenta).
5. Desplazate hasta el final del panel.
6. Pulsa **"Eliminar cuenta"**.
7. Confirma escribiendo `ELIMINAR` en mayusculas en el cuadro de texto.

El proceso ejecuta `deleteUserAccountV1` y devuelve confirmacion en
menos de 60 segundos. Recibiras un email final de confirmacion en la
direccion que tenias registrada. La cuenta queda eliminada y no podras
recuperar el contenido. Si volvieras a registrarte con el mismo email
sera una cuenta nueva sin historial.

### 3.2 Si NO tienes la app instalada

Si has desinstalado la app pero tu cuenta sigue activa, puedes
solicitar el borrado por correo electronico siguiendo este proceso:

1. Envia un email a **`privacy@werockapp.com`** desde **la direccion
   de email asociada a tu cuenta WeRock**. Esto es necesario para
   verificar tu identidad sin pedirte mas datos personales.
2. Asunto: `Solicitud de borrado de cuenta - art. 17 RGPD`.
3. Cuerpo del email (puedes copiarlo y pegarlo):

   > Solicito el borrado completo de mi cuenta WeRock asociada a este
   > email, en ejercicio del derecho de supresion reconocido en el
   > articulo 17 del Reglamento (UE) 2016/679 (RGPD).
   >
   > Confirmo que entiendo que el borrado es irreversible y que no
   > podre recuperar el contenido publicado, las sesiones GPS, los
   > vídeos de tricks ni los pedidos del marketplace asociados a esta
   > cuenta.
   >
   > [Tu nombre publico en WeRock, opcional pero ayuda al match]

4. Procesaremos la peticion en un plazo maximo de **30 dias naturales**
   (plazo legal RGPD), tipicamente en menos de 72 horas.
5. Recibiras un email final de confirmacion una vez completado el
   borrado en sistemas.

### 3.3 Si has perdido acceso al email registrado

Si ya no puedes acceder al email con el que te registraste:

1. Envia tu solicitud a `privacy@werockapp.com` desde tu email actual.
2. Adjunta cualquier informacion que nos permita verificar tu identidad
   sin recurrir a documentos personales (por ejemplo, fecha aproximada
   del registro, ciudad, dispositivo desde el que te registraste,
   nombre publico que usabas en la app).
3. Si la verificacion no es concluyente, te pediremos foto de un
   documento de identidad. **Borraremos esa imagen en cuanto
   verifiquemos** y nunca la usaremos para ningun otro fin.

---

## 4. Plazos y confirmacion

| Etapa | Plazo |
| --- | --- |
| Recepcion de la solicitud | Inmediato |
| Borrado tecnico en sistemas (CF `deleteUserAccountV1`) | < 60 segundos desde la confirmacion |
| Email de confirmacion al rider | Mismo dia (tipicamente < 5 minutos) |
| Borrado en bases analiticas / Crashlytics / backups | < 30 dias (rotacion natural de logs y backups; periodo legal RGPD) |
| Plazo legal maximo RGPD | 30 dias naturales desde la solicitud |

---

## 5. Tus derechos relacionados

El borrado total no es la unica via para controlar tus datos. Tambien
puedes ejercer:

- **Acceso (art. 15 RGPD):** solicitar copia de tus datos personales
  procesados en `privacy@werockapp.com`.
- **Rectificacion (art. 16 RGPD):** corregir datos inexactos desde
  Mi Zona o por email.
- **Limitacion de tratamiento (art. 18 RGPD):** pedir que pausemos el
  uso de tus datos sin borrarlos.
- **Portabilidad (art. 20 RGPD):** descargar tus datos en formato
  estructurado JSON (te lo enviamos en un plazo maximo de 30 dias).
- **Oposicion (art. 21 RGPD):** oponerte al tratamiento basado en
  interes legitimo.
- **Eliminacion parcial sin cerrar cuenta:** ver
  `https://legal.werockapp.com/delete-data-es`.

---

## 6. Reclamaciones

Si consideras que no hemos atendido correctamente tu solicitud, puedes
reclamar ante la **Agencia Espanola de Proteccion de Datos (AEPD)**:

- Web: `https://www.aepd.es`
- Sede electronica: `https://sedeagpd.gob.es`
- Direccion postal: C/ Jorge Juan, 6, 28001 Madrid

---

## 7. Contacto

Para cualquier duda relacionada con la eliminacion de tu cuenta o el
ejercicio de tus derechos RGPD:

- **Email privacidad:** `privacy@werockapp.com`
- **Email soporte general:** `support@werockapp.com`
- **Politica de Privacidad completa:** `https://legal.werockapp.com/privacy-es`
- **Terminos del Servicio:** `https://legal.werockapp.com/terms-es`

---

## Historial

| Fecha | Version | Cambio | Operador |
| --- | --- | --- | --- |
| 7 may 2026 | 1.0 | Creacion del documento como respuesta al campo "Account deletion URL" obligatorio del formulario Data Safety de Google Play Console (Sprint C). | Agente |
