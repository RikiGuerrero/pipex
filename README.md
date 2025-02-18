# pipex

![C Language](https://img.shields.io/badge/C-Programming-blue.svg) ![Makefile](https://img.shields.io/badge/Makefile-Build-orange.svg) ![Git](https://img.shields.io/badge/Git-Version%20Control-red.svg) ![Norminette](https://img.shields.io/badge/Norminette-Code%20Style-brightgreen.svg)

## 📌 Descripción

**pipex** es un proyecto de la escuela **42** cuyo objetivo es simular el comportamiento de una tubería (pipe) en Unix. El programa toma un archivo de entrada, aplica dos comandos secuenciales y redirige la salida a un archivo de salida, replicando el comportamiento de:
```bash
< archivo_entrada cmd1 | cmd2 > archivo_salida
```
Este proyecto permite profundizar en la programación de sistemas, la comunicación entre procesos y la gestión de redirecciones en Unix.

## 🛠 Lenguajes y Tecnologías

- **C**
- **Makefile**
- **Norminette**
- **Funciones del sistema Unix:**
  -  ``fork()``
  -  ``pipe()``
  -  ``dup2()``
  -   ``execve()``
  -   ``kill()``
  -   ``signal()``

## 💡 Conceptos de Programación Aplicados

- **Comunicación entre procesos:** Uso de ``pipe()`` para transmitir datos entre procesos.
- **Redirección de entrada y salida:** Manipulación de ``stdin`` y ``stdout`` mediante ``dup2()``.
- **Gestión de procesos:** Creación y sincronización de procesos con ``fork()`` y ``wait()``.
- **Señales:** Manejo de interrupciones y envío de señales con ``kill()`` y ``signal()``.

## 📂 Estructura del Proyecto

```
pipex
├── Makefile
├── README.md
├── includes
│   └── pipex.h
├── libft
│   ├── Makefile
│   ├── ft_putstr_fd.c
│   ├── ft_split.c
│   ├── ft_split2.c
│   ├── ft_strchr.c
│   ├── ft_strdup.c
│   ├── ft_strjoin.c
│   ├── ft_strlen.c
│   ├── ft_strncmp.c
│   └── libft.h
└── src
    ├── get_cmd_path.c
    ├── pipex.c
    └── utils.c
```

## 🚀 Instalación

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/RikiGuerrero/pipex.git
   cd pipex
2. Compilar el proyecto:
   ```bash
   make
   ```
3. Ejecuta el programa:
   ```bash
   ./pipex archivo_entrada "comando1" "comando2" archivo_salida
   ```
   Ejemplo:
   ```bash
   ./pipex input.txt "grep 42" "wc -l" output.txt
   ```
   Esto tomará ``input.txt``, filtrará las líneas que contienen "42" y contará las ocurrencias, guardando el resultado en ``output.txt``.

## 🎯 Ejemplo de Uso

Ejemplo de ejecución:
```bash
echo -e "Hola\n42\nMundo\n42" > input.txt
./pipex input.txt "grep 42" "wc -l" output.txt
cat output.txt
```
Salida esperada en ``output.txt``:
```bash
2
```

## ✅ Normas y Estilo de Código

El código sigue las reglas de la **Norminette**, la herramienta de estilo de 42. Para verificar:
```bash
norminette
```

## 📜 Licencia

Este proyecto es parte del currículo de 42 y sigue las reglas de la escuela.
