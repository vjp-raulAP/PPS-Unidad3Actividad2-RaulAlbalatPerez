# PPS-Unidad3Actividad2-RaulAlbalatPerez
Unidad 3 - Actividad 2. Detección de equipos, puertos, servicios,vulnerabilidades.
---
## ACTIVIDADES A REALIZAR
- Busca información de:
  - Como podemos obtener información pública con protocolo whois, web DoaminTools y DSNrecon.
    Información pública: `whois`, DomainTools y `dnsrecon`

    - **WHOIS**: Es una herramienta que permite consultar información sobre el propietario de un dominio o una dirección IP.
        **Comando WHOIS** (en Kali o Linux):

    ```bash
    whois [dominio_o_ip]
    ```
    - **DomainTools**: Plataforma en línea que proporciona información detallada sobre dominios, como registros históricos, propietarios, etc. Puedes buscar en [https://www.domaintools.com/](https://www.domaintools.com/).

    - **DNSRecon**: Herramienta para obtener información de registros DNS de un dominio. Algunos comandos básicos:

    ```bash
    dnsrecon -d [dominio]
    ```

- Cómo podemos utilizar Nmap y nikto,   para buscar equipos, puertos abiertos, servicios, vulnerabilidades.
 - **Nmap**: Herramienta para escanear puertos, identificar servicios y detectar vulnerabilidades. Algunos ejemplos de comandos:
    - Escaneo básico de puertos:
        ```bash
        nmap [IP o dominio]
        ```
    - Escaneo de puertos con detección de servicios:
        ```bash
        nmap -sV [IP o dominio]
    - Detección de sistema operativo:
        ```bash
        nmap -O [IP o dominio]
        ```
    - Escaneo de vulnerabilidades con scripts de Nmap (ver más abajo).
  
- **Nikto**: Escáner de vulnerabilidades web para identificar configuraciones incorrectas y vulnerabilidades comunes en servidores web.
  - Comando básico para escanear un servidor web:
        ```bash
        nikto -h [http://dominio_o_ip]
        ```
- Cómo utilizar Wfuzz, Dirb para localizar recursos web en servidores.
- **Wfuzz**: Herramienta para fuzzing en aplicaciones web. Se utiliza para identificar directorios y archivos ocultos.
  - Ejemplo de comando básico para fuzzing de directorios:
        ```bash
        wfuzz -c -w /ruta/a/wordlist.txt -u http://[dominio]/FUZZ
        ```
- **Dirb**: Herramienta similar a Wfuzz para buscar recursos en aplicaciones web.
  - Ejemplo de comando básico para buscar directorios:
        ```bash
        dirb http://[dominio]
        ```
- Que scripts que podemos utilizar con Nmap para la búsqueda de vulnerabilidades.
- **Nmap Scripting Engine (NSE)**: Nmap tiene un conjunto de scripts predefinidos para detectar vulnerabilidades.
  - Para ver la lista de scripts disponibles, puedes consultar:
    ```bash
    nmap --script-help
    ```
  - Para ejecutar un script de vulnerabilidad, por ejemplo:
    ```bash
    nmap --script=vuln [IP]
    ```


- Cómo podemos buscar información de explotación de vulnerabilidades con searchsploit
- **Searchsploit** es una herramienta que proporciona acceso a la base de datos de Exploit-DB, donde puedes encontrar exploits disponibles para vulnerabilidades conocidas.
  - Comando básico para buscar exploits para Linux con Kernel 5:
    ```bash
    searchsploit linux kernel 5
    ```

- Instala en tu navegador la extensión de Shodan y muestra la información que tenemos tanto de ip, como de dominio del sitio http://iesvalledeljerteplasencia.es 
- Sobre la red del laboratorio PPS con kali, bWAPP, Multidillae y DVWA:<
	- Ayudándote del fichero docker-compose localiza las diferentes máquinas y puertos que deberían de tener abiertos.
	- Identifica los equipos de la Red con Nmap.
	- Realiza análisis de puertos en las MV.
	- Encuentra los Servicios y Sistemas Operativos de las MV.
	- Inspecciona los puertos con nikto.
	- Busca las vulnerabilidades de las MV con los scripts de Nmap.
	- Localiza los servicios web que tienen las diferentes máquinas (Wfuzz y Dirb).
	- Utiliza el comando searchsploit para buscar información de explotación de vulnerabilidades presentes en linux con kernel 5
---	
## ENTREGA

>__Realiza las operaciones indicadas__

>__Crea un repositorio  con nombre PPS-Unidad3Actividad2-Tu-Nombre donde documentes la realización de ellos.__

> No te olvides de documentarlo convenientemente con explicaciones, capturas de pantalla, etc.

>__Sube a la plataforma, tanto el repositorio comprimido como la dirección https a tu repositorio de Github.__
