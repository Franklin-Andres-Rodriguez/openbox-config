# Documentación Completa de la Configuración del Sistema de h4ckio

Esta documentación detalla la configuración actual del sistema basado en Openbox utilizada por h4ckio, destacando sus componentes, herramientas, personalizaciones y medidas de seguridad aplicadas para mantener un entorno minimalista, eficiente y seguro.

---

## 1. Sistema Operativo Base
El usuario utiliza una distribución basada en **Lubuntu**, reemplazando su entorno de escritorio tradicional por el gestor de ventanas minimalista **Openbox**.

### Motivación para el Cambio a Openbox
- El usuario prefiere un entorno de trabajo minimalista y altamente configurable.
- Evita el uso de entornos de escritorio completos para reducir el consumo de recursos.
- Prioriza la seguridad, estabilidad y flexibilidad del sistema.

### Pasos para Instalar Lubuntu y Configurar Openbox
1. Descarga la ISO de Lubuntu desde [lubuntu.me](https://lubuntu.me/).
2. Realiza una instalación mínima de Lubuntu.
3. Instala Openbox:
   ```bash
   sudo apt update
   sudo apt install openbox obconf
   ```

---

## 2. Gestor de Ventanas: Openbox
El sistema está configurado para utilizar **Openbox** como un gestor de ventanas puro, sin un entorno de escritorio completo ni complementos adicionales innecesarios.

### Características de Openbox en la Configuración
- Configuración minimalista.
- Uso de combinaciones de teclas personalizadas para gestionar ventanas y aplicaciones.
- Evita paneles o docks.
- Priorización de estabilidad y funcionalidad sin comprometer la seguridad.

### Archivos de Configuración de Openbox
- `~/.config/openbox/autostart`: Archivo para iniciar aplicaciones automáticamente.
- `~/.config/openbox/rc.xml`: Configuración principal de Openbox.
- `~/.config/openbox/menu.xml`: Menú de aplicaciones de Openbox.

---

## 3. Herramientas y Utilidades Instaladas
El entorno del usuario incluye las siguientes herramientas principales para la gestión del sistema:

### 3.1 Terminal y Shell
- **Kitty**: Terminal avanzada altamente configurable.
  - Instalación:
    ```bash
    curl -L https://sw.kovidgoyal.net/kitty/installer.sh | sh /dev/stdin
    ```
  - El directorio `$HOME/.local/kitty.app/bin` está añadido a la variable de entorno `$PATH`.
  - Personalización de colores en carpetas y archivos mediante **LS_COLORS**:
    ```bash
    export LS_COLORS='di=1;34:fi=0:ln=1;36:pi=1;33:so=1;35:bd=1;33:cd=1;33:or=1;31:mi=1;31:ex=1;32:*.pdf=1;31'
    ```
    Esto permite mostrar las carpetas en color azul, los archivos ejecutables en verde, y los archivos PDF en rojo, mejorando la visibilidad en la terminal.

- **Zsh**: Shell interactiva con características avanzadas.
  - Instalación:
    ```bash
    sudo apt install zsh
    ```
  - Personalización con **power10k**:
    ```bash
    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
    echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
    ```

### 3.2 Administrador de Ventanas
- **Openbox**: Personalizado para ser altamente eficiente y sin distracciones.

### 3.3 Herramientas de Productividad
- **sxhkd**: Administrador de atajos de teclado simple y rápido para gestionar combinaciones de teclas personalizadas.
  - Instalación:
    ```bash
    sudo apt install sxhkd
    ```
- **Picom**: Compositor ligero para manejar efectos de transparencia y sombras.
  - Instalación:
    ```bash
    sudo apt install picom
    ```
- **feh**: Utilidad ligera para establecer fondos de pantalla.
  - Instalación:
    ```bash
    sudo apt install feh
    ```
- **Unclutter**: Herramienta para ocultar automáticamente el puntero del ratón cuando no está en uso.
  - Instalación:
    ```bash
    sudo apt install unclutter
    ```

---

## 4. Configuración de Inicio de Sesión
El usuario evita el uso de TTY y prefiere utilizar un **gestor gráfico de inicio de sesión** que sea ligero y seguro.

### Instalación de LightDM (opcional)
```bash
sudo apt install lightdm lightdm-gtk-greeter
```

---

## 5. Configuración Personalizada de la Terminal
### Power10k
- Utilizado para personalizar el aspecto de la terminal.
- Incluye fuentes y colores personalizados para mejorar la legibilidad y la estética.

---

## 6. Personalización del Sistema
El usuario ha realizado las siguientes personalizaciones clave:
- **Atajos de teclado personalizados** mediante **sxhkd**.
- **Temas y estilos de Openbox** configurados manualmente para mantener un aspecto minimalista y profesional.
- **Fondo de pantalla** gestionado con **feh**.

---

## 7. Recomendaciones para Mantener y Mejorar la Configuración
- **Revisar periódicamente las configuraciones de la terminal y los colores personalizados.**
- **Mantener actualizadas las herramientas clave (Kitty, Picom, etc.).**
- **Explorar opciones adicionales para mejorar la gestión de atajos de teclado y scripts automatizados.**
- **Documentar los scripts personalizados y configuraciones clave.**

---

## 8. Configuración de Variables de Entorno
El directorio específico de Kitty ha sido añadido a la variable de entorno PATH:
```bash
export PATH="$HOME/.local/kitty.app/bin:$PATH"
```
Esto permite ejecutar **Kitty** desde cualquier ubicación en la terminal.

---

## 9. Consideraciones de Seguridad
- Evitar el uso de aplicaciones innecesarias que puedan introducir vulnerabilidades.
- Priorizar herramientas ligeras y bien mantenidas por la comunidad.

---

## 10. Conclusión
La configuración del sistema de h4ckio está diseñada para ser minimalista, segura y eficiente. Con Openbox como gestor de ventanas y herramientas como Kitty, Zsh y Picom, el entorno es altamente personalizable y se adapta perfectamente a las necesidades del usuario.

Se recomienda continuar optimizando las configuraciones y documentar cualquier cambio significativo para mantener la coherencia y la seguridad del sistema.

