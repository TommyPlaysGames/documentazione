# Interfacce Grafiche (GUI)

Le interfacce grafiche (GUI) sono una parte cruciale delle applicazioni interattive. In Java, il toolkit più utilizzato per la creazione di GUI è **Swing**, che fornisce una serie di componenti per la costruzione di interfacce utente.

## Concetti Principali

### Componenti principali di una GUI Swing

- **JFrame**: la finestra principale dell'applicazione.
- **JPanel**: un contenitore flessibile che può contenere vari componenti.
- **JButton**: un pulsante che l'utente può cliccare.
- **JLabel**: un'etichetta per visualizzare testo o immagini.
- **JTextField**: un campo di testo per l'input.

### Esempio di creazione di una semplice finestra

```java
import javax.swing.*;

public class MyGUI {
public static void main(String[] args) {
JFrame frame = new JFrame("Interfaccia Grafica");
JButton button = new JButton("Cliccami");
        frame.add(button);
        frame.setSize(300, 200);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
    }
}
```

In questo esempio, si crea una finestra con un pulsante "Cliccami". Ogni componente è aggiunto al contenitore principale **JFrame** e la finestra è visualizzata con il metodo `setVisible(true)`.

### Layout Manager

I **layout manager** gestiscono la disposizione dei componenti all'interno di un contenitore come il **JPanel** o il **JFrame**. Alcuni layout comuni sono:

- **BorderLayout**: divide il contenitore in cinque regioni.
- **FlowLayout**: posiziona i componenti in sequenza orizzontale.
- **GridLayout**: organizza i componenti in una griglia con righe e colonne fisse.

