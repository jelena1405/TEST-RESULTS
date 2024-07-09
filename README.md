# TEST-RESULTS


import static org.junit.Assert.assertEquals;
import org.junit.Test;
import java.util.Arrays;

public class CalculatorTest {
    @Test
    public void testCalculate() {
        // Osnovne operacije
        assertEquals("9.0", Calculator.Run("4+5"));
        assertEquals("5.0", Calculator.Run("10-5"));
        assertEquals("21.0", Calculator.Run("3*7"));
        assertEquals("5.0", Calculator.Run("20/4"));

        // Kombinovane operacije
        assertEquals("14.0", Calculator.Run("2+3*4"));
        assertEquals("20.0", Calculator.Run("(2+3)*4"));

        // Testiranje sa negativnim brojevima
        assertEquals("1.0", Calculator.Run("-4+5"));
        assertEquals("5.0", Calculator.Run("10+-5"));

        // Testiranje sa decimalnim brojevima
        assertEquals("6.0", Calculator.Run("2.5+3.5"));
        assertEquals("10.0", Calculator.Run("10.1-0.1"));

        // Testiranje grešaka
        assertEquals("ERROR", Calculator.Run("10/0"));
        assertEquals("ERROR", Calculator.Run("4++5"));
        assertEquals("ERROR", Calculator.Run("5**2"));
    }
}





## Sistemsko Testiranje (Black Box Testing)

1. Osnovne operacije:
   - `4+5` rezultat: `9` (tačno)
   - `10-5` rezultat: `5` (tačno)
   - `3*7` rezultat: `21` (tačno)
   - `20/4` rezultat: `5` (tačno)

2. Kombinovane operacije:
   - `2+3*4` rezultat: `14` (tačno)
   - `(2+3)*4` rezultat: `20` (tačno)

3. Testiranje sa negativnim brojevima:
   - `-4+5` rezultat: `1` (tačno)
   - `10+-5` rezultat: `5` (tačno)

4. Testiranje sa decimalnim brojevima:
   - `2.5+3.5` rezultat: `6.0` (tačno)
   - `10.1-0.1` rezultat: `10.0` (tačno)

5. Testiranje grešaka:
   - `10/0` rezultat: Greška (deljenje sa nulom) (tačno)
   - `4++5` rezultat: Greška (neispravan izraz) (tačno)
   - `5**2` rezultat: Greška (neispravan operator) (tačno)
