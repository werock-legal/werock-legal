# Terminos del Servicio — WeRock

**Ultima actualizacion:** 6 de mayo de 2026
**Version:** 1.0 (M0)

Estos terminos regulan el uso de la aplicacion **WeRock** (`https://werock.app`) y servicios asociados, prestados por **WeRock Platform** (en adelante, "WeRock", "nosotros") al usuario registrado (en adelante, "rider" o "tu").

Al crear una cuenta o usar la app, aceptas estos terminos. Si no estas de acuerdo, no uses la app.

---

## 1. Que es WeRock

WeRock es una plataforma social y operativa para deportes de accion: patinaje en linea, skate, ciclismo, running. Te permite:

- Descubrir spots y rutas validados por la comunidad.
- Inscribirte y organizar eventos (clases, viajes, talleres, retos).
- Compartir contenido (posts, fotos, videos cortos) con otros riders.
- Trackear sesiones de entrenamiento.
- Obtener recomendaciones personalizadas via asistente IA AI Mayordomo.
- Comprar y vender material de segunda mano (P2P) y nuevo (cuando publiquemos el modulo Pro).
- Ganar **ABECs** (moneda virtual interna) por contribucion comunitaria.

WeRock NO es una agencia de viajes, NO contrata seguros, NO actua como entidad organizadora de los eventos: solo facilita la conexion entre riders y organizadores.

## 2. Registro y cuenta

### 2.1 Edad minima

Debes tener al menos **14 anos** cumplidos para registrarte (limite legal LOPDGDD Espana). Entre 14 y 17 puedes registrarte por ti mismo, pero algunas acciones (eventos pagados, ventas) requieren consentimiento parental.

### 2.2 Veracidad

Te comprometes a registrar datos verdaderos. Crear cuentas con email falso, datos de terceros o multiples cuentas para abusar del sistema (granjeo de ABECs, evasion de bans) supone **expulsion inmediata** y bloqueo del email/dispositivo.

### 2.3 Una cuenta = una persona

WeRock detecta y bloquea cuentas duplicadas mediante App Check + Play Integrity + caps de ABECs por cuenta + revision manual de patrones sospechosos. Si necesitas multiple cuentas legitimas (ej. una personal y una de tu tienda), abre un caso en `support@werock.app` antes para evitar baneos automaticos.

### 2.4 Seguridad de tu cuenta

Eres responsable de:

- Guardar tu contrasena de forma segura (no compartirla).
- Cerrar sesion en dispositivos que no sean tuyos.
- Notificarnos en `support@werock.app` si sospechas acceso no autorizado.

## 3. Reglas de la comunidad

Al usar WeRock te comprometes a NO:

1. Publicar contenido ilegal, violento, sexual explicito, discriminatorio, de odio o que vulnere derechos de terceros (incluyendo derechos de imagen y propiedad intelectual).
2. Acosar, intimidar o amenazar a otros riders.
3. Suplantar a otra persona, marca o entidad.
4. Spam: publicar contenido repetitivo, links promocionales no relacionados, schemes piramidales o reclutamiento para servicios externos no autorizados.
5. Manipular el sistema de ABECs, kudos, valoraciones, validaciones o ranking (granjeo).
6. Hackear, ingenieria inversa, scraping no autorizado o ataques DDoS contra la plataforma.
7. Subir malware, virus o contenido que pueda danar dispositivos de terceros.
8. Explotar bugs en lugar de reportarlos a `bugs@werock.app`.
9. Usar la app para actividades comerciales fuera del modulo Pro autorizado.

Las violaciones se sancionan con:

- Aviso (primera vez, falta leve).
- Suspension temporal (faltas medias o reincidencia).
- **Expulsion permanente** (faltas graves: acoso, contenido ilegal, granjeo masivo). En este caso perderas acceso a tu cuenta, contenido publicado puede ser retirado y los ABECs no se reembolsan.

## 4. Contenido publicado

### 4.1 Tu contenido sigue siendo tuyo

Al subir un post, una foto de spot, un video de un truco, mantienes la propiedad intelectual.

### 4.2 Licencia que nos das

Para que podamos mostrarlo a la comunidad y prestarte el servicio, nos otorgas una licencia **mundial, no exclusiva, gratuita, transferible** para:

- Almacenarlo en nuestra infraestructura (Firebase Storage, region `europe-west1`).
- Mostrarlo dentro de la app a otros riders y a sistemas de moderacion automatizada.
- Procesarlo con IA solo para tareas explicitas (ej. detectar contenido inapropiado, generar miniaturas).
- Indexarlo para busqueda interna.

Esta licencia termina cuando:

- Borras el contenido (lo eliminamos en 30 dias del backup).
- Borras tu cuenta (purga total inmediata via `deleteUserAccountV1`).

### 4.3 Lo que NO podemos hacer con tu contenido

- Venderlo a terceros.
- Usarlo en campanas publicitarias externas sin consentimiento explicito por escrito.
- Entrenar modelos de IA propios de WeRock (Gemini de Google es proveedor, no nosotros, y solo procesa datos que le enviamos para devolver respuesta — no los guarda como training data).

