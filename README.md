#  Creación de Cuenta y Máquina Virtual en Azure for Students

## Introducción
Este documento explica el procedimiento seguido para **crear la cuenta de Azure for Students** y configurar una **máquina virtual (VM)** que sirvió como base para desplegar la aplicación **PokeDex (Angular)**.  
El objetivo principal fue disponer de un entorno en la nube gratuito, seguro y flexible para el despliegue de proyectos web académicos.

---

## 1. Registro en Azure for Students

### 1.1 Acceso al portal
Se ingresó al sitio oficial de registro de Azure for Students:  
🔗 [https://azure.microsoft.com/es-es/free/students/](https://azure.microsoft.com/es-es/free/students/)

### 1.2 Requisitos
- Correo institucional activo 
- Acceso a Internet estable  
- Verificación académica (Azure valida que el correo pertenece a una institución educativa)

### 1.3 Activación de beneficios
Una vez validada la cuenta, Microsoft otorga:
- **100 USD en créditos** gratuitos (sin necesidad de tarjeta bancaria)  
- Acceso a todos los servicios de Azure (máquinas virtuales, redes, almacenamiento, etc.)  

---

## 2. Ingreso al portal de Azure

Tras la activación, se accedió al panel principal en:  
🔗 [https://portal.azure.com](https://portal.azure.com)

La interfaz principal permite crear y gestionar recursos.  
En el buscador superior escribe **“máquinas virtuales”**:



En la vista se muestra el acceso directo a:
- Crear un nuevo recurso  
- Ver las máquinas virtuales existentes  
- Revisar los grupos de recursos recientes 
- Gestionar suscripciones de Azure for Students  

---

## 3. Creación de la Máquina Virtual (VM)

### 3.1 Selección del recurso
En el menú de servicios se seleccionó:
> **“Máquinas virtuales → Crear”**

Esto abre el asistente para generar una nueva VM.

### 3.2 Configuración básica
Se definieron los parámetros principales:

| Parámetro | Valor asignado |
|------------|----------------|
| **Suscripción** | `Azure for Students` |
| **Grupo de recursos** | `pokedex-prod` |
| **Nombre de la VM** | `vm-pokedex` |
| **Región** | La más cercana geográficamente |
| **Imagen** | Ubuntu Server 24.04 LTS |
| **Tamaño** | Standard_D2s_v3 - 2 vcpu, 8 GiB de memoria |
| **Autenticación** | Contraseña |
| **Nombre de usuario** | andresgary |
| **Contraseña** | Andresgary8113 |
| **Puertos publicos** | Permitir puertos seleccionados |
| **Puertos de entrada** | 22 (SSH), 80 (HTTP), 443 (HTTPS) |

### 3.3 Grupo de recursos
Durante la creación se generó un grupo de recursos llamado **`pokedex-prod`**, que agrupa todos los componentes relacionados con la VM.

---

## 4. Revisión y creación

Una vez completados los campos, Azure mostró un **resumen de la configuración**.  
Tras la validación, se pulsó **“Crear”**, iniciando el despliegue automático de la VM.

El proceso tardó entre 2 y 4 minutos. Al finalizar, se asignó automáticamente:
- Una **IP pública** (para conexión SSH y acceso web)
- Un **nombre DNS temporal** (si se configura)

---

## 5. Conexión a la máquina virtual

### 5.1 Acceso correcto

Si la conexión se establece correctamente, aparece el mensaje de bienvenida del servidor Ubuntu.

----------

## 6. Verificación en el portal

En la sección **“Máquinas virtuales”** se confirmó que la instancia aparecía como:

-   Estado: **En ejecución**
    
-   Nombre: **vm-coolify**
    
-   Grupo de recursos: **rg-coolify**
    
-   Sistema operativo: **Linux**
    
-   IP pública visible
    

----------

## 7. Resultado final

La cuenta de **Azure for Students** y la **máquina virtual** quedaron correctamente configuradas.  
Esta VM sirvió como infraestructura base para:

-   Instalar **Coolify** (plataforma PaaS autoalojada)
    
-   Desplegar la aplicación web **PokeDex (Angular)**
    
-   Configurar HTTPS, DNS y seguridad HTTP
    

----------

## Conclusión

Gracias a **Azure for Students**, se logró crear y administrar una máquina virtual gratuita que proporciona un entorno de desarrollo profesional en la nube.  
El proceso es reproducible, seguro y escalable, ideal para proyectos académicos o pruebas de despliegue.

    



