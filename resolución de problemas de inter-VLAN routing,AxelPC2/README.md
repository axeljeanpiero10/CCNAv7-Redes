🛠️ Packet Tracer - Resolución de Problemas de Inter-VLAN Routing

📘 Descripción
Este proyecto simula una red con múltiples VLANs y un router configurado para enrutamiento entre VLANs. El objetivo es identificar y corregir errores de configuración que impiden la conectividad entre dispositivos de distintas VLANs. Es una práctica clave para afianzar conceptos de subinterfaces, trunking y direccionamiento IP.

🎯 Objetivos
Diagnosticar problemas de conectividad entre VLANs.

Corregir configuraciones erróneas en el router y el switch.

Verificar el funcionamiento del enrutamiento inter-VLAN.

Aplicar comandos de verificación y solución en CLI.

🧪 Escenario
La red incluye:

Router R1 con subinterfaces G0/1.10 y G0/1.30.

Switch S1 con puertos asignados a VLAN 10 y VLAN 30.

PCs en VLAN 10 (PC1) y VLAN 30 (PC3).

🔍 Comandos Útiles
show ip interface brief

show interface g0/1.10

show interface trunk

ping entre PCs y hacia el router

✅ Resultados Esperados
Subinterfaces activas y correctamente encapsuladas.

Switch configurado en modo troncal.

PCs con gateway correcto.

Pings exitosos entre VLANs.

✅ Datos correctos 
se tiene los registros guardados en 
problem1rede.xlsx
