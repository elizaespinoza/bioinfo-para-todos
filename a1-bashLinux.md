[![CC BY 4.0][cc-by-shield]][cc-by]

# Navegando en Linux

## Qué es Linux?

Así como Windows, iOs y MacOs, Linux (o GNU/Linux) es un sistema operativo (SO), en otras palabras, gestiona la comunicación entre el software (lo que tú ves) y el hardware (lo que el computador ve).

<center><img src="https://img.icons8.com/nolan/64/linux--v1.png"/></center>

> ***¿Sabias que?:** El nombre GNU/Linux es la fusión del proyecto GNU por Richard Stallman (1983) con el kernel creado por Linus Torvalds (1991).*

## ¿Por qué Linux para bioinfo?

Linux permite **automatizar procesos** y minimizar los errores subsecuentes al hacer tareas repetitivas. Además es el preferido para los [programas y herramientas más usadas](https://snapcraft.io/search?category=science)) en este campo. 

<details><summary><b><i>Con linux puedo fácilmente...</i></b>
    </summary>
<p>

> 1. Construir pipelines rápidamente
>
> 2. Instalar programas y hacerles una configuración especial
>
> 3. Ordenar, cortar, girar, copiar... modificar archivos de texto
>
> 4. Acceder a entornos bioinformáticos listos para usar ([*biolinux*](http://environmentalomics.org/bio-linux-download/))
>
> 5. Mejorar la reproducibilidad de mis trabajos e investigaciones
>
> 6. Instalar varias versiones de un programa y activarlas o desactivarlas
>
> 7. Ayudar a difundir y (*por qué no*) desarrollar herramientas de código abierto
>
> 8. Correr mis análisis en grupos de computadoras
>
> 9. Mucho más...

Puedes ver la lista completa en el foro [biostars](https://www.biostars.org/p/11085/) (*el stackoverflow para biocomp*). 
    
</p>
</details>

### Distros

Una distro incluye determinados paquetes de software para satisfacer las necesidades de un grupo específico de usuarios.

| Común           | Difiere                  |
|-----------------|--------------------------|
| <img src="https://img.icons8.com/material/24/000000/checkmark--v1.png"/>  kernel Linux    | <i class="fas fa-times"></i> softwares de instalación |
| <i class="fas fa-check"></i>  GNU             | <i class="fas fa-times"></i> exploradores web         |
| <i class="fas fa-check"></i>  editor de texto | <i class="fas fa-times"></i> documentación            |
| <i class="fas fa-check"></i>  etc             |  <i class="fas fa-times"></i> suporte de la comunidad  |
|                 | <i class="fas fa-times"></i> entre otros                      |

> ***¿Sabias que?** Linux tiene más de 600 distribuciones, con 500 en activo desarrollo.*
>
> <center><img src="https://3.bp.blogspot.com/-0jYZSw_TPTs/WqscGOREDLI/AAAAAAAAABA/LhqVvv9cbskezwxOtSOBPBHzVeF8Bjc2ACLcBGAs/s1600/LINUX.gif"/ style="width:100px;"></center>

#### ¿Cuál distro escojo?
*Factores a tomar en cuenta...*
* Distro que tenga una amplia colección de repositorios.
* Comunidad grande y comprensiva.
* Tener un buen soporte para el hardware de mi interés (nvidia, AMD, Intel, etc).

##### Ubuntu
<i class="fab fa-ubuntu"></i> Ubuntu es uno de los más populares, tem uma comunidad amplia, así como una interfaz amigable y es de fácil uso.

##### CentOS
Para servidores.

##### Fedora
Para computador personal.

##### Biolinux
[Biolinux](https://www.bioinformatics.org/download/bio-linux/) es basado en Ubuntu 14.04 LTS y ofrece mas de 500 programas com foco en bioinformática.

> *Dale un vistazo a otros [proyectos de **distros en bioinfo**](https://wiki.debian.org/DebianMed) PD: <code>Ctrl+F</code> "Similar Initiatives"*

### Shell

Es la interfaz de línea de comando que permite la comunicación entre el usuario y el SO. Por default en Linux viene [**bash**](https://github.com/ohmybash/oh-my-bash), mas existen otros como [fish](https://fishshell.com/), [zsh](https://ohmyz.sh/), sh, csh, *etc.*

> ***¿Sabias que?** Bash viene de "Bourne Again Shell", ya que es un reemplazo mejorado de sh escrito por Steve Bourne.*

### Emulador de terminal

Este programa nos da acceso al shell y nos permite interactuar con el. Linux usa "gnome-terminal" (más conocido como "terminal").

### [Usando <code>bash</code> para bioinfo](#1-practica)

¡Manos a la obra! Con tu [emulador de terminal abierto](https://github.com/ElizaAlfaro/bioinfo-para-todos/blob/main/a1-2-servidor.md) en tu compu, debes estar viendo <code>[trujillo@bioinfo ~]$</code>, este es el *'shell prompt'* que indica que el shell está listo para aceptar entradas.

Normalmente este va a incluir el <code>nombre-usuario@nombre-maquina</code>, seguido del directorio de trabajo actual y un signo de dólar (\$).

> *Si el último carácter del prompt es numeral (#) en lugar de dólar (\$), estamos en modo de superusuario.*

Ahora vamos a escribir algunos comandos simples, más útiles:

* ¿Quieres saber la fecha y hora actual? Usa el comando <code>date</code>!
> ```shell
> date
> Qui Set  2 11:36:06 -03 2021
>```

* Si tienes interés en revisar tu calendario usa el comando <code>cal</code>.
> ```shell
> cal
>     setembro 2021
> Do Se Te Qu Qu Se Sá
>          1  2  3  4
> 5  6  7  8  9  10 11
> 12 13 14 15 16 17 18
> 19 20 21 22 23 24 25
> 26 27 28 29 30
>

* Para limpiar tu terminal usa el comando <code>clear</code>.

* Si quieres terminal tu sesión y cerrar tu terminal, puedes usar el comando <code>exit</code>. ***Ojo!** Si cierras ahora tu terminal tienes que [entrar de nuevo al servidor](https://github.com/ElizaAlfaro/bioinfo-para-todos/blob/main/a1-2-servidor.md).*

#### Navegando en el servidor

Los comandos que necesitamos de inicio para navegar desde el terminal son [<code>cd</code>](https://www.rapidtables.com/code/linux/cd.html), [<code>ls</code>](https://www.rapidtables.com/code/linux/ls.html), <code>pwd</code>, [<code>mv</code>](https://www.rapidtables.com/code/linux/mv.html), <code>rm</code>, <code>mkdir</code> y <code>rmdir</code>.

> *Si quieres ver el manual de cada comando solo digita <code>man</code> seguido del comando que quieres revisar (ejemplo: <code>man ls</code>)*

* <code>cd</code> (**c**hange **d**irectory) te permite cambiar de directorio.
* <code>ls</code> (**l**i**s**t) te muestra los archivos que están en un directorio.
* <code>pwd</code> (**p**resent **w**orking **d**irectory) te muestra la ruta hasta el directorio actual.
* <code>mv</code> (**m**o**v**e) mueve un archivo o directorio a una dirección específica. También se usa para renombrar.
* <code>rm</code> (**r**e**m**ove): elimina un archivo.
* <code>mkdir</code> (**m**a**k**e **dir**ectory) crea un nuevo directorio.
* <code>rmdir</code> (**r**e**m**ove **dir**ectory) elimina un directorio.

Vamos a divertirnos haciendo algunos ejercicios ¡Buena suerte!

1. Muestra tu directorio actual.

> ```shell
> pwd
> /home/trujillo
>```

2. Retrocede un directorio

> ```shell
> cd ..
> pwd
> /home
>```

3. Vuelve al directorio de inicio.

> ```shell
> cd ~
> pwd
> /home/trujillo
>```

4. Vuelve al directorio anterior.

> ```shell
> cd -
> pwd
> /home
>```

5. Lista el contenido del directorio.

> ```shell
> ls
> ```

6. Lista el contenido del directorio con formato largo (mostrando permisos) y mostrando los archivos ocultos.

> ```shell
> ls -la
> ```

7. Lístalo de nuevo con formato largo mas mostrando un tamaño legible.

> ```shell
> ls -lh
> ```

8. Lístalo de forma ordenada por fecha y hora (del más reciente al más antiguo), ahora lístalo al revés.

> ```shell
> ls -t
> ls -tr
> ```

9. Lista el contenido del directorio con las opciones anteriores juntas. 

> ```shell
> ls -haltr
> ```

#### Trabajando con texto en Unix.

Ya que hemos calentado los motores, vamos a trabajar ahora con la secuencia de nucleótidos que codifican a la mioregulina.

1. Entra a la carpeta <code>intro_bioinfo</code>.

> ```shell
> cd intro_bioinfo
> pwd
> /home/trujillo/intro_bioinfo
> ```

2. Crea una carpeta con tu nombre y entra en ella.

> ```shell
> mkdir tu-nombre
> cd tu-nombre
> pwd
> /home/trujillo/intro_bioinfo/tu-nombre
> ```

3. Crea una carpeta llamada <code>bash_1</code> y entra en ella.

> ```shell
> mkdir bash_1
> cd bash_1
> pwd
> /home/trujillo/intro_bioinfo/tu-nombre/bash_1
> ```

Ahora vienen unos nuevos comandos que serán de gran utilidad.

4. Crea un archivo de texto llamado <code>sec</code> con ayuda del editor de texto <code>vi</code>.

> ```shell
> vi sec
> ```

5. Para entrar em modo de inserción (INSERT MODE) digita <code>i</code>.

6. Copia la secuencia la mioregulina de *Mus musculus* (ID NCBI: [NM_001304739.1](https://www.ncbi.nlm.nih.gov/nuccore/NM_001304739.1?report=fasta)) a seguir, dando click derecho en tu terminal.

```
1. AGTGAGCTTTTCGTCCATGGAGAGCAGATGGTGTTTTTGAAAGGAAGGGC
2. GGCCATTCCCAGGACTTTGGACTTGGCTCCGTTGCACCCCTGAACAGAAC
3. CAACGTTGCTAGGAGAACACCTGTGCCCCAGCACTTTGGTCCAGCAAGGG
4. CAGGAGAGGAGAGCTGGAAACTGGTAGAGCTGTGCTACCTGCTACCTCCT
5. GAGGCTCTCAGGGAGCAGGAGAATCTGAACATGAGTGGCAAGAGCTGGGT
6. ACTGATCTCTACTACTTCGCCCCAGAGCCTGGAAGATGAGATTCTGGGAC
7. GGCTTCTGAAAATTCTCTTCGTTTTGTTCGTTGACTTAATGTCCATTATG
8. TATGTCGTCATAACGTCCTAGCAACCTGACTTTCTTTACTCCGTGTGTAA
9. GTTTCAAACCAAATGCGAGCAAATAAAGATCTACATTTTAATCTGA
```
7. Cierra el editor de texto presionando la tecla <code>Esc</code>, luego digita <code>:x!</code>.

8. Verifica tu archivo <code>sec</code> mediante los siguientes comandos:

> ```shell
> cat sec      #imprime todo el archivo en el terminal
> head sec     #imprime las primeras lineas del archivo
> head -3 sec  #imprime las primeras 3 lineas del archivo
> tail sec     #imprime las últimas líneas del archivo
> tail -3 sec  #imprime las últimas 3 líneas del archivo
> more sec     #imprime el archivo en el terminal
> less sec     #imprime el archivo en el terminal
> ```

9. Busca donde aparece <code>2</code> y <code>6</code> e muestra las líneas que los tienen.

> ```shell
> grep "[2|6]" sec
> 2. GGCCATTCCCAGGACTTTGGACTTGGCTCCGTTGCACCCCTGAACAGAAC
> 6. ACTGATCTCTACTACTTCGCCCCAGAGCCTGGAAGATGAGATTCTGGGAC
> ```

#### Concatenando procesos

##### *Convirtiendo ADN en ARN*

1. Substituye la timina <code>T</code> por el uracilo <code>U</code> y guarda esta secuencia en un archivo llamado <code>rna_sec</code>.

> ```shell
> cat sec | tr T U > "rna_sec"
> head -3 rna_sec
> 1. AGUGAGCUUUUCGUCCAUGGAGAGCAGAUGGUGUUUUUGAAAGGAAGGGC
> 2. GGCCAUUCCCAGGACUUUGGACUUGGCUCCGUUGCACCCCUGAACAGAAC
> 3. CAACGUUGCUAGGAGAACACCUGUGCCCCAGCACUUUGGUCCAGCAAGGG
> ```

##### *Hallando el reverso complementar*
1. Selecciona solamente la secuencia de nucleótidos, substituye estos por su respectivo complementar (A para C para G y viceversa), invierte el orden y guarda la secuencia resultante en un archivo llamado <code>dna_comp</code>.

> ```shell
> grep -o '[ACTG]*' sec | tr ACGT TGCA | rev > "dnacomp_sec"
> head -3 dnacomp_sec
> 1. AGUGAGCUUUUCGUCCAUGGAGAGCAGAUGGUGUUUUUGAAAGGAAGGGC
> 2. GGCCAUUCCCAGGACUUUGGACUUGGCUCCGUUGCACCCCUGAACAGAAC
> 3. CAACGUUGCUAGGAGAACACCUGUGCCCCAGCACUUUGGUCCAGCAAGGG
> ```

##### *Calculando GC*
1. Selecciona solamente los caracteres que correspondem a citocina <code>C</code> y guanina <code>G</code> y calcula cuantos son.
> ```shell
> grep -o '[CG]' sec | wc -l
> 217
> ```

##### *Contando el número de secuencias*
1. En la dirección <code>/home/trujillo/data/</code> se encuentra el archivo <code>tumor.seq</code>. Revisa el archivo con <code>less</code>.

> ```shell
> less /home/trujillo/data/tumor.seq
> ```

2. Cuenta el número de secuencias presentes en aquel archivo.

> ```shell
> cat /home/trujillo/data/tumor.seq | grep ">" -c
> 510703
> ```

#### Alineamiento de secuencias con Blast

Vamos alinear la secuencia de [<code>ace2</code>](https://www.uniprot.org/uniprot/Q9BYF1.fasta) de *H. sapiens* contra el transcriptoma de tumor de mama <code>tumor.seq</code>, para ver si este receptor de coronavirus está expresado en este. 

1. Guarda la secuencia del receptor de coronavirus en tu carpeta utilizando <code>vi</code>.
```python
>sp|Q9BYF1|ACE2_HUMAN Angiotensin-converting enzyme 2 OS=Homo sapiens OX=9606 GN=ACE2 PE=1 SV=2
MSSSSWLLLSLVAVTAAQSTIEEQAKTFLDKFNHEAEDLFYQSSLASWNYNTNITEENVQ
NMNNAGDKWSAFLKEQSTLAQMYPLQEIQNLTVKLQLQALQQNGSSVLSEDKSKRLNTIL
NTMSTIYSTGKVCNPDNPQECLLLEPGLNEIMANSLDYNERLWAWESWRSEVGKQLRPLY
EEYVVLKNEMARANHYEDYGDYWRGDYEVNGVDGYDYSRGQLIEDVEHTFEEIKPLYEHL
HAYVRAKLMNAYPSYISPIGCLPAHLLGDMWGRFWTNLYSLTVPFGQKPNIDVTDAMVDQ
AWDAQRIFKEAEKFFVSVGLPNMTQGFWENSMLTDPGNVQKAVCHPTAWDLGKGDFRILM
CTKVTMDDFLTAHHEMGHIQYDMAYAAQPFLLRNGANEGFHEAVGEIMSLSAATPKHLKS
IGLLSPDFQEDNETEINFLLKQALTIVGTLPFTYMLEKWRWMVFKGEIPKDQWMKKWWEM
KREIVGVVEPVPHDETYCDPASLFHVSNDYSFIRYYTRTLYQFQFQEALCQAAKHEGPLH
KCDISNSTEAGQKLFNMLRLGKSEPWTLALENVVGAKNMNVRPLLNYFEPLFTWLKDQNK
NSFVGWSTDWSPYADQSIKVRISLKSALGDKAYEWNDNEMYLFRSSVAYAMRQYFLKVKN
QMILFGEEDVRVANLKPRISFNFFVTAPKNVSDIIPRTEVEKAIRMSRSRINDAFRLNDN
SLEFLGIQPTLGPPNQPPVSIWLIVFGVVMGVIVVGIVILIFTGIRDRKKKNKARSGENP
YASIDISKGENNPGFQNTDDVQTSF
```

2. Como nuestra query corresponde una secuencia proteica y nuestros trasncriptos son conformados por nucleótidos, vamos utilizar la modalidad tblastn.

```shell
blastall -p tblastn -i ace2 -d /home/trujillo/data/tumor.seq -e 1e-10 -F F -a 20 -o salida &
ls
less salida
```

3. Continuaremos con la modalidad tblastn, mas visualizaremos la salida tabulada y comentada.

```shell
blastall -p tblastn -i ace2 -d /home/trujillo/data/tumor.seq -e 1e-10 -F F -a 20 -o m9salida -m 9 &
ls
less m9salida
```
4. Ahora vamos a visualizar esta salida tabulada no comentada <code>m8salida</code>.

```shell
blastall -p tblastn -i ace2 -d /home/trujillo/data/tumor.seq -e 1e-10 -F F -a 20 -o m8salida -m 8 &
ls
less m8salida
```

5. Con esta salida tabulada sin comentarios, vamos a contar cuantos transcriptos de ace2 tenemos en nuestro transcriptoma <code>tumor.seq</code>.

```shell
cat m8salida | cut -f 1 | wc
      8       8     168
```

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg