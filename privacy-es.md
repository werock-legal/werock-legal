# Politica de Privacidad — WeRock

**Ultima actualizacion:** 6 de mayo de 2026
**Version:** 1.0 (M0)

WeRock (`https://werock.app`) es una plataforma social y operativa para deportes de accion (patinaje, skate, ciclismo, running) operada por **WeRock Platform** (en adelante, "WeRock", "nosotros"). Esta politica explica que datos personales tratamos de los **riders** registrados, con que finalidad, y como puedes ejercer tus derechos.

Cumplimos con el **Reglamento (UE) 2016/679** (RGPD) y la **Ley Organica 3/2018 de Proteccion de Datos Personales y garantia de los derechos digitales (LOPDGDD)**.

---

## 1. Responsable del tratamiento

| Concepto | Detalle |
| --- | --- |
| Responsable | WeRock Platform (forma juridica final por confirmar antes de Sprint B) |
| CIF / NIF | Por publicar antes del lanzamiento publico |
| Domicilio fiscal | Por publicar antes del lanzamiento publico |
| Contacto privacidad | `privacy@werock.app` |
| Delegado de proteccion de datos (DPO) | No aplica todavia (no superamos los umbrales de la LOPDGDD para nombrar DPO obligatorio en M0) |

Esta seccion se actualizara antes del primer lanzamiento publico (Sprint C) con los datos legales finales.

## 2. Datos personales que tratamos

### 2.1 Datos de cuenta (obligatorios)

| Dato | Origen | Finalidad |
| --- | --- | --- |
| Email | Tu lo introduces en el wizard de registro | Identificarte, enviarte verificacion email, comunicaciones operativas (recuperacion password, cambios materiales en politica) |
| Hash de contrasena | Generado por Firebase Authentication. Nunca recibimos la contrasena en claro | Permitirte iniciar sesion |
| Fecha de nacimiento | Tu la introduces en el wizard | Cumplimiento legal (mayoria de edad para ciertas acciones, eventos +18, contenido adulto), recordatorios de cumpleanos opcionales |
| Disciplina inicial | Tu la seleccionas en el wizard | Personalizar el feed, recomendaciones, mapa de spots |
| UID interno | Generado por Firebase | Identificador opaco interno (no tiene significado legal ni se publica) |

### 2.2 Datos opcionales (perfil avanzado)

Solo si tu los introduces voluntariamente desde "Mi Zona":

- Avatar y nombre publico (apodo).
- Bio corta.
- Telefono movil (necesario solo para promocionarte a rol economico — organizador / comercio / sponsor — en futuras fases).
- Direccion postal (envios marketplace).
- CIF/NIF y datos fiscales (necesarios solo si activas un perfil profesional vendedor / organizador, conforme a obligaciones tributarias).

**Importante:** WeRock M0 NO pide ningun documento legal (DNI, CIF) en el registro inicial. Solo se piden si voluntariamente activas un rol economico que tenga implicaciones fiscales.

### 2.3 Datos generados por tu uso

| Categoria | Ejemplos | Finalidad |
| --- | --- | --- |
| Contenido publico | Spots que publicas, fotos de spots, eventos que organizas, posts en el feed, comentarios, kudos, valoraciones de tricks | Mostrarlo al resto de la comunidad WeRock |
| Contenido privado | Sesiones GPS de entrenamiento (`tracked_sessions`), perfil de gear, recomendaciones IA personalizadas | Tu estadistica personal, no se comparte por defecto |
| Telemetria de uso | Pantallas visitadas, tiempo en app, dispositivo, sistema operativo, version app, region | Mejorar la app, diagnosticar bugs (Firebase Analytics + Crashlytics) |
| Logs de errores | Stack traces, breadcrumbs (sin PII directo: filtramos email, phone, CIF/NIF antes de logear) | Diagnostico de fallos (Firebase Crashlytics) |
| Posicion GPS | Solo si das permiso: para mostrar spots cercanos y registrar sesiones | Funcionalidad mapa y tracking |

### 2.4 Datos que NO recogemos

