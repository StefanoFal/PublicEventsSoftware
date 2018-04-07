Per eseguire il progetto senza compilarlo, fare doppio click sul file ProgettoINGSW - gruppo17 .jar. Se invece si intende compilarlo, è necessario installare le librerie esterne utilizzate (AWS, Data Picker, jUnit, jFreeChart).

GUIDA ALLA COMPILAZIONE
Installare Aws Toolkit for Eclipse. E' consigliato utilizzare eclipse perché amazon web services ha sviluppato un plugin per collegare i progetti java ad AWS velocemente. (https://docs.aws.amazon.com/toolkit-for-eclipse/v1/user-guide/setup-install.html). 
Creare un nuovo progetto Java AWS (Aws Java project) - potrebbe richiedere alcuni minuti.
Per collegare il database utilizzato al progetto, utilizzare le seguenti chiavi: (non dovrebbe comunque richiederle in quanto si è posto un accesso esplicito nel codice della connessione)
AWSAccessKeyId=AKIAJAXEAITBHDSGIJHA
AWSSecretKey=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

Importare il progetto (.zip) all'interno di eclipse facendo click col destro sul progetto creato > Import > Import existing project > import from zip > selezionare il zip export_progetto > selezionare la cartella ProgettoINGSWcsa > finish. 
Per importare le librerie Data Picker e JFreeChart decomprimere il file nella cartella con le librerie esterne(Pagine github associate: https://github.com/JDatePicker/JDatePicker https://github.com/jfree/jfreechart), click col destro sul progetto > Properties > Java build path > Add external Jars > selezionare il jar scaricato.

E' necessario avere installato anche la libreria jUnit per poter compilare il package di testing.

Per compilare - a causa di un bug di Eclipse - è necessario avere una versione di Java <= 8. Reinstallare se necessario, chiudere eclipse e riaprirlo, dopodiché compilare in un jar (Nota: il peso del Jar risulterà essere molto maggiore di quello già "pronto" nel progetto, questo perché di default verranno inserite tutte le librerie Maven - ovvero aws - nonostante ne venga utilizzata solo una piccola parte. E' possibile rimuovere manualmente le librerie in più).

Per eventuali problemi, contattare stefanofalangone@gmail.com
