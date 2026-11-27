- **Alumno:** Lautaro Martín Casquet  
- **Bloque:** B1 — Entorno  
- **Fase / ejercicio:** 0120.1_1 · Actualización de material (Cole)  
- **Fecha de inicio:** 27/11/2026  
- **Fecha de entrega:** 27/11/2026  
  
---  
  
## ![🎯](https://fonts.gstatic.com/s/e/notoemoji/17.0/1f3af/32.png) Qué se pedía  
  
El profesor ha reorganizado el material del Bloque 1: las fichas de laboratorio están ahora en tres carpetas (`B1_Lab_VirtualBox`, `B1_Lab_HyperV` y `B1_Lab_Comun`). Como mi copia del repositorio era la vieja, había que tirarla y sacar una nueva desde el repositorio actualizado (`[https://www.google.com/url?q=http://github.com/sor-iesjj/bloque-1-entorno%60&source=gmail&ust=1795881998868000&sa=E](https://www.google.com/url?q=http://github.com/sor-iesjj/bloque-1-entorno%60&source=gmail&ust=1795881998868000&sa=E)): borrar mi repositorio en GitHub, borrar la carpeta local, crear uno nuevo con **Use this template**, clonarlo como `B1_Entorno` y comprobar que estaba bien.  
  
## ![⌨️](https://fonts.gstatic.com/s/e/notoemoji/17.0/2328_fe0f/32.png) Comandos y pasos importantes  
  
- **GitHub → Settings → Danger Zone → Delete this repository** — para borrar mi `bloque-1-entorno` viejo (pide escribir el nombre completo y confirmar la identidad con un código por correo).  
- **Use this template → Create a new repository** — en el repositorio del profesor, para crear el mío nuevo: nombre `bloque-1-entorno`, **Public**.  
- `cd Documents/` → `cd SOR/` → `cd Bóveda_SOR/01_Prácticas/` — para ir a la carpeta donde van las prácticas.  
- `ls -l` — para comprobar que `B1_Entorno` ya no estaba antes de clonar.  
- `git clone git@github.com:Lauta-Martin-SMR/bloque-1-entorno.git B1_Entorno` — para bajar el repositorio nuevo con el nombre de carpeta correcto.  
- `ls` — para ver que la carpeta `B1_Entorno` había aparecido.  
- `cd B1_Entorno/` y `git log --oneline -1` — para ver el último commit del repositorio nuevo.  
  
## ![🛠️](https://fonts.gstatic.com/s/e/notoemoji/17.0/1f6e0_fe0f/32.png) Qué he hecho  
  
1. Empecé la grabación con OBS, enseñé el Explorador y el enunciado de la tarea en Teams.  
2. Abrí mi repositorio viejo `bloque-1-entorno` en GitHub y comprobé que solo tenía el `Initial commit` de hace tres semanas, nada mío.  
3. Lo borré desde **Settings → Danger Zone → Delete this repository**. GitHub me pidió confirmar el acceso con un código enviado a mi correo. Después miré la lista de mis repositorios y ya no salía.  
4. Fui al repositorio actualizado del profesor (`sor-iesjj/bloque-1-entorno`), pulsé **Use this template → Create a new repository**, le puse de nombre `bloque-1-entorno`, lo dejé público y lo creé. El repositorio nuevo salió con las carpetas `99_Recursos`, `B1_Lab_Comun`, `B1_Lab_HyperV` y `B1_Lab_VirtualBox` y la marca "Generated from sor-iesjj/bloque-1-entorno".  
5. Cerré lo que tenía abierto y en el Explorador entré en `Documentos/SOR/Bóveda_SOR/01_Prácticas` y borré la carpeta `B1_Entorno`. En Obsidian comprobé que ya no aparecía.  
6. Copié la dirección SSH del repositorio nuevo (botón **Code**), abrí Git Bash, fui a `01_Prácticas` y con `ls -l` vi que solo quedaban `B2_Ubuntu_Local`, `bloque-0-prerequisitos` y `bloque-2-ubuntu-local`.  
7. Cloné el repositorio, la primera vez sin el segundo argumento (ver fallos) y la segunda con `B1_Entorno`. Con `ls` salió `B1_Entorno/`.  
8. Entré en `B1_Entorno` y con `git log --oneline -1` salió `3e3d9d8 (HEAD -> main, origin/main, origin/HEAD) Initial commit`.  
9. Por último abrí Obsidian, creé la nota `b1-actualizacion-material-cole` en `00_Apuntes/Trimestre_N/B1_Entorno/` y pegué las seis preguntas para contestarlas.  
  
## ![🚩](https://fonts.gstatic.com/s/e/notoemoji/17.0/1f6a9/32.png) Qué me ha fallado y cómo lo he resuelto  
  
- **Cloné sin el segundo argumento.** Lancé `git clone git@github.com:Lauta-Martin-SMR/bloque-1-entorno.git` y Git creó la carpeta `bloque-1-entorno`, que no es la que espera el curso. Borré esa carpeta en el Explorador y volví a clonar añadiendo `B1_Entorno` al final.  
- **`git log` fuera del repositorio.** Hice `git log --oneline -1` estando todavía en `01_Prácticas` y me salió `fatal: not a git repository (or any of the parent directories): .git`. Luego probé `cd bloque-` y me dijo `No such file or directory`, porque esa carpeta ya la había borrado. Lo resolví con `cd B1_Entorno/` y ahí `git log` ya funcionó.  
- **Confirmación de identidad en GitHub.** Al borrar el repositorio, GitHub me pidió un código por correo (*Confirm access*). No era un fallo, pero hay que tener el correo a mano.  
  
## ![🤔](https://fonts.gstatic.com/s/e/notoemoji/17.0/1f914/32.png) Respuestas a las preguntas  
  
1. **¿Qué tres carpetas tiene el repositorio nuevo y qué guarda cada una?** `B1_Lab_VirtualBox`, con las fichas de laboratorio que se hacen con VirtualBox; `B1_Lab_HyperV`, con las mismas prácticas pero hechas con Hyper-V; y `B1_Lab_Comun`, con las fichas que valen para los dos programas. Además está `99_Recursos` con material de apoyo.  
2. **¿Por qué el segundo argumento de `git clone` es obligatorio? ¿Qué habría pasado sin él?** Porque decide cómo se llama la carpeta en mi ordenador, y el curso (Obsidian, las rutas de las fases) espera que se llame `B1_Entorno`. Sin él, Git usa el nombre del repositorio y crea `bloque-1-entorno`. Me pasó en el vídeo: tuve que borrar esa carpeta y clonar otra vez.  
3. **¿Qué se puede deshacer: borrar la carpeta local o borrar el repositorio de GitHub?** Borrar la carpeta local, porque se vuelve a bajar con `git clone` mientras el repositorio siga en GitHub. Borrar el repositorio de GitHub no se puede deshacer: GitHub lo avisa en la Danger Zone ("there is no going back").  
4. **¿Con qué comando compruebas que estás en la versión nueva? ¿Qué tiene que decir la respuesta?** Con `git log --oneline -1` dentro de `B1_Entorno`. Según el enunciado, el último commit tiene que decir `2026-11-26`. A mí me salió `Initial commit`, porque Use this template crea el repositorio con un único commit nuevo; lo que demuestra que es la versión nueva es que aparecen las carpetas `B1_Lab_*`.  
5. **¿Qué es Use this template y en qué se diferencia de un fork?** Es un botón de GitHub que crea un repositorio nuevo en mi cuenta con una copia de los ficheros del original, pero sin su historial (empieza con un solo commit) y sin quedar enganchado a él. Un fork copia también todo el historial y sigue vinculado al original, para poder mandarle cambios con pull requests.  
6. **¿Había algo tuyo en el repositorio viejo? Si lo había, ¿dónde lo guardaste?** No. Antes de borrarlo comprobé que solo tenía el `Initial commit` del principio. Mis apuntes van en mi repositorio `apuntes-sor-t1`, no en el material del curso.  
  
## ![🔗](https://fonts.gstatic.com/s/e/notoemoji/17.0/1f517/32.png) Enlaces  
  
- **Vídeo de esta fase:** https://youtu.be/bBnUZc7zjLM
- **Playlist:** https://youtube.com/playlist?list=PLT4ip4N9IOZQ&si=2VwnrRMvITGqaS8C
- **Mi repositorio nuevo:** https://github.com/Lauta-Martin-SMR/bloque-1-entorno
