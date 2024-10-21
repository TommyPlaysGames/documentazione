# Incremento/Decremento JTextField - Documentazione

## Descrizione

Il programma `spadaTommasoIncrementoDecremento` implementa un'applicazione Java Swing che consente all'utente di incrementare o decrementare un valore numerico visualizzato in un campo di testo (`JTextField`). Il valore è limitato a un intervallo compreso tra -10 e 10. Due pulsanti, uno per incrementare e uno per decrementare il valore, permettono all'utente di modificarlo facilmente.

### Funzionalità principali:
- Visualizzazione di un valore numerico all'interno di un campo di testo.
- Possibilità di incrementare o decrementare il valore tramite pulsanti.
- Il valore è limitato a un intervallo compreso tra -10 e 10.

## Classi e Metodi

### Classe `spadaTommasoIncrementoDecremento`

Questa classe rappresenta la finestra principale dell'applicazione. Utilizza un layout `FlowLayout` e gestisce la logica di incremento e decremento del valore.

#### Metodi principali:

- **`main(String[] args)`** 
  Il metodo principale che avvia l'applicazione, crea la finestra e imposta i componenti della GUI (campo di testo e pulsanti).

- **`incrementButton.addActionListener`** 
  Aggiunge un listener al pulsante di incremento. Quando premuto, aumenta il valore di `1` se il valore corrente è inferiore a `10`.

- **`decrementButton.addActionListener`** 
  Aggiunge un listener al pulsante di decremento. Quando premuto, diminuisce il valore di `1` se il valore corrente è superiore a `-10`.

## Esecuzione del programma

Il metodo `main` avvia l'applicazione creando un'istanza di `JFrame` con i seguenti componenti:
- **`JTextField`**: Visualizza il valore numerico che può essere incrementato o decrementato.
- **`JButton +`**: Incrementa il valore.
- **`JButton -`**: Decrementa il valore.

Il valore iniziale è 0 e può variare tra -10 e 10. La finestra si apre con una dimensione di 300x200 pixel.

```java
public class spadaTommasoIncrementoDecremento {
    private static int value = 0;

    public static void main(String[] args) {
        JFrame frame = new JFrame("Incrementa/Decrementa");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(300, 200);
        frame.setLayout(new FlowLayout());

        JTextField valueField = new JTextField(String.valueOf(value), 5);
        frame.add(valueField);

        JButton incrementButton = new JButton("+");
        JButton decrementButton = new JButton("-");

        incrementButton.addActionListener(_ -> {
            if (value < 10) {
                value++;
                valueField.setText(String.valueOf(value));
            }
        });

        decrementButton.addActionListener(_ -> {
            if (value > -10) {
                value--;
                valueField.setText(String.valueOf(value));
            }
        });

        frame.add(incrementButton);
        frame.add(decrementButton);
        frame.setVisible(true);
    }
}
```
## Dettagli Tecnici

- **Layout utilizzato:** `FlowLayout`  
  La finestra utilizza un layout che organizza i componenti in una disposizione lineare.

- **Componenti Swing utilizzati:**
  - `JTextField`: per visualizzare il valore corrente.
  - `JButton`: per incrementare o decrementare il valore.

## Dipendenze

Il programma richiede le seguenti librerie:
- `javax.swing.*`: per la gestione della GUI.
- `java.awt.*`: per i componenti grafici e il layout.

## Note

- Il programma è pensato per essere eseguito su una finestra di dimensioni standard (300x200).
- Il valore è limitato a un intervallo di [-10, 10].
