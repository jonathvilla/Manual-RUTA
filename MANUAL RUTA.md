<p>MANNUAL DE INSTALACION DE RUTA EN XUBUNTO 20.04</p>
<p>JONATH MERCADO LOZANO</p>
<p>INTELLIGENT ELECTRONIC SOLUTIONS</p>
<p>20121</p>
<h2 id="section"></h2>
<p><strong>1. REQUISITOS PARA LA INSTALACIÓN DE XUBUNTU 20.04.ISO</strong><br>
Imágen iso de xubunto 20.04.iso<br>
USB (debe estar formateada en formato fat 32)<br>
Balean Etcher (programa para bootear memoria usb)</p>
<h2 id="section-1"></h2>
<p><strong>2. DESCRAGA DE XUBUNTO 20.04.ISO</strong><br>
2.1 Vamos al siguiente link <a href="https://xubuntu.org/download/">https://xubuntu.org/download/</a> y elegimos el servidor más cercano un micaso united States.</p>
<p>2.2 Link de descarga de imagen xubuntu 20.04.iso</p>
<p>Una vez elegido nuestro servidor nos mostrará una ventana como lo muestra la imagen seleccionamos nuestra iso a descargar y empezará la descarga</p>
<p><a href="http://mirror.us.leaseweb.net/ubuntu-cdimage/xubuntu/releases/20.04/release/">http://mirror.us.leaseweb.net/ubuntu-cdimage/xubuntu/releases/20.04/release/</a></p>
<p><strong>3. DESCARGA DE BALENA ETCHER</strong><br>
Balena es un programa que nos permite bootear usb, descargamos el programa del siguiente link</p>
<p><a href="https://www.balena.io/etcher/">https://www.balena.io/etcher/</a>y damos clic en download</p>
<p><strong>3.1 crear booteable de xubuntu 20.04</strong><br>
Una vez tengamos el archivo extraido nos muestra una ventana donde<br>
Seleccionamos La iso y la usb<br>
una vez todo listo clic en flash par que el proceso de booteo empiece<br>
empezará a crear la usb booteable</p>
<h2 id="section-2"></h2>
<p><strong>4. INSTALACIÓN DE XUBUNTU 20.04</strong><br>
Reiniciamos el pc y presionamos las teclas indicadas <strong>(F11,F12, ESC)</strong> para elegir cómo queremos que arranque la máquina en nuestro caso será por medio de la usb para preparar la instalación de xubuntu 20.04</p>
<p>Damos enter y empieza a cargar los archivos</p>
<p>Empezamos a configurar, elegimos el idioma, en nuestro caso (español) y damos clic en instalar xubuntu<br>
configuramos nuestro teclado y clic en continuar</p>
<p>Clickeamos en descargar actualizaciones al instalar xubuntu y continuar</p>
<p>seleccionamos el tipo de instalación a utilizar en nuestro caso borrar disco e instalar xubuntu y damos clic en instalar ahora</p>
<p>nos muestra una pantalla emergente damos clic en continuar</p>
<p><strong>NOTA:</strong> Es importante siempre leer antes de ejecutar cualquier accion</p>
<p>Configuramos nuestra ubicación y clic en continuar<br>
Configuramos nuestras credenciales y clic en continuar<br>
Comenzara la instalacion del SO XUBUNTU 20.04</p>
<p>Reiniciamos nuestro equipo damos clic en reiniciar ahora</p>
<p>Cuando se haya reiniciado nuestro equipo nos pedirá que retiremos la memoria y le damos clic en la tecla enter</p>
<p>Una vez hecho todo esto tendremos instalado xubuntu 20.04 en nuestra máquina</p>
<h2 id="section-3"></h2>
<p><strong>5. INSTALACIÓN DE OPENBOX</strong></p>
<p><strong>5.1 Openbox</strong><br>
Es un entorno de escritorio liviano y vacío el cual nos permite manejar mejor nuestrorecursos</p>
<p><strong>5.2 Obconf</strong><br>
Es un programa creado para openbox nos permitirá no sólo configurar las ventanas de openboxsino que también podremos instalar temas para el gestor de ventanas o configurar los lanzadores</p>
<p><strong>5.3 Instalando openbox</strong><br>
instalamos nuestro entorno de escritorio openbox con el comando <strong><code>sudo apt-get install openbox obconf</code></strong> y nos instala obconf con el mismo comando</p>
<p>una vez instalado openbox cerramos sesión y no mostrará una ventana en donde  seleccionaremos nuestro entorno openbox</p>
<p>cuando ingresemos a openbox nos mostrará una ventana vacía  para encontrar nuestros programas clic derecho y nos desplegara una ventana donde podemos seleccionar nuestras herramientas de trabajo y tendríamos openbox listo para trabajar</p>
<h2 id="section-4"></h2>
<p><strong>6. DESINSTALAR ENTORNOS GRÁFICOS</strong></p>
<p>Una vez instalado openbox desinstalamos los otros entornos gráficos que trae xubuntu por defecto, nos quedamos solo con openbox esto lo hacemos para liberar recursos</p>
<p><strong>6.1 Desinstalar libxfce4util</strong></p>
<p>desinstalamos el entorno gráfico que trae por defecto xubuntu con el siguiente comando<br>
<strong><code>sudo apt-get purge libxfce4util-common</code></strong></p>
<h2 id="section-5"></h2>
<p><strong>7. INSTALAR PCMANFM</strong><br>
Instalamos pcmanfm con el comando <strong><code>sudo aptitude install pcmanfm</code></strong></p>
<h2 id="section-6"></h2>
<p><strong>8. INSTALAR LIGHTDM</strong><br>
Instalamos lightdm con el comando <strong><code>sudo aptitude install lightdm</code></strong></p>
<h2 id="section-7"></h2>
<p><strong>9. VERIFICAMOS LOS PERMISOS DE SUDOERS</strong><br>
Verificar que el archivo de sudoers tenga los permisos correctos, ingresar a <strong><code>sudo nano /etc/sudoers</code></strong> control O para guardar y control X para volver al terminal</p>
<h2 id="section-8"></h2>
<p><strong>10. AUTO LOGIN</strong></p>
<p>Ingresar al archivo lightdm.conf con el comando <strong><code>sudo nano /etc/lightdm/lightdm.conf</code></strong> y colocamos las dos líneas siguiente, esto es con el fin que al iniciar no pida usuario y contraseña<br>
autologin-user = ruta<br>
autologin-user-timeout=0</p>
<h2 id="section-9"></h2>
<p><strong>11. INSTALAR x11-xserver-utils</strong></p>
<p>Instalamos el x11-xserver-utils con el siguiente comando <strong><code>sudo aptitude install x11-xserver-utils</code></strong></p>
<h2 id="section-10"></h2>
<p><strong>12. INGRESAR A RULES.D</strong></p>
<p>Ingresamos a la carpeta 10_es.rules con el siguiente comando <strong><code>cd /etc/udev/rules.d</code></strong> una vez parado en la ruta colocamos el siguiente comando <strong><code>sudo nano 10\_ies.rules</code></strong><br>
Una vez ingresado al archivo 10 ies.rules pegamos la siguiente instrucción<br>
guardamos con la instrucción (control O y control x para volver a la terminal)</p>
<pre><code>KERNEL==&amp;quot;js\*&amp;quot;, SUBSYSTEM==&amp;quot;input&amp;quot;, ATTRS{idVendor}==&amp;quot;0079&amp;quot;, ATTRS{idProduct}==&amp;quot;0006&amp;quot;, SYMLINK+=&amp;quot;ies/key%n&amp;quot;, MODE:=&amp;quot;0666&amp;quot;
</code></pre>
<h2 id="section-11"></h2>
<p><strong>13. INSTALAR DOCKER ENGINE</strong></p>
<p>Instalamos docker para el manejo de contenedores e imágenes de nuestra aplicación</p>
<p><strong>13.1 verificar versiones de docker</strong></p>
<p>verificamos que no tengamos ninguna versión de docker para cuando instalemos no tengamos problemas con la instalación.<br>
actualizamos con el comando <strong><code>sudo apt-gte update</code></strong></p>
<p>Una vez actualizado preparamos la instalación de nuestro repositorio con el comando.</p>
<pre><code>(sudo apt-get install \
apt-transport-https \
ca-certificates \
curl \
gnupg \
lsb-release)
</code></pre>
<p>debemos instalar la clave oficial de docker con el siguiente comando.</p>
<pre><code>**curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg`**
</code></pre>
<p>Con el siguiente comando configuramos el repositorio estable para agregar el repositorio de prueba</p>
<pre><code>echo \
&amp;quot;deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \**
$(lsb\_release -cs) stable&amp;quot; | sudo tee /etc/apt/sources.list.d/docker.list \&amp;gt; /dev/null
</code></pre>
<p>Actualizamos nuevamente con el comando <strong><code>sudo apt-get update</code></strong> para poder instalar docker</p>
<p>Con el siguiente comando <strong><code>sudo apt-get install docker-ce docker-ce-cli containerd.io</code></strong><br>
instalamos docker</p>
<h2 id="section-12"></h2>
<p><strong>14. INSTALACIÓN DE DOCKER COMPOSE</strong></p>
<p>Con el siguiente comando instalamos la versión actual de docker compos</p>
<pre><code>sudo curl -L &amp;quot;https://github.com/docker/compose/releases/download/1.29.0/docker-compose-$(uname -s)-$(uname -m)&amp;quot; -o /usr/local/bin/docker-compose
</code></pre>
<p>Con el siguiente comando damos los permiso al ejecutables <strong><code>sudo chmod +x /usr/local/bin/docker-compose</code></strong></p>
<h2 id="section-13"></h2>
<p><strong>15. INSTALACIÓN DE Qt5.9.2</strong><br>
Descargamos qt de la página oficial<br>
<a href="https://www.qt.io/download-qt-installer?hsCtaTracking=99d9dd4f-5681-48d2-b096-470725510d34%7C074ddad0-fdef-4e53-8aa8-5e8a876d6ab4">https://www.qt.io/download-qt-installer?hsCtaTracking=99d9dd4f-5681-48d2-b096-470725510d34%7C074ddad0-fdef-4e53-8aa8-5e8a876d6ab4</a><br>
damos clic en download.</p>
<p>Guardamos nuestro archivo dando clic en save file y aceptar</p>
<p>Con el siguiente comando  <strong><code>sudo chmod +x qt-unified-linux-x64-4.1.0-online.run</code></strong> damos los permisos de ejecución para que se pueda ejecutar correctamente qt.</p>
<p>con el siguiente comando <code>./ qt-unified-linux-x64-4.1.0-online.run</code>ejecutamos el archivo para que comience su instalación.<br>
Una vez ejecutado el comando nos muestra una ventana donde le daremos el correo y contraseña<br>
damos clic en <strong>i have read</strong> y clic en next.</p>
<p>Damos clic en <strong>help</strong> y next para continuar</p>
<p>Le damos la ruta <strong>/home/ruta/Documents/qt</strong> que deseamos para el proyecto, seleccionamos continuar instalación y clic en next</p>
<p>Le damos clic en archive y clic en <strong>filter</strong> esto con el fin de filtrar los archivos del programa, clic en next<br>
Nos muestra una ventana en  donde se despliega qt<br>
Seleccionamos <strong>qt 5.9.2</strong> y clic en next<br>
Clic en <strong>have reade</strong> y clic en next</p>
<p>Luego damos clic en <strong>install</strong> para iniciar la instalación de qt</p>
<p>Se despliega una barra de carga en donde mostrara el avance esto  tardará unos minutos</p>
<h2 id="section-14"></h2>
<p><strong>16. INSTALACIÓN DE mysql-client</strong><br>
Ejecutamos el comando <strong><code>sudo apt-get install mysql-client</code></strong> para instalar mysql-clien<br>
Descargamos la librería <strong>libmysqlclient</strong><br>
se descargara automáticamente colocando la siguiente ruta en nustro navegador.<br>
<a href="https://repo.mysql.com/apt/ubuntu/pool/mysql-5.7/m/mysql-community/libmysqlclient20_5.7.33-1ubuntu18.04_amd64.deb">https://repo.mysql.com/apt/ubuntu/pool/mysql-5.7/m/mysql-community/libmysqlclient20_5.7.33-1ubuntu18.04_amd64.deb</a></p>
<p>una vez descargado el paquete verificamos con el comando <strong><code>ls</code></strong> y la ejecutamos con el comando <strong><code>sudo dpkg -i libmysqlclient20\_5.7.33-1ubuntu18.04\_amd64.deb</code></strong></p>
<p>Actualizamos con el comando <strong><code>sudo apt-get update</code></strong></p>
<p>Instalamos libmysqlclient20 deb package con el comando<br>
<strong><code>sudo apt-get install libmysqlclient20</code></strong></p>
<h2 id="section-15"></h2>
<p><strong>17. INSTALAR PSMISC</strong></p>
<p>Instalamos psmisc con el comando <strong><code>sudo aptitude install psmisc</code></strong></p>
<p><strong>18. DAR PERMISOS DE EJECUCIÓN</strong><br>
Le damos permiso de ejecución a los archivo para no tener problemas ala hora de ejecutar nuestra aplicación<br>
<strong>18.1 Permisos de ejecución para los archivos libICT_bill.s*</strong><br>
Le damos los permiso de ejecución con el siguiente comando <strong><code>sudo chmod +x libICT\_Bill.s\*</code></strong><br>
una vez tengan los permisos los ubicamos en la siguiente ruta <strong>/usr/lib/ con el comando cd /usr/lib/</strong><br>
verificamos con el siguiente comando <strong>ls -l</strong> que pertenezcan al usuario root</p>
<p><strong>18.2 Permisos a la carpeta kbitech_ICT</strong><br>
Le damos todo los permisos a la carpeta <strong>kbitech_ICT</strong> con el comando sudo <strong><code>chmod 777 kbitech\_ICT</code></strong><br>
ubicamos la carpeta <strong>kbitech_ICT</strong> en la siguiente ruta con el comando sudo <strong><code>mv kbitech\_ICT /usr/include</code></strong><br>
Verificamos que la carpeta <strong>kbitech_ICT</strong> pertenezca a root en grupo y propietario con el siguiente comando<br>
<strong><code>ls -l</code></strong></p>
<p><strong>18.3 Instalar alsa-utils</strong><br>
Instalamos <strong>alsa-utils</strong> con el comando <strong><code>sudo apt-get install alsa-utils</code></strong><br>
<strong>18.4 Instalar alsamixer</strong></p>
<p>Instalamos alsamixer con el siguiente comando sudo <strong><code>apt-get install alsamixer</code></strong></p>
<h2 id="section-16"></h2>
<p><strong>19. ARCHIVOS AUTOSTART</strong><br>
En este archivo es donde se ejecuta los permisos de nuestra aplicación</p>
<p><strong>19.1 ubicación de archivo autostart</strong><br>
Ubicamos el archivo autostart en la ruta <strong>.config/openbox</strong> si la carpeta openbox no existe la creamos con el comando <strong><code>sudo mkdir openbox</code></strong><br>
Una vez en la ruta le damos los permisos de ejecución con el comando <strong><code>sudo chmod +x autostart</code></strong><br>
Ubicamos la carpeta RUTA en <strong>/home/ruta</strong> y verificamos los permisos grupo y propietarios sea ruta</p>
<p><strong>19.2 Ejecutar comandos</strong><br>
Una vez ubicada la carpeta ruta corremos los siguientes comandos<br>
<strong><code>chmod +x /home/ruta/RUTA/\*/\*.x86\_64</code></strong><br>
<strong><code>chmod 777 /home/ruta/RUTA/\*/\*/\*/\*.xml</code></strong></p>
<p><strong>19.3 Crear carpeta db</strong><br>
crear la carpeta db en <strong>/home/ruta/RUTA/</strong> y correr el siguiente comando <strong><code>sudo chown -R 999:docker db</code></strong></p>
<p><strong>20. MANAGER, COMFIGURACION, GENERICMODALS, DOCKER-CLEAN</strong><br>
Ubicamos los siguientes archivos(manager, comfiguracion, genericmodals, docker-clan) en la siguiente ruta <strong>/usr/local/bin</strong> con el comando <strong>s<code>udo mv manager configuracion genaricModals docker-clean</code></strong> y le damos permisos de ejecución, además de verificar que sean del grupo y propietario del usuario ruta y<br>
verificamos que los archivos están en la ruta correcta con el comando <strong><code>ls -l</code></strong></p>
<h2 id="section-17"></h2>
<p><strong>21. INSTALACION DE LIBRERIAS</strong><br>
Es necesario instalar las siguientes librerías para el funcionamiento de ruta,estas librerías se instalan una a una con los siguientes comandos.</p>
<ul>
<li><strong><code>sudo aptitude install libqt5printsupport5</code></strong></li>
<li><strong><code>sudo aptitude install libqt5serialport5</code></strong></li>
<li><strong><code>sudo aptitude install libqt5websockets5</code></strong></li>
<li><strong><code>sudo aptitude install libqt5sql5</code></strong></li>
<li><strong><code>sudo aptitude install libqt5quick5</code></strong></li>
<li><strong><code>sudo aptitude install qml-module-qtmultimedia</code></strong></li>
<li><strong><code>sudo aptitude install qml-module-qtquick-window2</code></strong></li>
</ul>
<h2 id="section-18"></h2>
<p><strong>22. MOVER ARCHIVO tty_enable.sh</strong><br>
Movemos el siguiente <strong>archivo tty_enable.sh</strong> con el comandosudo <strong><code>mv archivo tty\_enable.sh /usr/bin/</code></strong> a la ruta /usr/bin dar permisos de ejecución y verificar que pertenezca al usuario root<br>
damos los permisos con el comando <strong><code>sudo chmod +x archivo tty\_enable.sh</code></strong></p>
<p>verificamos que pertenezcan al a usuario root en caso de que no pertenezcan lo cambiamos con el comando <strong><code>sudo chown root:root ttys-enable.sh</code></strong></p>
<p><strong>23. MOVER SERVICIO tty-enable.service</strong><br>
Movemos el siguiente servicio a la ruta <strong>/etc/systemd/system</strong>/ le damos permisos de ejecución y verificamos que pertenezca al usuario root<br>
le damos los permisos con el comando <strong><code>sudo chmod +x ttys-enable.service</code></strong></p>
<p>Verificamos los permiso y que pertenezca al usuario root en caso de que no pertenezca lo cambiamos con el comando <strong><code>sudo chown root:root enable.service</code></strong></p>
<p><strong>23.1 HABILITAR SERVICIO PARA ttys-enable.service</strong><br>
Habilitamos el servicio con el siguiente comando <strong><code>sudo systemctl enable ttys-enable.service</code></strong></p>
<p><strong>23.2 COMENZAR EL SERVICIO</strong><br>
Comenzamos el servicio con el siguiente comando <strong>s<code>udo systemctl start ttys-enable.service</code></strong></p>
<h2 id="section-19"></h2>
<p><strong>24. MOVER ARCHIVO billetero.ini</strong></p>
<p>movemos el archivo billetero.ini a la ruta <strong>etc/ruta</strong> con el comando <strong><code>sudo mv billetero.ini /etc/ruta</code>,</strong> en caso de que no es te la carpeta ruta la creamos con el comando <strong><code>sudo mkdir ruta</code></strong></p>
<p>le damos los permisos con el comando <strong><code>sudo chmod 777 billetero.ini</code></strong></p>
<h2 id="section-20"></h2>
<p><strong>25. UBICAR ARCHIVO <a href="http://autoverificacion.sh">autoverificacion.sh</a></strong></p>
<p>Ubicamos el archivo <strong><a href="http://autoverificacion.sh">autoverificacion.sh</a></strong> en la ruta <strong>/usr/bin</strong> con el siguiente comando<br>
<strong><code>sudo mv autoverificacion.sh /usr/bin</code>,</strong> Verificar que pertenezca a el usuario y grupo root y que tenga permisos de ejecución</p>
<h2 id="section-21"></h2>
<p><strong>26. ARCHIVO CROMTAB</strong><br>
Ingresamos al archivo cromtab con el siguiente comando <strong><code>sudo nano /etc/crontab</code></strong> y colocamos el siguiente texto en la última línea<br>
<strong>01 * * * * root find /RUTA/Screenshots/* -mtime +1 -delete</strong></p>
<h2 id="section-22"></h2>
<p><strong>27. VERIFICAR PROPIETARIO Y GRUPO DE LA CARPETA DOCUMENST</strong><br>
verificamos que la carpeta Documents tenga propietario y grupo al usuario ruta</p>
<p><strong>28. GENERAR CARPETA IMAGENES</strong></p>
<p>Generamos la carpeta imágenes con el comando <strong><code>mkdir imágenes</code></strong> en la ruta <strong>home/RUTA</strong></p>
<p><strong>29. GENERAR Y MONTAR CONTENEDORES</strong><br>
Nos ubicamos en la ruta /home/ruta/Documents/docker/ con el comando<br>
<strong><code>cd /home/ruta/Documents/docker/</code></strong> y corremos los siguientes comandos</p>
<p><strong><code>sudo docker-compose -f docker-compose.yml build</code></strong><br>
<strong><code>sudo docker-compose -f docker-compose.yml up -d</code></strong></p>
<p><strong>30. INSTALACION DE ANYDESK</strong><br>
Entramos en la página oficial de anydesk y seleccionamos la versión que necesitamos o la mas actual<br>
la descargamosde siguinte link. <a href="https://anydesk.softonic.com/">https://anydesk.softonic.com/</a><br>
Abrimos la terminal y ejecutamos el siguiente comando <strong><code>sudo dpkg -i anydesk</code></strong><br>
Nos saldrá un error al preparar los paquetes de anydesk con el siguiente comando lo solucionaremos<br>
este comando nos permite descargar los paquetes necesarios para la instalación.<br>
<strong><code>sudo apt install -f -y</code></strong><br>
Con el comando anterior al ejecutarlo tendremos listo anydesk</p>

