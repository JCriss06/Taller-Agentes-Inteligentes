# Taller-Agentes-Inteligentes

## Descripción General

Este proyecto es un sistema de agendamiento de citas diseñado para ilustrar la productividad exponencial que se logra al dirigir a Agentes Inteligentes de Programación. El desarrollo se centró en aplicar el concepto de "Pensamiento en Contratos", asegurando una arquitectura modular que separa estrictamente la lógica de negocio de la implementación de la interfaz y la persistencia.

Ofrece una interfaz fácil de usar para que los administradores y clientes puedan crear, actualizar y manejar citas e información sobre los clientes.

## Características Arquitectónicas y Funcionales
* Gestión de Entidades (CRUD): Implementación de las operaciones básicas de Crear, Obtener, Actualizar y Eliminar para los recursos de Citas/Turnos y Clientes/Registros.

* Módulo de Notificaciones Automatizadas: Uso de Background Jobs (Job Scheduling) para el envío de recordatorios de citas por correo electrónico y/o SMS.

* Seguridad: Implementación de middleware para la autenticación y protección de las rutas críticas.

* Integración de Base de Datos: Conexión para el almacenamiento persistente de todos los datos del sistema.

## Estructura del Proyecto
La organización sigue un patrón modular para facilitar la comprensión de las responsabilidades de cada capa del código:

appointment-scheduler  
├── src  
│   ├── api  
│   │   ├── controllers    
│   │   ├── routes  
│   │   └── middleware  
│   ├── config  
│   ├── db  
│   ├── jobs  
│   ├── models  
│   ├── notifications  
│   ├── repositories  
│   ├── services  
│   ├── types  
│   └── utils  
├── tests  
│   ├── integration  
│   └── unit  
├── scripts  
├── docker  
├── .env.example  
├── package.json  
├── tsconfig.json  
├── ormconfig.js  
├── .eslintrc.js  
├── .prettierrc  
└── .gitignore  

## Instalación
Clonar el repositorio:
```Bash
git clone <repository-url>
```
Navegar al directorio del proyecto:
```Bash
cd appointment-scheduler
```
Instalar dependencias:
```Bash
npm install
```
Configurar la Base de Datos:  
Asegúrese de configurar sus variables de entorno en .env (siguiendo el ejemplo de .env.example) y luego ejecute el script de inicialización:
```Bash
./scripts/setup-db.sh
```

## Uso
Iniciar el servidor:
```Bash
npm start
```
Acceda a la documentación de la API para interactuar con los endpoints de gestión de citas y clientes.
