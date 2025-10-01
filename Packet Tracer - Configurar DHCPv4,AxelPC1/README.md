 🧪 Packet Tracer – Configurar DHCPv4

Este proyecto corresponde al ejercicio 7.2.10 del curso CCNA v7, donde se configura un router Cisco como servidor DHCPv4, se implementa retransmisión DHCP y se verifica la conectividad entre dispositivos.

 🎯 Objetivos del ejercicio

- Configurar un router como servidor DHCP.
- Implementar DHCP Relay en routers intermedios.
- Configurar un router como cliente DHCP.
- Verificar asignaciones IP y conectividad entre hosts.

 🧩 Topología

La red está compuesta por tres routers (R1, R2, R3), dos PCs (PC1, PC2) y un servidor DNS. R2 actúa como servidor DHCP centralizado.

⚙️ Configuraciones clave

 🔐 Exclusión de direcciones

R2(config)# ip dhcp excluded-address 192.168.10.1 192.168.10.10

R2(config)# ip dhcp excluded-address 192.168.30.1 192.168.30.10

📦 Pools DHCP

R2(config)# ip dhcp pool R1-LAN

R2(dhcp-config)# network 192.168.10.0 255.255.255.0

R2(dhcp-config)# default-router 192.168.10.1

R2(dhcp-config)# dns-server 192.168.20.254

R2(config)# ip dhcp pool R3-LAN

R2(dhcp-config)# network 192.168.30.0 255.255.255.0

R2(dhcp-config)# default-router 192.168.30.1

R2(dhcp-config)# dns-server 192.168.20.254

📡 DHCP Relay

R1(config)# interface g0/0

R1(config-if)# ip helper-address 10.1.1.2

R3(config)# interface g0/0

R3(config-if)# ip helper-address 10.2.2.2

🌐 Cliente DHCP
bash
R2(config)# interface g0/1

R2(config-if)# ip address dhcp

R2(config-if)# no shutdown

✅ Verificación
Comando: show ip dhcp binding en R2.
Comando: show ip interface brief para verificar IP dinámica.
Pruebas de ping entre PC1, PC2 y otros dispositivos.

👨‍💻 Autor
Axel Jean Piero Bazán Ramos Estudiante de Ingeniería de Sistemas – UTP Arequipa, Perú
