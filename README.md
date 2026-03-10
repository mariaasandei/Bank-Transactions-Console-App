
# 🏦 BankAccount System (C# Console App)

O aplicație de consolă robustă care simulează gestionarea unui cont bancar, punând accent pe **integritatea datelor** și **gestionarea excepțiilor**. Proiectul permite crearea de conturi, efectuarea de depuneri/retrageri și generarea unui istoric detaliat al tranzacțiilor.

---

## ✨ Funcționalități Principale

* **Generare Automată de Conturi:** Fiecare cont primește un număr unic de 10 cifre, pornind de la o bază prestabilită.
* **Sistem de Tranzacții:** Utilizează un istoric complet (listă de obiecte `Transaction`) pentru a calcula balanța în timp real.
* **Validări de Siguranță:**
    * Previne depunerile sau retragerile cu sume negative.
    * Blochează retragerile care ar duce la o balanță negativă (Overdraft Protection).
    * Cerință obligatorie de balanță inițială pozitivă la deschiderea contului.
* **Raportare:** Generarea unui istoric tabelar care include Data, Suma, Balanța rezultată și Notele tranzacției.

---

## 🛠️ Detalii Tehnice

* **Limbaj:** C# (.NET 8.0)
* **Concepte OOP utilizate:**
    * `Properties` cu logică de calcul (getters).
    * `Static fields` pentru managementul semințelor (seeds) de cont.
    * `Records` pentru imuabilitatea datelor tranzacțiilor.
    * `Exception Handling` (ArgumentOutOfRangeException, InvalidOperationException).


---

## 📂 Structura Codului

* **`BankAccount.cs`**: Logica principală a contului (Depuneri, Retrageri, Calcul Balanță).
* **`Transaction.cs`**: Record-ul care stochează detaliile fiecărei operațiuni.
* **`Program.cs`**: Punctul de intrare care testează scenariile de succes și tentativele de fraudă/eroare.

---

## 🚀 Cum rulezi aplicația?

1. Descarcă sau clonează repository-ul.
2. Deschide soluția `BankAccount.slnx` în Visual Studio 2022 sau VS Code.
3. Rulează proiectul (`F5` sau `dotnet run`).

### Exemplu de Output în Consolă:
```text
Account 1234567890 was created for Maria with 1000 initial balance.
500
600
Exception caught trying to overdraw
System.InvalidOperationException: Not sufficient funds for this withdrawal...
