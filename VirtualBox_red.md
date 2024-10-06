## VirtualBox Red
**A la hora de crear una máquina virtual en VirtualBox este nos ofrece una gran cantidad de opciones de configuración a nivel de red.**

## Configuraciones de red

### NAT
La VM obtiene dirección IP privada de una subred que va a definir VirtualBox.La IP privada asignada proviene de una subred definida en la configuración de virtualBox.Misma conectividad que el PC host en salida pero no es posibLe comunicarse con la máquina virtual desde un equipo que este fuera de la red local si no activamos la opción "Reenvío de puertos"

*La VM accede a Internet, pero es invisible desde el exterior.*

### Red NAT
Similiar a NAT es decir,la VM obtiene dirección IP privada definida por virtualBox. La diferencia radica en que cada máquina virtual conectada a la red NAT puede comunicarse con el resto de máquinas en la misma red, es decir podemos acceder a la máquina desde otro equipo que este en la misma red NAT.

*Varias VM pueden comunicarse entre sí y acceder a Internet.*

### Adaptador puente
A la máquina virtual se le asigna una IP privada de la misma forma que las del resto de máquinas locales como si fuera otro dispositivo más en la red. La máquina virtual tiene su propia IP y esta completamente integrada en la red como un dispositivo más.

*La VM está completamente integrada en la red del anfitrión, con su propia IP.*

### Red Interna
La máquina virtual no tiene acceso a ninguna red externa, solo podría comunicarse con el resto de máquinas que se encuentren en la misma red interna. La IP de estas máquinas se puede configurar de forma manual o mediante un servidor DHCP pero VirtualBox no va a proporcionar un servidor DHCP por defecto para este modo como lo hace para NAT.

*Las VM solo se comunican entre ellas, en un entorno aislado.*

### Adaptador solo para anfitrión
La máquina virtual puede comunicarse con el anfitrión y con otras máquinas virtuales que esten en el mismo modo <u>Host-Only</u>. VirtualBox crea automáticamente una interfaz de red virtual "Host-Only" en el sistema anfitrión y un servidor DHCP para esa red, por lo que no es necesario asignar IPs de forma manual.

*Las VM y el anfitrión pueden comunicarse, pero no tienen acceso a Internet.*

### Controlador genérico
Opción avanzada de red que permite utilizar controladores personalizados para cada VM. No es muy habitual, y su configuración depende del hardware y las necesidades específicas.
Suele usarse para configuraciones específicas con hardware o drivers adicionales.

*Configuración avanzada para controladores personalizados.*

### No conectado
La máquina virtual no esta conectada a ninguna red y no puede comunicarse con otras máquinas ni con el anfitrión.

*La VM no está conectada a ninguna red.*



