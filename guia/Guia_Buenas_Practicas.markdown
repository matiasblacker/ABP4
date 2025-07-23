# Guía de Buenas Prácticas – Proyecto Infraestructura Viva

## Seguridad
- Utilizar **grupos de seguridad restrictivos**, permitiendo solo el tráfico necesario (por ejemplo, puertos 22, 80 y 443).
- Habilitar **Multi-AZ y backups automáticos** en RDS para alta disponibilidad y recuperación ante desastres.
- Configurar políticas de acceso en S3 para evitar la exposición pública de datos sensibles.

## Escalabilidad
- Desplegar instancias EC2 dentro de un **Balanceador de Carga (ELB)** para manejar tráfico variable.
- Utilizar **Amazon CloudFront** para mejorar la entrega de contenido estático a nivel global.
- Configurar **escalado automático** para instancias EC2 si el proyecto lo requiere a futuro.

## Redes
- Crear una VPC con **subredes públicas y privadas**, asegurando separación de servicios.
- Limitar el acceso a bases de datos usando **subredes privadas**.
- Usar VPN o túneles seguros si se necesita conexión híbrida con sistemas on-premise.

## Monitoreo
- Configurar métricas clave en CloudWatch (CPU, errores, tráfico).
- Establecer **alarmas** con notificaciones a través de SNS para problemas críticos.
- Usar logs para auditar eventos y anticiparse a incidentes.

## Costos
- Mantenerse dentro del **nivel gratuito de AWS** siempre que sea posible.
- Automatizar la eliminación de recursos cuando no se usen (por ejemplo, con scripts o policies de retención).
