# Programmazione Orientata agli Oggetti (OOP)

Java è un linguaggio orientato agli oggetti, e questa sezione descrive i concetti fondamentali di OOP, inclusi classi, oggetti, ereditarietà e polimorfismo.

## Concetti Principali

### Classi e Oggetti
In Java, tutto ruota attorno alle classi e agli oggetti:
- **Classe**: Definisce un modello o schema da cui creare oggetti. Le classi possono contenere campi (variabili) e metodi.
  ```java
  class Persona {
  String nome;
  int età;
      void saluta() {
          System.out.println("Ciao, sono " + nome);
      }
  }
  ```
- **Oggetti**: Sono istanze di una classe.
  ```java
  Persona p = new Persona();
  p.nome = "Mario";
  p.saluta();
  ```

### Incapsulamento
L'incapsulamento consente di nascondere i dettagli interni delle classi e di esporre solo ciò che è necessario:
- I campi privati possono essere accessibili solo tramite metodi pubblici (getter/setter).
  ```java
  class Persona {
  private String nome;

      public String getNome() {
          return nome;
      }

      public void setNome(String nuovoNome) {
          nome = nuovoNome;
      }
  }
  ```

### Ereditarietà
L'ereditarietà permette a una classe di ereditare i metodi e i campi di un'altra classe:
```java
class Animale {
    void dormi() {
        System.out.println("Sto dormendo");
    }
}

class Cane extends Animale {
    void abbaia() {
        System.out.println("Woof Woof");
    }
}
```
Un cane eredita il comportamento di un animale e aggiunge nuove funzionalità.

### Polimorfismo
Il polimorfismo permette di trattare gli oggetti in modo flessibile, utilizzando una classe base per riferirsi a oggetti di classi derivate:
```java
Animale a = new Cane();
a.dormi(); // Output: Sto dormendo
```

### Interfacce e Classi Astratte
Le interfacce e le classi astratte offrono un modo per definire comportamenti comuni che possono essere implementati in classi diverse:
- **Interfacce**: Definiscono solo metodi astratti, che devono essere implementati nelle classi concrete.
  ```java
  interface Animale {
      void suono();
  }

  class Cane implements Animale {
      public void suono() {
          System.out.println("Woof Woof");
      }
  }
  ```

- **Classi Astratte**: Possono contenere sia metodi astratti che metodi concreti.
  ```java
  abstract class Forma {
      abstract void disegna();
  }

  class Cerchio extends Forma {
      void disegna() {
          System.out.println("Disegna un cerchio");
      }
  }
  ```