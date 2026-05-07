# Eliminar datos sin cerrar tu cuenta de WeRock

**Ultima actualizacion:** 7 de mayo de 2026
**Version:** 1.0 (M0)

> **Mirror publico:** este archivo es la fuente de verdad. La copia
> publicada en `https://legal.werockapp.com/delete-data-es` se actualiza
> desde el repo `werock-legal/werock-legal` (GitHub Pages + custom domain
> via Cloudflare DNS). Cualquier cambio aqui debe propagarse al mirror.

WeRock (`https://werockapp.com`) te ofrece un control granular sobre
los datos personales que tratamos. Si no quieres cerrar tu cuenta pero
si quieres que **borremos un subconjunto concreto** de tus datos, esta
pagina te explica como hacerlo. Cumple con el **derecho de supresion
parcial** del **art. 17 RGPD** y el **derecho de oposicion** del
**art. 21 RGPD**.

> **Si lo que quieres es eliminar tu cuenta entera**, ve a
> `https://legal.werockapp.com/delete-account-es`.

---

## 1. Que datos puedes borrar sin cerrar la cuenta

| Categoria | Como se borra | Resultado |
| --- | --- | --- |
| **Sesiones GPS** (`tracked_sessions`) | Mi Zona → Sesiones → mantener pulsado una sesion → "Eliminar" | Las trazas se borran. Tu cuenta y tu progreso public no se ven afectados. |
| **Vídeos de tricks** subidos a TrickTree | Mi Zona → TrickTree → menu del vídeo → "Eliminar" | El archivo de vídeo y el documento desaparecen. Pierdes el XP asociado. |
| **Posts del feed** que has publicado | Comunidad → tu post → menu → "Eliminar" | El post + comentarios + kudos asociados se borran. |
| **Spots** que has publicado | Discover → Mapa → tu spot → menu → "Eliminar" | El spot desaparece de la app si nadie mas lo ha referenciado. |
| **Eventos** que has organizado (sin asistentes confirmados) | Discover → Eventos → tu evento → menu → "Eliminar" | El evento desaparece. Si hay registros de asistentes ya confirmados, primero hay que cancelarlo y notificar antes de borrar. |
| **Anuncios del marketplace** sin operacion en curso | Discover → Market → tu anuncio → menu → "Eliminar" | El listing desaparece. Si tiene un pedido en curso (`pendiente_envio`, `enviado`), primero hay que completar o cancelar la operacion. |
| **Avatar y bio publicos** | Mi Zona → Cuenta → "Editar perfil" → borrar campo → guardar | Tu perfil queda con avatar por defecto y bio vacia. La cuenta sigue activa. |
| **Numero de telefono** | Mi Zona → Cuenta → "Editar perfil" → borrar campo → guardar | Solo lo necesitabas si activaste rol economico. Borrarlo desactiva las funciones que lo requieran. |
| **Datos fiscales (CIF/NIF, direccion fiscal)** | Mi Zona → Cuenta → "Datos profesionales" → "Borrar datos fiscales" | Pierdes el rol economico hasta que vuelvas a introducirlos. Las facturas ya emitidas se conservan por obligacion legal (6 anos, ver §3 abajo). |
| **Direccion de envio** | Mi Zona → Cuenta → "Direcciones" → menu → "Eliminar" | Te impedira comprar en marketplace hasta que añadas otra direccion. |
| **Notificaciones internas leidas** | Notificaciones → "Limpiar leidas" | Se borran de la app. No afecta a la cuenta. |
| **Recomendaciones IA personalizadas** | Mi Zona → Cuenta → "Asistente IA" → "Resetear historial" | Reinicia el contexto del asistente. Tu cuenta y tu progreso siguen intactos. |
| **Permisos de localizacion / camara / microfono** | Ajustes del telefono (Android: Configuracion → Aplicaciones → WeRock → Permisos) | La app dejara de pedir esos datos. Algunas funciones (mapa de spots, vídeos de tricks) dejaran de funcionar. |
| **Marketing y comunicaciones promocionales** | Mi Zona → Cuenta → "Notificaciones y privacidad" → desactivar checkbox | Dejaras de recibir comunicaciones comerciales. Las operativas (cambios materiales en politicas, recibos) se mantienen por obligacion legal. |

Todas estas acciones se ejecutan en menos de 5 segundos directamente
en la app, sin necesidad de contactar con soporte.

---

## 2. Como solicitar borrado parcial via email

Si **no encuentras la opcion** en la app o quieres borrar algo que no
aparece en la tabla anterior, escribenos:

1. Envia un email a **`privacy@werockapp.com`** desde **la direccion
   de email asociada a tu cuenta WeRock** (verificacion sin papeleo).
