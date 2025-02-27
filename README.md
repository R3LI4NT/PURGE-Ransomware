<p align="center">
  <img src="https://github.com/user-attachments/assets/54d95895-d824-4423-a56e-8de919599432" alt="Purge Logo" Logo" />
</p>

<p align="center">
    <a href="https://python.org">
    <img src="https://img.shields.io/badge/Python-3-green.svg">
  </a>
    <img src="https://img.shields.io/badge/Release-1.3-blue.svg">
  </a>
    <img src="https://img.shields.io/badge/Private-%F0%9F%94%92-red.svg">
  </a>
</p>

<h1 align="center"></h1>

### ¿De qué trata el proyecto "PURGE - Ransomware"?

PURGE es un malware de tipo Ransomware programado en lenguaje Python, este tipo de software malicioso se distingue por bloquear el acceso a diversos recursos del sistema operativo infectado y, posteriormente, exigir un rescate a cambio de restaurar el acceso a dichos recursos. El proyecto es de uso **privado** y fue creado con el objetivo de desarrollar un malware de alto nivel utilizando Python, sin ningún fin malicioso ni de causar daño, sino con fines de investigación.

Python es un lenguaje de programación muy potente, gracias a la gran variedad de bibliotecas y módulos disponibles. Sin embargo, no está diseñado específicamente para la creación de malware, a diferencia de lenguajes como C o C++, que tienen un control más directo sobre el sistema operativo. 

<h1 align="center"></h1>

### Características de PURGE `1.3`:

- [x] **Encriptación:** La clave AES es cifrada con la clave privada RSA para mayor seguridad, se envían al atacante.

- [x] **Descifrador GUI:** Se cuenta con un descifrador para recuperar la clave AES. El .exe es enviado a la víctima junto con la clave privada luego de pagar el rescate.

- [x] **C&C Discord:** Se implementó un bot oficial de Purge como comando de control, que selecciona los archivos confidenciales y los envía al canal de Discord controlado por el atacante.

- [x] **Stealers agregados:**
- __Keylogger:__ Registra las pulsaciones del teclado y envía los logs cada 5 minutos al servidor del atacante.
- __System Dumper:__ Enumera toda la información del sistema operativo (incluyendo hardware) + GeoIP para luego ser enviada al servidor del atacante.
- __SessionGopher:__ Extrae información de sesiones guardadas de herramientas como WinSCP, PuTTy, SuperPuTTy, RDP Microsoft para luego ser enviada al servidor del atacante.

- [x] **Ejecución remota:** Uso de PAExec para ejecutar comandos remotos en el sistema infectado. PAExec es una modificación de PaExec, siendo indetectable en varios antivirus.

- [x] **Eliminación de backups:** Deshabilita mecanismos de recuperación de Windows, cifra con AES-256 (sin almacenarse, lo que impide la recuperación) y destruye particiones.

- [x] **Sobreescribe MBR:** Eliminación de opción "Modo Seguro", bloquea bcdedit para impedir modificaciones en el arranque (BCD), desactiva la recuperación del sistema y restauración de Windows, manipula Winlogon para afectar el comportamiento de inicio de sesión. Al presionar el botón DESTRUCTION, el MBR se sobrescribe con los primeros 512 bytes del disco, lo que impide que el sistema pueda arrancar.

- [x] **Empaquetado UPX/UPX-Patcher:** Evadir detección de antivirus, dificulta el análisis estático y reversing, ofuscación básica.

<h1 align="center"></h1>

### Características de PURGE `1.2`:

- [x] **Algoritmo de cifrado:** Utiliza Fernet(AES), la misma clave que genera se usa para cifrar y descifrar la información. Permite cifrar grandes volúmenes de datos, a diferencia de RSA que usa dos keys y es más lento.

