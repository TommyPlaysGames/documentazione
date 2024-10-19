# Database e Persistenza

L'integrazione con un database è fondamentale per applicazioni che richiedono la memorizzazione persistente dei dati. Java supporta l'interazione con i database relazionali tramite l'API **JDBC** (Java Database Connectivity).

## Concetti Principali

### Connessione al Database con JDBC

Il seguente codice mostra come stabilire una connessione con un database MySQL utilizzando JDBC.

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

public class DatabaseConnection {
    public static Connection connect() {
        try {
            String url = "jdbc:mysql://localhost:3306/miodatabase";
            String user = "root";
            String password = "password";
            Connection connection = DriverManager.getConnection(url, user, password);
            return connection;
        } catch (SQLException e) {
            e.printStackTrace();
            return null;
        }
    }
}
```

La connessione è stabilita utilizzando il metodo `getConnection` che richiede l'URL del database, l'utente e la password.

### Persistenza dei Dati

La **persistenza dei dati** può essere gestita anche attraverso file, oltre che con database. Un modo semplice di scrivere dati su un file in Java è usare **FileWriter**.

```java
import java.io.FileWriter;
import java.io.IOException;

public class FilePersistence {
    public static void main(String[] args) {
        try {
            FileWriter writer = new FileWriter("dati.txt");
            writer.write("Esempio di scrittura su file.");
            writer.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```