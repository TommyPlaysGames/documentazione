# Prodotto Matrici JTextArea - Documentazione

## Descrizione

Il programma `spadaTommasoProdottoMatriciJTextArea` implementa un'applicazione Java Swing che permette di visualizzare la moltiplicazione di due matrici generate casualmente. Le matrici e il loro prodotto vengono visualizzati in tre diverse aree di testo (`JTextArea`), ognuna contenuta in un pannello di scorrimento (`JScrollPane`).

Le dimensioni delle matrici sono predefinite:
- La prima matrice ha dimensioni 2x3.
- La seconda matrice ha dimensioni 3x4.
- Il risultato della moltiplicazione sarà una matrice 2x4.

### Funzionalità principali:
- Generazione di due matrici con valori casuali.
- Calcolo del prodotto delle due matrici.
- Visualizzazione delle matrici e del loro prodotto all'interno di `JTextArea`.

## Classi e Metodi

### Classe `spadaTommasoProdottoMatriciJTextArea`

Questa classe estende `JFrame` e rappresenta la finestra principale dell'applicazione. Il costruttore configura la GUI, genera le matrici e visualizza il risultato della moltiplicazione.

#### Metodi principali:

- **`spadaTommasoProdottoMatriciJTextArea()`** 
  Costruttore che configura il layout della finestra, crea tre `JTextArea` per visualizzare le due matrici e il risultato, e calcola il prodotto delle matrici.

- **`generaMatrice(int righe, int colonne)`** 
  Metodo che genera una matrice di dimensioni `righe x colonne` con valori casuali compresi tra 0 e 9.

- **`visualizzaMatrice(JTextArea textArea, int[][] matrice)`** 
  Metodo che converte una matrice in una stringa formattata e la visualizza in un componente `JTextArea`.

- **`moltiplicaMatrici(int[][] matrice1, int[][] matrice2)`** 
  Metodo che esegue la moltiplicazione di due matrici e restituisce il risultato.

### Esempio di Output:

La finestra dell'applicazione si suddivide in tre pannelli:
1. **Matrice 1:** Visualizza la prima matrice generata (ad es. 2x3).
2. **Matrice 2:** Visualizza la seconda matrice generata (ad es. 3x4).
3. **Risultato:** Mostra il prodotto delle due matrici (ad es. 2x4).

## Esecuzione del programma

Il metodo `main` avvia l'applicazione creando un'istanza della classe `spadaTommasoProdottoMatriciJTextArea`. La finestra si apre con tre aree di testo che mostrano le matrici e il loro prodotto. Il programma termina chiudendo la finestra.

```java
public static void main(String[] args) {
    spadaTommasoProdottoMatriciJTextArea frame = new spadaTommasoProdottoMatriciJTextArea();
    frame.setVisible(true);
}
```
## Dettagli Tecnici

- **Layout utilizzato:** `GridLayout(1, 3)` 
  La finestra utilizza un layout a griglia con una sola riga e tre colonne, in cui vengono posizionati i pannelli di scorrimento delle aree di testo.

- **Gestione delle matrici:** 
  La moltiplicazione delle matrici avviene tramite tre cicli `for` annidati, che seguono la classica procedura di moltiplicazione tra matrici.

- **Componenti Swing utilizzati:**
  - `JTextArea`: per visualizzare le matrici.
  - `JScrollPane`: per aggiungere la barra di scorrimento orizzontale e verticale in caso di necessità.
  
## Dipendenze

Il programma richiede le seguenti librerie:
- `javax.swing.*`: per la gestione della GUI.
- `java.awt.*`: per i componenti grafici e il layout.
- `java.util.Random`: per generare i valori casuali delle matrici.

## Note

- Il programma è pensato per essere eseguito su una finestra di dimensioni standard (1366x768).
- Il calcolo della moltiplicazione richiede che il numero di colonne della prima matrice sia uguale al numero di righe della seconda matrice.
