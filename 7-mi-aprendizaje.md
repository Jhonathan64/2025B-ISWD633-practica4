# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.

Al comenzar con esta práctica no tenía conocimiento en cuanto a los recursos de la memoria y demás pero ahora al comparar mis conocimientos teóricos iniciales con lo que logré aplicar y solucionar en esta práctica, mis principales avances se centran en cómo hacer que los programas dentro de Docker usen solo los recursos que necesitan y se mantengan funcionando de forma confiable.

Memoria y CPU 
Antes del taller, sabía que Docker podía limitar los recursos, pero ahora sé cómo hacerlo con precisión, lo cual es vital para el buen funcionamiento de muchas aplicaciones en un solo servidor.
•	Memoria: Aprendí a distinguir y establecer el límite de Memoria RAM con su respectivo comando por separado de la memoria total que incluye el área de intercambio (Swap), usando (--memory-swap). Esto me permite gestionar la memoria de manera eficiente.
•	CPU: Descubrí cómo asignar una cantidad específica de potencia de procesamiento, incluso fracciones (--cpus="1.5"). Lo más importante es que aprendí a encerrar un programa en núcleos específicos (--cpuset-cpus), lo que evita que el programa se pelee con otros por la potencia del procesador y garantiza su rendimiento.

Imágenes
La práctica con el Dockerfile me enseñó a convertir una serie de pasos de instalación en una receta automática para crear imágenes.
•	Comprendí cómo Docker es inteligente al construir. Cada paso crea una capa, y si un paso no cambia (como instalar un paquete grande), Docker lo saca de un "almacén" (el caché) y se salta ese proceso. Esto me permite hacer cambios rápidos en mi código sin tener que esperar por la reinstalación de todo el sistema base.
•	Aprendí a usar comandos esenciales (RUN, COPY, EXPOSE, CMD) para asegurarme de que la imagen contenga todo lo necesario y sepa qué hacer exactamente cuándo se inicie como contenedor.

Políticas de Reinicio
Finalmente, aprendí a hacer que mis programas sean más robustos, es decir, que se recuperen solos si algo sale mal:
•	Usando la opción --restart, puedo configurar un contenedor para que se vuelva a encender inmediatamente si falla (on-failure o always). Esto significa que Docker actúa como un vigilante que asegura que el servicio esté siempre disponible, sin necesidad de intervención manual.

Problema Solucionado
Un logro significativo fue solucionar un problema técnico durante la construcción de la imagen de CentOS 7. El comando de actualización (yum update) falló porque los sitios web de descarga de software de CentOS se habían movido. Esto me obligó a investigar y a añadir un paso extra en el Dockerfile para redirigir la configuración de paquetes de CentOS a la nueva ubicación de archivo. Esto me enseñó a no solo escribir la receta, sino también a solucionar fallos a nivel del sistema operativo base dentro del proceso de construcción.
