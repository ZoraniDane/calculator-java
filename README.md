LOC(lines of code) 214 (188+26)

Neformalan pregled: Calculator.java

Pozitivne strane:
    • Jasna razdvojenost između različitih operacija.
    • Korištenje statičkih klasa i metoda za definisanje operacija.
Preporuke:
    1. Izvođenje računa:
        ◦ Metoda Calculate je rekurzivna, što može biti neefikasno za duge izraze zbog mogućnosti prepunjenja steka. Preporučujem iterativni pristup.
        ◦ Bolje rukovanje greškama, posebno za deljenje s nulom, može poboljšati stabilnost.
    2. Razdvojenost logike:
        ◦ Razdvojiti logiku parsiranja izraza i izvođenja operacija u zasebne metode ili klase radi bolje čitljivosti i održavanja.
    3. Optimizacija:
        ◦ Preporučujem izbegavanje višestrukog prolaska kroz listu operacija i brojeva. Umesto toga, koristi jednu petlju za izvođenje svih operacija prema prioritetu.
    4. Validacija ulaza:
        ◦ Dodati više provera valjanosti ulaza kako bi se osiguralo da korisnik unosi ispravan matematički izraz.

 Neformalan pregled: Start.java
 
 Pozitivne strane:
    • Jednostavna i čitljiva implementacija glavne petlje koja omogućava unos izraza i ispis rezultata.
Preporuke:
    1. Resursi:
        ◦ Stvaranje novog Scanner objekta unutar petlje nije efikasno. Bolje je inicijalizirati Scanner samo jednom izvan petlje.
        ◦ Osigurati zatvaranje Scanner objekta na kraju programa.
    2. Uslovni izrazi:
        ◦ Uslovni izraz if (Expression.equals("exit")) može koristiti equalsIgnoreCase za bolju korisničku podršku.

    Statička analiza:Calculator.java

Calculator.java 1 of 9 problems: - 1. import java.util.list; - Move his file to a named package.). Sonarlint (java:S1220)
Calculator.java 2 of 9 problems: - 1. import java.util.list; - Calculator.java is a non-project file, only syntax errors are reported  Java(16)
Calculator.java 3 of 9 problems: - 4. public class Calculator { - Add a private constructor to hide the implicit public one  Sonarlint (java:S1118)
Calculator.java 4 of 9 problems: - 18.public static String ToString() { - Rename method "ToString" to prevent any misunderstanding/clash with method "toString" defined in superclass "java.lang.Object".Sonarlint (java:S1845)
Calculator.java 5 of 9 problems: - 18.public static String ToString() { - Rename this method name to match the regular expression '^[a-z][a-zA-Z0-9]*$'.Sonarlint (java:S100)
Calculator.java 6 of 9 problems: - 24.public static String Run(String expression) {
- Rename this method name to match the regular expression '^[a-z][a-zA-Z0-9]*$'.Sonarlint (java:S100)
Calculator.java 7 of 9 problems: - 70.String textResult = Float.toString(finalResult); - Immediately return this expression instead of assigning it to the temporary variable "textResult". Sonarlint (java:S1488)
Calculator.java 8 of 9 problems: - 74. private static void Calculate(List<Float> numbers, List<String> operations) {
 - Rename this method name to match the regular expression '^[a-z][a-zA-Z0-9]*$'. Sonarlint (java:S100)
Calculator.java 9 of 9 problems - 183.return; - Sonarlint (java:S3626)

    Statička analiza:Start.java
  
Start.java 1 of 5 problems: - 1. import java.util.list; - Move his file to a named package. Sonarlint (java:S1220)
Start.java 2 of 5 problems: - 1. import java.util.list; - Start.java is a non-project file, only syntax errors are reported Java(16)
Start.java 3 of 5 problems: - 6. String Expression; Rename this local variable to match the regular expression '^[a-z][a-zA-Z0-9]*$'.^[а-з][а-зА-З0-9]*$'.)sonarlint (java:S117)
Start.java 4 of 5 problems: - 8. System.out.println("Enter expression here (type 'exit' to quit):");.Replace this use of System.out by a logger.sonarlint(java:S106)
Start.java 5 of 5 problems: - 19.System.out.println(Calculator.Run(Expression));
Replace this use of System.out by a logger( System.out).sonarlint(java:S106)
  
Urađeno uz pomoć ChatGPT i SonarLint
    
