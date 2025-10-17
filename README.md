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

## 2. Creación de la Maquina Virtual en azure

### 2.1 Accede al panel principal en:  
🔗 [https://portal.azure.com](https://portal.azure.com)
  
En el buscador superior escribe **“máquinas virtuales”**
luego le das en crear, y vuelves a seleccionar maquinas virtuales.
> **“Máquinas virtuales → Crear → Máquina virtual”** 

### 2.2 Configuración básica
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
| **Puertos publicos** | Permitir puertos seleccionados |
| **Puertos de entrada** | 22 (SSH), 80 (HTTP), 443 (HTTPS) |

### 2.3 Revisión y creación
Una vez completados los campos, Azure mostró un **resumen de la configuración**.  
Tras la validación, se pulsó **“Crear”**, iniciando el despliegue automático de la VM.

---

## 3. Configurar las reglas de red(NSG)

### 3.1 Selección del recurso
selecciona la maquina virtual → Redes → Configuración de red

---

## 4. 


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

    



