📘 Packet Tracer - Revisión de una Configuración del Router

🧩 Descripción
Este proyecto simula la configuración básica de un router Cisco (R2) en Packet Tracer. Incluye asignación de direcciones IP, configuración de parámetros de seguridad, habilitación de acceso remoto por SSH y verificación de conectividad. Es una práctica integral para reforzar comandos IOS y conceptos de redes IPv4/IPv6.

🎯 Objetivos
Configurar interfaces de PCs y router con direcciones IPv4 e IPv6.

Establecer parámetros básicos del router (hostname, contraseñas, dominio).

Habilitar acceso remoto por SSH.

Verificar conectividad entre dispositivos.

Usar comandos show para revisar el estado del router.

🛠️ Requisitos
Cisco Packet Tracer (versión 7.3 o superior recomendada).

Archivo .pka del laboratorio: 14.3.5 Packet Tracer - Basic Router Configuration Review.pka.

Conocimientos básicos de CLI en routers Cisco.

⚙️ Pasos de Configuración
Parte 1: Configuración y Verificación
Interfaces de PC3 y PC4

Asignar direcciones IPv4 e IPv6 según la tabla de direccionamiento.

Router R2

Cambiar nombre del dispositivo: hostname R2

Configurar contraseñas: enable secret, line console, line vty

Establecer dominio: ip domain-name ccna-lab.com

Crear usuario SSH: username SSHadmin secret 55Hadm!n

Generar claves RSA: crypto key generate rsa

Activar IPv6: ipv6 unicast-routing

Configurar interfaces con IPs, descripciones y no shutdown

Guardar configuración: copy running-config startup-config

Verificación de conectividad

Pings entre PCs y hacia el ISP

Prueba de conexión SSH desde PC3 a R2

Parte 2: Revisión del Router
show version: versión IOS, memoria, tiempo activo

show running-config | include password: verificar cifrado de contraseñas

show ip route: revisar tabla de enrutamiento

show ip interface brief: estado de interfaces IPv4

show ipv6 interface brief: estado de interfaces IPv6

✅ Resultados Esperados
Todas las interfaces activas y correctamente configuradas.

Acceso remoto por SSH funcional.

Pings exitosos entre dispositivos conectados.

Comandos show muestran información precisa del router.

📌 Notas
No se configura ruta por defecto en R2, por lo que solo se accede a redes locales.

El comando service password-encryption cifra las contraseñas en texto plano.

📚 Créditos
Basado en la actividad oficial del curso CCNA v7 de Cisco Networking Academy. Guía de referencia: ExamenRedes - Revisión básica del router