2. Asunto: `Solicitud de borrado parcial de datos - art. 17 RGPD`.
3. En el cuerpo, especifica **que datos concretos** quieres borrar.
   Ejemplo:

   > Solicito el borrado de:
   > - Todas mis sesiones GPS anteriores al 1 de enero de 2026.
   > - El vídeo de mi truco "kickflip" del 12 de marzo de 2026.
   > - Mi numero de telefono +34 6XX XXX XXX.
   >
   > Quiero **mantener mi cuenta abierta**. Solicito unicamente la
   > supresion de los datos arriba indicados, en ejercicio del derecho
   > de supresion del articulo 17 del Reglamento (UE) 2016/679 (RGPD).

4. Procesaremos la peticion en un plazo maximo de **30 dias naturales**
   (plazo legal RGPD), tipicamente en menos de 72 horas.
5. Recibiras un email final de confirmacion una vez completado el
   borrado.

---

## 3. Que NO podemos borrar (excepciones legales)

Aunque pidas el borrado parcial, hay **datos que estamos obligados a
conservar** durante un plazo minimo legal:

| Categoria | Plazo de retencion | Base legal |
| --- | --- | --- |
| Facturas / tickets emitidos por compras en marketplace o eventos pagados | 6 anos | Ley General Tributaria 58/2003 (art. 29 y 30 — obligacion contable y fiscal) |
| Logs de auditoria de seguridad (intentos fallidos de login, cambios de rol economico) | 1 ano | Interes legitimo (art. 6.1.f RGPD) — proteger el servicio frente a abuso |
| Logs de operaciones de pago Stripe (ID transaccion, importe, fecha) | 6 anos | PSD2 + obligaciones AML + Ley General Tributaria |
| Reportes de moderacion ya cerrados que afectan a otros riders (decisiones tomadas por el equipo de moderacion para protegerlos) | 1 ano | Interes legitimo (art. 6.1.f RGPD) — integridad de la comunidad |

Estos datos retenidos **no se usan para perfilarte** ni para
comunicaciones comerciales. Tras el plazo legal se eliminan
automaticamente.

---

## 4. Que ocurre con datos que afectan a otros riders

Cuando un dato tuyo es referenciado por otro rider (por ejemplo, un
kudos que te dio en uno de sus posts, o que asisitio a un evento que
organizaste), aplicamos un criterio de **anonimizacion en cascada**:

- Tu autoria se elimina o se sustituye por "rider eliminado".
- El contenido del otro rider (su kudos, su asistencia, su comentario)
  se conserva si tiene valor comunitario, pero sin tu identidad
  asociada.
- Si el contenido pierde sentido sin tu autoria (ej. un comentario
  como "gracias @TuNombre"), se conserva textualmente pero no se
  enlaza a tu antiguo perfil.

Este enfoque equilibra tu derecho de supresion con el derecho del
resto de riders a conservar el contenido que ellos mismos crearon.

---

## 5. Plazos y confirmacion

| Etapa | Plazo |
| --- | --- |
| Borrado autoservicio desde la app | Inmediato (< 5 segundos) |
| Recepcion de solicitud por email | Inmediato |
| Borrado tecnico en sistemas | < 72 horas tipico, < 30 dias plazo legal RGPD |
| Borrado en bases analiticas / Crashlytics / backups | < 30 dias (rotacion natural) |

---

## 6. Reclamaciones

Si consideras que no hemos atendido correctamente tu solicitud, puedes
reclamar ante la **Agencia Espanola de Proteccion de Datos (AEPD)**:

- Web: `https://www.aepd.es`
- Sede electronica: `https://sedeagpd.gob.es`
- Direccion postal: C/ Jorge Juan, 6, 28001 Madrid

---

## 7. Contacto

Para cualquier duda relacionada con el borrado parcial o el ejercicio
de tus derechos RGPD:

- **Email privacidad:** `privacy@werockapp.com`
- **Email soporte general:** `support@werockapp.com`
- **Politica de Privacidad completa:** `https://legal.werockapp.com/privacy-es`
- **Eliminar cuenta entera:** `https://legal.werockapp.com/delete-account-es`
- **Terminos del Servicio:** `https://legal.werockapp.com/terms-es`

---

## Historial

| Fecha | Version | Cambio | Operador |
| --- | --- | --- | --- |
| 7 may 2026 | 1.0 | Creacion del documento como respuesta al campo "URL de eliminacion de datos" (opcional pero recomendado) del formulario Data Safety de Google Play Console (Sprint C). Complementa `delete-account-es` permitiendo borrado granular sin cerrar la cuenta. | Agente |