- [x] **Extensiones:** ['.pdf', '.txt', '.png', '.csv', '.docx', '.doc', '.ppt', '.jpg', '.jpeg', '.xls', '.mp3', '.mp4', '.psd', '.html', '.mov', '.rar', '.db', '.sqlite', '.sql', '.mdb', '.accdb', '.myd', '.frm', '.dmp', '.ndf', '.mdf', '.py', '.php', '.perl', '.rb', '.c', '.cs', '.js', '.css', '.dat', '.asc', '.csr', '.RTF', '.uot', '.crt', '.DOT', '.pot', '.ots', '.std', '.xlt', '.jar', '.pas', '.cpp', '.ms11', '.sldm', '.sldx', '.ibd', '.bat', '.lay', '.asm', '.vbs', '.raw', '.cmd', '.zip', '.tar', '.vmdk', '.jsp', '.avi', '.file', '.mkv', '.mpg', '.aes', '.hash', '.class', '.fla']

- [x] **Disablers:** Deshabilita la protección de Windows Defender, Firewall, UAC y procesos del sistema (taskmanager.exe, cmd.exe, regedit.exe). Desactiva varios puertos populares para evitar que el sistema pueda ser accedido de forma remota desde el exterior.

- [x] **Killers:** Bloquea 18 tipos de navegadores para impedir que el usuario navegue mientras el Ransomware está en ejecución, y también deshabilita la interfaz de red para evitar la conexión a Internet.

- [x] **Stealers:** Mediante requests silenciosas, PURGE descarga y ejecuta herramientas como Mimikatz, WiFi-Dumper y LaZagn en el directorio "C:\Windows\Temp", renombrándolas como "explorer.exe", "notepad.exe" y "calculator.exe" para pasar desapercibidas por el usuario.

- [x] **UploadFiles:** Los resultados generados por las herramientas son cargados en el almacenamiento en la nube del atacante para su análisis. Posteriormente, tanto las herramientas como los archivos de salida se cifran con AES-256 y se eliminan del sistema de la víctima para cubrir las huellas del ataque.

- [x] **Builder**: Cuenta con un builder para empaquetar el source code a un .EXE de forma automatizada.

- [x] **Decrypter:** Por cada usuario, generá una llave para desencriptar la información.

- [x] **Auto-Destruction:** Cuenta con un botón para eliminar toda la información en caso de que el usuario no quiera pagar el rescate.

- [x] **Auto-Downloading:** Tiene la función de descargar un wallpaper y ponerlo de escritorio, así como también un mp3 que será reproducido una vez que encripte la información.

<h1 align="center"></h1>

#### Mensaje de Rescate ~ GUI

![2](https://github.com/user-attachments/assets/e41ba8e3-2887-4623-9faa-a1a2e27121f5)

![3](https://github.com/user-attachments/assets/108348a9-03d5-4dce-80ce-cf0db02f280f)

#### Archivos encriptados

![4](https://github.com/user-attachments/assets/a7e7a939-aaba-4194-993c-bae5aea3467f)

#### Ejecución de stealers ~ Drive

![5](https://github.com/user-attachments/assets/5ffbff24-9fa3-44bb-84fd-f1934855941e)

#### Descifrador de clave AES

![6](https://github.com/user-attachments/assets/9fe75a29-2c93-41f1-8466-6af45b987fbc)

#### MBR Sobreescrito

![7](https://github.com/user-attachments/assets/f7f1178a-16b5-4e38-bcb1-e43f2c68a417)

#### Panel de control ~ Discord

https://github.com/user-attachments/assets/f37e769f-a0ec-4e90-9733-2e6958f6cd47

</br>

<h1 align="center"></h1>

> [!CAUTION]
> Al utilizar este software, usted acepta los términos y condiciones establecidos. En consecuencia, cualquier uso indebido de este software será de exclusiva responsabilidad del usuario final, y no del autor. Este proyecto tiene como objetivo inicial demostrar las capacidades de Python como herramienta para el desarrollo de malware en entornos controlados. Tradicionalmente, lenguajes como C y C++ se utilizan para crear este tipo de software.

⬇️ **Download:**  

<h1 align="center"></h1>

<h4 align="center">PURGE continúa mejorando...</h4>

<h1 align="center"></h1>

#### Developer: ~R3LI4NT~
