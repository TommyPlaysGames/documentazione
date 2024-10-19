# Applicazioni Avanzate

Le applicazioni avanzate in Java combinano varie tecnologie come interfacce grafiche, database, e algoritmi complessi per risolvere problemi reali o gestire sistemi complessi. Una parte importante di queste applicazioni è l'integrazione efficiente tra le componenti.

## Concetti Principali

### Integrazione di GUI e Database

In molte applicazioni avanzate, l'utente interagisce con un'interfaccia grafica per gestire dati salvati su un database. Ad esempio, un'applicazione gestionale può consentire di aggiungere, modificare e cancellare record tramite la GUI e salvare le modifiche in un database.

Ecco un esempio in cui un utente può aggiungere un record di un libro a un database da una GUI:

```java
import javax.swing.*;
import java.awt.event.*;
import java.sql.*;

public class AggiungiLibroGUI {
public static void main(String[] args) {
JFrame frame = new JFrame("Aggiungi Libro");
JTextField titoloField = new JTextField(20);
JButton aggiungiButton = new JButton("Aggiungi");

        aggiungiButton.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                String titolo = titoloField.getText();
                try {
                    Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/biblioteca", "root", "password");
                    String query = "INSERT INTO libri (titolo) VALUES (?)";
                    PreparedStatement stmt = connection.prepareStatement(query);
                    stmt.setString(1, titolo);
                    stmt.executeUpdate();
                    connection.close();
                    JOptionPane.showMessageDialog(frame, "Libro aggiunto con successo");
                } catch (SQLException ex) {
                    ex.printStackTrace();
                }
            }
        });

        frame.add(titoloField);
        frame.add(aggiungiButton);
        frame.setLayout(new BoxLayout(frame.getContentPane(), BoxLayout.Y_AXIS));
        frame.setSize(300, 150);
        frame.setVisible(true);
    }
}
```