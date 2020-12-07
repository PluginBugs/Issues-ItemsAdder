# Guida su come si crea un Server localhost

### Premessa
1) Scaricare questo: https://git-scm.com/downloads
<br/>1.2) Assicurarsi di abilitare l'attivazione di tutte le proprietà del download e lasciare l'installer scegliere le funzioni in maniera autonoma.
<br/>Per farla breve: premere "avanti" o "accetto" tutto il tempo.
2) Creare la cartella dove si desidera effettivamente creare il proprio Server di gioco, per esempio MC_TEST_SERVER

## Fare la seguente scelta:
### SCELTA: Creare un Server SPIGOT
4) Guida dettagliata in caso di bisogno: https://www.spigotmc.org/wiki/buildtools
5) Scaricare l'ultima build qui: https://hub.spigotmc.org/jenkins/job/BuildTools/
6) Creare una cartella dedicata alla build spigot, per esempio MC_SPIGOT
<br/>6.2) Inserire la build scaricata nella cartella MC_SPIGOT

### SCELTA: Creare un Server PAPER
4) Andare qui: https://papermc.io/downloads
5) Scaricare l'ultima build in download
6) Inserire la build scaricata nella cartella del proprio server di gioco MC_TEST_SERVER

### Iniziare lo spacchettamento dei dati della Build
7) Cliccando in un punto vuoto della cartella con il TASTO DESTRO del vostro Mouse, selezionare la voce **GIT BASH HERE"
8) Vi si aprirà un terminale di comandi da amministratore...

  • Se state creando un server **SPIGOT**, in esso eseguite il seguente comando:
<br/>`java -jar BuildTools.jar`

  • *La versione di Spigot può essere definita usando il parametro `--rev <version>`. Esempio: `java -jar BuildTools.jar --rev 1.16.4`. In assenza di questo parametro, sarà scaricata automaticamente la versione più recente disponibile.*
  
  • Se state creando un server **PAPER**, rinomina il file .jar in server.jar ed eseguite il seguente comando:
<br/>`java -jar server.jar`

9) :warning: ATTENZIONE, proprio in questo punto potreste riscontrare un primo problema. Il processo potrebbe arrestarsi con la motivazione di "out of memory". In questo caso nella schermata del terminale vi consiglia automaticamente il comando da eseguire per poter risolvere il problema e specificando quindi manualmente la quantità di memoria.
<br/>Questo valore sarà definito da questa stringa: Esempio: -Xmx1024M e dovete inserirla come negli esempi di seguito. Il valore numerico cambia da computer a computer.
<br/>Rieseguite quindi il comando come in questo esempio:
<br/>Esempio Spigot: `java -Xmx1024M -jar BuildTools.jar`
<br/>Esempio Paper: `java -Xmx1024M -jar server.jar`
<br/>Se invece siete sicuri di avere una memoria piu ampia e non capite come mai vi impone questo limite non avete probabilmente installato Java a 64 bit.
<br/>Potete scaricarlo qui: https://www.java.com/fr/download/ Una volta terminata questa installazione eseguite di nuovo il punto **8**

10) Si iniziano a creare delle cartelle e dei files.
11) **Se hai scelto di creare un Server PAPER salta diretto al punto 17, altrimenti continua la lista.**
12) Ok hai scelto di creare un Server SPIGOT, allora aspetta che tutto il processo termini.
13) A processo finito, noterai che si è creato un file di nome: "spigot-<version>.jar" nella tua cartella MC_SPIGOT. Esempio: "spigot-1.16.4.jar"
14) Rinomina questo file in questo modo: "spigot.jar"
15) Fai CTRL+X (taglialo) su di lui ed incollalo nella cartella che hai precedentemente creato di nome MC_TEST_SERVER.
16) Fai DOPPIO-CLICK (come per aprire) il file "spigot.jar", noterete che inizieranno a creare delle cartelle e dei files.
17) Però il processo si interromperà. Ma stavolta è normale. Perché il sistema vi obbligherà ad accettare l'EULA.
18) Aprire il file "eula.txt"
19) Modificare la configurazione `eula=false` in `eula=true`
20) Fai DOPPIO-CLICK (come per aprire) sul file "spigot.jar" oppure "server.jar"
21) Il server è finalmente ONLINE. Potete entrarci andando nel vostro launcher di minecraft e nell'indirizzo server scrivete "localhost"


# Sezione relativa alla risoluzione dei problemi se ce ne fossero.
22) Se nonostante tutto non riesci ad avviare il server perché ti da problemi di "out of memory" prova a:

**Windows:**
<br/>Incolla il testo seguente in un file testuale. Salvalo come "start.bat" nella stessa cartella dove si trova "spigot.jar" oppure "server.jar":

• SPIGOT
```
@echo off
java -Xms#G -Xmx#G -XX:+UseG1GC -jar spigot.jar nogui
pause
```
• PAPER
```
@echo off
java -Xms#G -Xmx#G -XX:+UseG1GC -jar server.jar nogui
pause
```
<br/>(where # is your allocated server memory in GB)
<br/>23. Fai doppio click sul file "start.bat" e torna al punto **21** della lista
<br/>*Se usi Mac oppure un altro tipo di coputer, fai riferimento a questa guida:* https://www.spigotmc.org/wiki/spigot-installation/



# ItemAdder compatibility
Se vuoi rendere compatibile il tuo server privato con ItemAdder segui queste indicazioni:
<br/>https://itemsadder.plugin.ga/plugin-usage/tips-for-fastest-usage
