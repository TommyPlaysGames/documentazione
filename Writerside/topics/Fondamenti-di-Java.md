# Fondamenti di Java

Questa sezione introduce i concetti di base del linguaggio Java, la sua sintassi, e le strutture fondamentali. È pensata per chi si avvicina per la prima volta a Java o per chi desidera rinfrescare le proprie conoscenze di base.

## Concetti Principali

### Variabili e Tipi di Dati
In Java, le variabili sono utilizzate per memorizzare dati e vengono definite con un tipo specifico. Esistono tipi di dati primitivi come:
- **`int`**: numeri interi (es. `int x = 5;`)
- **`double`**: numeri con la virgola mobile (es. `double pi = 3.14;`)
- **`char`**: singoli caratteri (es. `char iniziale = 'A';`)
- **`boolean`**: valori booleani, che possono essere `true` o `false` (es. `boolean flag = true;`)

### Operatori
Gli operatori permettono di eseguire operazioni su variabili e costanti:
- **Aritmetici**: come `+`, `-`, `*`, `/` per le operazioni matematiche.
- **Relazionali**: come `==`, `!=`, `>`, `<` per confronti tra valori.
- **Logici**: come `&&`, `||`, `!` per espressioni booleane complesse.

### Strutture di Controllo
Le strutture di controllo permettono di gestire il flusso di esecuzione del programma:
- **Condizionali**: `if`, `else`, `else if` per eseguire codice basato su condizioni specifiche.
  ```java
  if (x > 10) {
      System.out.println("x è maggiore di 10");
  } else {
      System.out.println("x è minore o uguale a 10");
  }
  ```
- **Switch**: un’alternativa all’`if-else` per gestire più condizioni su valori discreti.
  ```java
  switch(giorno) {
      case 1: System.out.println("Lunedì"); break;
      case 2: System.out.println("Martedì"); break;
      default: System.out.println("Altro giorno");
  }
  ```

### Cicli
I cicli permettono di ripetere blocchi di codice:
- **`for`**: usato per iterazioni con un numero determinato di ripetizioni.
  ```java
  for (int i = 0; i < 5; i++) {
      System.out.println(i);
  }
  ```
- **`while`** e **`do-while`**: usati per eseguire blocchi di codice finché una condizione è vera.
  ```java
  while (condizione) {
      // Codice
  }
  ```

### Metodi
I metodi permettono di suddividere il codice in blocchi riutilizzabili. Definire un metodo include specificare il suo tipo di ritorno, il nome e i parametri:
```java
public int somma(int a, int b) {
    return a + b;
}
```
- I metodi possono avere o meno parametri, e restituire o no un valore.

### Gestione degli Errori
In Java, gli errori possono essere gestiti utilizzando le eccezioni (`try-catch`):
```java
try {
    // Codice che può lanciare un'eccezione
} catch (Exception e) {
    System.out.println("Si è verificato un errore: " + e.getMessage());
}
```