### 4.4 Moderacion

Nos reservamos el derecho de:

- Eliminar contenido que viole estos terminos sin previo aviso.
- Suspender cuentas que reincidan.
- Cooperar con autoridades en caso de actividad delictiva (denuncias judiciales).

## 5. ABECs (moneda virtual interna)

### 5.1 Que son los ABECs

ABECs son **puntos virtuales** de actividad y contribucion comunitaria. NO son dinero real, NO son criptomonedas, NO se pueden convertir a euros.

### 5.2 Como se ganan

Por contribucion al ecosistema (publicar spots validados, organizar eventos exitosos, enviar feedback util al asistente IA, etc.). Los detalles del sistema de recompensas estan en `lib/config/abec_economy_config.dart` (mirror server-side `ABEC_DAILY_CAPS / MONTHLY_CAPS`) — pueden ajustarse por updates de la app.

### 5.3 Para que sirven

Los ABECs te permiten desbloquear **cuota IA extra** (mas consultas al asistente AI Mayordomo cuando agotas tu cuota gratuita diaria) y, en futuras fases, otros canjes intracomunidad.

### 5.4 Caducidad y reseteo

Los ABECs caducan a los **24 meses** sin uso. Si tu cuenta queda inactiva, los ABECs no acumulados durante la inactividad se pierden.

### 5.5 Penalizaciones

Si detectamos granjeo o fraude, **anulamos los ABECs ganados ilicitamente** sin compensacion.

## 6. Eventos pagados

Cuando organizas o te inscribes en un evento pagado:

- WeRock **NO es organizadora** del evento. La organizacion legal corresponde al rider/empresa que lo crea.
- WeRock actua como **intermediario tecnico** que facilita inscripciones y pagos via Stripe.
- WeRock cobra una **comision de servicio** (porcentaje detallado en la pagina del evento al inscribirte).
- Los **reembolsos** dependen de la politica del organizador, mostrada en cada evento. Si el organizador cancela, te reembolsamos automaticamente menos comisiones de plataforma irrecuperables.

## 7. Marketplace P2P

Cuando vendes o compras articulos entre riders:

- WeRock facilita el contacto y, opcionalmente, el escrow de pago.
- La transaccion es **entre riders**, WeRock no garantiza calidad / autenticidad / estado del producto.
- Para vender de forma habitual te tienes que dar de alta como Pro (con CIF/NIF y obligaciones fiscales propias).

## 8. Disponibilidad del servicio

Nos esforzamos en ofrecer >99% uptime, pero **no garantizamos servicio ininterrumpido**:

- Mantenimiento programado: te avisaremos en la app.
- Fallos de proveedores (Firebase down, Stripe down) — fuera de nuestro control directo.
- Beta cerrada M0: pueden producirse cortes mas frecuentes que en una version GA. Reportalos en `bugs@werock.app`.

No nos hacemos responsables por danos derivados de cortes de servicio salvo dolo o negligencia grave probada.

## 9. Limitacion de responsabilidad

WeRock no se hace responsable por:

- Lesiones, accidentes o danos durante la practica deportiva. **Patinas, montas o corres bajo tu propia responsabilidad.** Cada evento puede tener su propio waiver legal (lo aceptas al inscribirte).
- Disputas entre riders, organizadores o comercios fuera de la plataforma.
- Datos publicados por otros riders (spots erroneos, reviews falsas) que tu uses como guia. Verifica siempre por tu cuenta.
- Robos, perdidas o danos materiales en eventos no organizados directamente por WeRock.

Nuestra responsabilidad agregada esta limitada al maximo permitido por ley aplicable y nunca superara el equivalente al **importe de tus pagos a WeRock en los 12 meses anteriores al hecho** (incluyendo cero, si no has pagado nada).

## 10. Cambios en los terminos

Podemos modificar estos terminos. Te avisaremos por email con **15 dias de antelacion** ante cambios materiales. Si sigues usando la app despues de la entrada en vigor, aceptas los nuevos terminos. Si no estas de acuerdo, puedes borrar tu cuenta antes (RGPD Art. 17, sin coste).

## 11. Ley aplicable y jurisdiccion

- **Ley aplicable:** legislacion espanola, Reglamento (UE) 2016/679 (RGPD), Ley 34/2002 de Servicios de la Sociedad de la Informacion (LSSI), Ley General para la Defensa de los Consumidores y Usuarios.
- **Jurisdiccion:** tribunales del domicilio del consumidor (cuando seas consumidor en Espana o UE) o, alternativamente, tribunales de la sede social de WeRock (cuando uses la plataforma como Pro / empresa).

## 12. Contacto

- **Atencion al cliente:** `support@werock.app`
- **Reportes de bug y abuso:** `bugs@werock.app`
- **Privacidad / RGPD:** `privacy@werock.app`
- **Asuntos legales:** `legal@werock.app`

---

## Historial

| Version | Fecha | Cambios |
| --- | --- | --- |
| 1.0 (M0) | 6 may 2026 | Version inicial M0 — beta cerrada Espana, Android only |
