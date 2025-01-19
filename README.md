![purge_text](https://github.com/user-attachments/assets/54d95895-d824-4423-a56e-8de919599432)

<h1 align="center"></h1>

### ¿De qué trata el proyecto "PURGE - Ransomware"?

PURGE es un malware de tipo Ransomware programado en lenguaje Python, este tipo de software malicioso se distingue por bloquear el acceso a diversos recursos del sistema operativo infectado y, posteriormente, exigir un rescate a cambio de restaurar el acceso a dichos recursos. El proyecto es de uso privado y fue creado con el objetivo de concienciar a los usuarios sobre este tipo de ataques, a través de charlas informativas y demostraciones en vivo de la ejecución del Ransomware.

### Características de PURGE:

➤ **Algoritmo de cifrado:** Utiliza Fernet(AES), la misma clave que genera se usa para cifrar y descifrar la información. Permite cifrar grandes volúmenes de datos, a diferencia de RSA que usa dos keys y es más lento.

➤ **Extensiones:** ['.pdf', '.txt', '.png', '.csv', '.docx', '.doc', '.ppt', '.jpg', '.jpeg', '.xls', '.mp3', '.mp4', '.psd', '.html', '.mov', '.rar', '.db', '.sqlite', '.sql', '.mdb', '.accdb', '.myd', '.frm', '.dmp', '.ndf', '.mdf', '.py', '.php', '.perl', '.rb', '.c', '.cs', '.js', '.css', '.dat', '.asc', '.csr', '.RTF', '.uot', '.crt', '.DOT', '.pot', '.ots', '.std', '.xlt', '.jar', '.pas', '.cpp', '.ms11', '.sldm', '.sldx', '.ibd', '.bat', '.lay', '.asm', '.vbs', '.raw', '.cmd', '.zip', '.tar', '.vmdk', '.jsp', '.avi', '.file', '.mkv', '.mpg', '.aes', '.hash', '.class', '.fla']

➤ **Disablers:** Deshabilita la protección de Windows Defender, Firewall, UAC y procesos del sistema (taskmanager.exe, cmd.exe, regedit.exe). Desactiva varios puertos populares para evitar que el sistema pueda ser accedido de forma remota desde el exterior.

➤ **Killers:** Bloquea 18 tipos de navegadores para impedir que el usuario navegue mientras el Ransomware está en ejecución, y también deshabilita la interfaz de red para evitar la conexión a Internet.

➤ **Stealers:** Mediante requests silenciosas, PURGE descarga y ejecuta herramientas como Mimikatz, WiFi-Dumper y LaZagn en el directorio "C:\Windows\Temp", renombrándolas como "explorer.exe", "notepad.exe" y "calculator.exe" para pasar desapercibidas por el usuario.

➤ **UploadFiles:** Los resultados generados por las herramientas son cargados en el almacenamiento en la nube del atacante para su análisis. Posteriormente, tanto las herramientas como los archivos de salida se cifran con AES-256 y se eliminan del sistema de la víctima para cubrir las huellas del ataque.

➤ **Builder**: Cuenta con un builder para empaquetar el source code a un .EXE de forma automatizada.

➤ **Decrypt:** Por cada usuario, generá una llave para desencriptar la información.

➤ **Auto-Destruction:** Cuenta con un botón para eliminar toda la información en caso de que el usuario no quiera pagar el rescate.

➤ **Auto-Downloading:** Tiene la función de descargar un wallpaper y ponerlo de escritorio, así como también un mp3 que será reproducido una vez que encripte la información.


![2](https://github.com/user-attachments/assets/e41ba8e3-2887-4623-9faa-a1a2e27121f5)

![1](https://github.com/user-attachments/assets/108348a9-03d5-4dce-80ce-cf0db02f280f)

![3](https://github.com/user-attachments/assets/a7e7a939-aaba-4194-993c-bae5aea3467f)

![4](https://github.com/user-attachments/assets/333fad2e-71b3-4032-8121-8356c2600ec7)

</br>

<h1 align="center"></h1>

#### Desarrollador: ~R3LI4NT~
