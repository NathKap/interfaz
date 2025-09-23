# ┏━━━━━☆*･｡ﾟ.ﾟ･*☆━━━━━┓
#  (⁄⁄•⁄ω⁄•⁄⁄)       🌸  ISC 🌸
# ┗━━━━━☆*･｡ﾟ.ﾟ･*☆━━━━━┛
#
# Asignatura : Lenguajes de Interfaz en TECNM Campus ITT
# Autor      : Garcia Hernandez Ana Gabriela
# Fecha      : 2025/09/23
#Codigo ✨🌈

DISPLAY_MODE = LCD_CMD_DISPLAY | LCD_CMD_DISPLAY_ON | LCD_CMD_DISPLAY_CURSOR | LCD_CMD_DISPLAY_CURSOR_BLINK

    lcc #LCD_INITIALIZE
    lcc #DISPLAY_MODE

.start:
    clra
    lcc #LCD_CMD_CLEAR
    data Ra, .tec
    call .printStr
    jmz

.printStr:
    mov Rc, Ra
.nextChar:
    lod Ra, Rc       ; cargar siguiente caracter
    tst Ra           ; verificar fin de cadena
    jz .done
    lcd Ra           ; mostrar caracter en el LCD
    inc Rc           ; avanzar puntero
    jmp .nextChar
.done:
    ret

.tec:
#d "TEC\0"

<img width="759" height="587" alt="image" src="https://github.com/user-attachments/assets/37e7dcd3-585e-4ebb-a732-34add1931fa3" />
<img width="770" height="571" alt="image" src="https://github.com/user-attachments/assets/17389f2d-84ac-43ee-9368-f248e2868642" />
<img width="758" height="581" alt="image" src="https://github.com/user-attachments/assets/644a1d1e-4107-438d-8443-192247682c35" />

