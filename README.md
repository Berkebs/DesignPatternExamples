# DesignPatternExamples
# Singleton Pattern

## Açıklama
**Singleton**, bir sınıftan yalnızca **tek bir nesne** oluşturulmasını garanti eden design pattern’dir.  
Unity’de genellikle `GameManager`, `AudioManager` veya `SaveSystem` gibi **global erişime ihtiyaç duyan** yapılarda kullanılır.

---

## UML Diyagramı
```mermaid
classDiagram
    class Singleton {
        - static Singleton instance
        - Singleton()
        + static Singleton GetInstance()
    }

    class GameManager {
        - int score
        + AddScore()
        + GetScore()
    }

    Singleton <|-- GameManager
