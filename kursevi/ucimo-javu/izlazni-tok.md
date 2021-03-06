---
title: Izlazni tok
layout: lekcija-java
permalink: /java-izlazni-tok
---

Klasa [`OutputStream`](https://docs.oracle.com/javase/7/docs/api/java/io/OutputStream.html) šalje čiste bajtove podataka na neko odredište, npr. konzolu ili mrežni server. Ova je klasa apstraktna, isto kao i `InputStream`.

## Metode

Mnoge metode u biblioteci Java klasa napravljene su tako da vraćaju objekte tipa `OutputStream`, umjesto objekte iz njenih specifičnih podklasa. Mnoge metode klase `OutputStream` su općenito korisne. To su:

```java
public abstract void write(int b) throws IOException
public void write(byte[] data) throws IOException
public void write(byte[] data, int offset, int length) throws IOException
public void flush() throws IOException
public void close() throws IOException
```

Nekoliko različitih `write()` metoda šalju čiste bajtove podataka svakom procesu koji osluškuje dati tok.

Ponekad operacijski sustav gomila izlazne tokove ("baferuje strim") zbog boljih performansi. To znači da se bajtovi prije ispisa akumuliraju u spremnik (bafer), čija veličina može biti od nekoliko bajtova do nekoliko tisuća bajtova. Kad se on napuni, svi podaci se ispisuju odjednom. Metoda `flush()` pokrenut će, međutim, ispis bez obzira da li je spremnik pun ili nije.

Primijetite da se ovdje radi o procesu na razini operacijskog sustava, i ovo nije isto što i taloženje koje provodi klasa `BufferedOutputStream`, koje izvodi Java runtime. Međutim, poziv metode `flush()` trebao bi isprazniti oba spremnika.

Metoda `close()` zatvara tok i otpušta resurse koji su s njim povezani. Jednom kad je tok zatvoren, pokušaj pisanja u njega izbacit će `IOException`.

## Primjer izlaznog toka

Izlazni tokovi koje ste do sad upoznali su `System.out` i `System.err`. Sljedeći primjer koristi metode `write()` i `flush()` iz klase `OutputStream`, da bi na `System.out` ispisao string “Hello World”

{:.ulaz}
```java
import java.io.*;

public class HelloOutputStream {
  public static void main(String[] args) {

    String s = "Hello World\r\n";
    byte[] b = new byte[s.length()];  // prevodi u niz bajtova
    s.getBytes(0, s.length()-1, b, 0);

    try {
      System.out.write(b);
      System.out.flush();
    }
    catch (IOException e) {
      System.err.println(e);
    }

  }
}
```

```
% javac HelloOutputStream.java
% java HelloOutputStream
 ello World
```

Primijetite da program ne radi baš onako kako bi se očekivalo nego proguta prvi znak (napomena: ovaj primer je zastareo).
