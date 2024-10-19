# Librerie e API Java

Java fornisce una vasta gamma di librerie e API per semplificare lo sviluppo di software. Questa sezione esplora le librerie più importanti e come utilizzarle.

## Concetti Principali

### Collezioni
Java offre diverse strutture dati per memorizzare e gestire gruppi di oggetti:
- **ArrayList**: Una lista dinamica che può espandersi.
  ```java
  ArrayList<String> lista = new ArrayList<>();
  lista.add("Elemento");
  ```
- **HashMap**: Una mappa per associare chiavi a valori.
  ```java
  HashMap<Integer, String> mappa = new HashMap<>();
  mappa.put(1, "Uno");
  ```
  
### I/O e File Handling
Java semplifica la lettura e la scrittura di file tramite le classi di I/O:
- **`BufferedReader`**: Per leggere dati da un file.
  ```java
  BufferedReader reader = new BufferedReader(new FileReader("file.txt"));
  String linea = reader.readLine();
  reader.close();
  ```

- **`FileWriter`**: Per scrivere dati in un file.
  ```java
  FileWriter writer = new FileWriter("file.txt");
  writer.write("Testo");
  writer.close();
  ```

### Gestione delle Eccezioni
Le eccezioni gestiscono gli errori durante l'esecuzione del programma, come file mancanti o input errato.
```java
try {
    // Codice che può lanciare un'eccezione
} catch (IOException e) {
    System.out.println("Errore di I/O");
}
```

### Java Streams API
Gli Stream forniscono un modo efficiente per lavorare con sequenze di dati:
```java
List<String> lista = Arrays.asList("A", "B", "C");
lista.stream().forEach(System.out::println);
```