- Listado de contactos del telefono.
- Mensajes SMS, llamadas, calendario.
- Historial de navegacion fuera de la app.
- Datos biometricos (huella, FaceID) — los usa el sistema operativo para desbloqueo, nosotros no los recibimos.
- Datos de salud detallados (HRV, frecuencia cardiaca continua) — M0 no integra wearables; cuando se integre sera con tu permiso explicito y consentimiento granular separado.

## 3. Bases legales del tratamiento

| Tratamiento | Base legal |
| --- | --- |
| Crear y mantener tu cuenta | Ejecucion del contrato (art. 6.1.b RGPD) — sin estos datos no podemos prestarte el servicio |
| Verificar tu identidad anti-fraude (App Check + Play Integrity) | Interes legitimo (art. 6.1.f RGPD) — proteger la comunidad y nuestros costes contra granjas de cuentas |
| Telemetria operativa (Crashlytics, Analytics) | Interes legitimo (art. 6.1.f RGPD) — mejorar la app sin identificarte personalmente |
| Recomendaciones IA, asistente AI Mayordomo | Ejecucion del contrato + tu consentimiento expreso al usar el feature |
| Datos fiscales (cuando los introduces) | Obligacion legal (art. 6.1.c RGPD) — Ley General Tributaria 58/2003 y normativa de comercio electronico |
| Marketing y comunicaciones promocionales | Tu consentimiento explicito (art. 6.1.a RGPD) — siempre opt-in y revocable |

## 4. Plazos de conservacion

| Categoria de dato | Plazo |
| --- | --- |
| Cuenta activa | Mientras la cuenta exista |
| Cuenta inactiva (sin login >12 meses) | Aviso por email; si no respondes, eliminamos la cuenta a los 24 meses sin actividad |
| Datos fiscales (facturacion) | 6 anos (obligacion mercantil, art. 30 Codigo de Comercio) |
| Logs de errores y telemetria | 30 dias (Cloud Logging) — borrado automatico tras la ventana |
| Inscripciones a eventos pagados | 5 anos tras el evento (obligacion fiscal y reclamacion civil) |
| Datos tras solicitud de borrado (RGPD Art. 17) | Borrado inmediato salvo los que la ley nos obliga a conservar (facturas) |

## 5. Quien recibe tus datos (subprocesadores)

WeRock no vende datos personales. Compartimos datos con los siguientes proveedores tecnicos para prestarte el servicio. Todos cumplen con RGPD via Clausulas Contractuales Tipo (CCT) y/o Adequacy Decision europea:

| Proveedor | Funcion | Region procesado | Marco legal |
| --- | --- | --- | --- |
| Google Firebase (Firestore, Auth, Storage, RTDB) | Backend, autenticacion, almacenamiento | `europe-west1` (Belgica) | RGPD + CCT |
| Google Cloud Functions | Logica de negocio, IA | `europe-west1` (Belgica) | RGPD + CCT |
| Google Vertex AI (Gemini) | Asistente IA, parsing de texto | `europe-west4` (Holanda) → `europe-west1` (Belgica) → `global` solo como fallback | RGPD + CCT. Filtramos datos PII antes de enviar al modelo |
| Google Cloud Logging | Logs operativos | `europe-west1` (Belgica) | RGPD |
| Google Maps Platform | Mapas, geocoding | Global. Solo enviamos coordenadas o textos publicos, nunca tu UID/email | RGPD + CCT |
| Stripe (cuando uses pagos) | Procesamiento de pagos | EEUU + Europa, segun region de tu tarjeta | RGPD + CCT + PCI-DSS Level 1 |
| Resend | Envio de emails operativos | EEUU. Solo enviamos email destino, no contenido sensible | RGPD + CCT |
| GitHub | Hosting de codigo / docs (no tus datos personales) | EEUU | RGPD + CCT |
| Sentry / Crashlytics | Reporte de fallos | EEUU (Crashlytics) | RGPD + CCT. Filtramos PII de los reportes |

## 6. Tus derechos RGPD

Tienes derecho a:

| Derecho | Como ejercerlo |
| --- | --- |
| **Acceso** (art. 15) — saber que datos tenemos sobre ti | Email a `privacy@werock.app` o desde "Mi Zona → Privacidad → Solicitar mis datos" (export en JSON, M1) |
| **Rectificacion** (art. 16) — corregir datos | Editas tu perfil en "Mi Zona" o pide ayuda en `privacy@werock.app` |
| **Supresion / Borrado** (art. 17) — borrar la cuenta | "Mi Zona → Privacidad → Borrar mi cuenta" (purga inmediata via Cloud Function `deleteUserAccountV1`); o `privacy@werock.app` |
| **Oposicion** (art. 21) — oponerte a un tratamiento concreto | `privacy@werock.app` indicando que tratamiento te opones |
| **Limitacion** (art. 18) | `privacy@werock.app` |
| **Portabilidad** (art. 20) — recibir tus datos en formato leible por maquina | `privacy@werock.app`. Te enviamos un JSON con todo tu perfil + contenido. Tiempo de respuesta: hasta 30 dias |
| **Retirar consentimiento** | Para marketing: opt-out desde Mi Zona → Notificaciones. Para tracking GPS: revocar permiso del sistema. Para AI: deja de usar el asistente |
| **Reclamacion ante la AEPD** | Si crees que infringimos tus derechos, puedes reclamar ante la **Agencia Espanola de Proteccion de Datos** (`https://www.aepd.es/`), tras intentar resolverlo con nosotros |

## 7. Menores de edad

- **Edad minima absoluta:** 13 anos (RGPD permite menores con consentimiento parental >= 14 segun pais; Espana fija el umbral en **14 anos**).
- Entre 14 y 17: puedes registrarte por ti mismo. Para acciones que tengan implicaciones legales o economicas (eventos pagados, profesional, fiscal) te pediremos consentimiento parental documentado.
- Menores de 14: NO podemos registrar tu cuenta sin consentimiento parental verificable.

## 8. Cookies y tecnologias similares

WeRock app movil **no usa cookies** (no es una web). El web build (cuando se publique) usara solo:

- **Cookies tecnicas** (sesion Firebase Auth) — necesarias, no requieren consentimiento bajo art. 22.2 LSSI.
- **NO usamos cookies analiticas o publicitarias** en M0.

## 9. Transferencias internacionales

Algunos subprocesadores (Stripe, Resend, Crashlytics, Vertex AI fallback global) tratan datos en EEUU u otros paises fuera del EEE. Estas transferencias estan amparadas por:

- **Clausulas Contractuales Tipo (CCT)** aprobadas por la Comision Europea.
- **Data Privacy Framework EU-US** (cuando aplica).
- **Adequacy Decisions** vigentes.

Te garantizamos que ningun dato fiscal (CIF/NIF, direccion postal completa) sale del EEE en M0. Solo telemetria operativa anonima y emails de notificacion pueden ir a EEUU.

## 10. Seguridad de los datos

Aplicamos medidas tecnicas y organizativas apropiadas (art. 32 RGPD):

- **Cifrado en transito:** TLS 1.2+ para todas las comunicaciones cliente-servidor.
- **Cifrado en reposo:** Firebase cifra automaticamente Firestore, Storage, RTDB y Auth con AES-256.
- **App Check + Play Integrity:** verificacion de dispositivo Android real, bloquea bots y emuladores.
- **Reglas de acceso (Firestore + Storage rules):** datos privados solo accesibles a su dueño, con jerarquia de roles (rider, organizador, comercio, manager, admin).
- **Logging sin PII:** los logs operativos no contienen email, telefono, CIF/NIF, direccion postal.
- **Right of erasure automatizado:** cualquiera puede borrar su cuenta en un click sin intervencion manual.
- **Auditoria de borrados:** mantenemos un audit log no-PII (`data_deletion_audit`) para responder a auditorias.

## 11. Cambios en esta politica

Publicaremos cualquier cambio material aqui con anotacion en la seccion **Historial** (al final). Te avisaremos por email con al menos **15 dias de antelacion** antes de la entrada en vigor de cambios materiales.

## 12. Contacto

Para cualquier consulta sobre esta politica:

- **Email:** `privacy@werock.app`
- **Direccion postal:** publicada antes del lanzamiento publico (Sprint C)

---

## Historial

| Version | Fecha | Cambios |
| --- | --- | --- |
| 1.0 (M0) | 6 may 2026 | Version inicial M0 — beta cerrada Espana, Android only |
