# Webservices - Lektion 5: ResponseEntity & Docker

## Response

När vi skickar ett svar (Response) från en webbtjänst till en klient måste vi definiera:

- **Body** – Innehållet i svaret (resultatet).
- **Header** – Metadata om svaret, t.ex. innehållstyp och datum.
- **StatusCode** – Anger om requesten lyckades eller inte.
- **Polymorphism** – Möjlighet att skicka olika typer av svar beroende på situation.

---

## Status Codes

HTTP-statuskoder förklarar **om requesten lyckades** och om inte, **vad som gick fel**:

| Kod | Betydelse |
|------|-----------|
| **200** | OK |
| **400** | Bad Request |
| **404** | Not Found |
| **500** | Internal Server Error |

---

## Headers

Headers används för att **förmedla metadata** mellan **Request** och **Response**.

Exempel:
- `Content-Type`
- `Date`

Headers kan konfigureras specifikt i varje **@Mapping**-metod i Spring.

---

## Body

Body är själva **innehållet** som returneras till klienten, t.ex. ett JSON-objekt, text eller annan data.

---

## ResponseEntity

`ResponseEntity` i Spring representerar ett **HTTP-svar**, inklusive:
- **Headers**
- **Body**
- **Status**

Liknande objekt i .NET: `IAction`.

Viktiga metoder:
- `.build()` – Bygger upp ett svar utan innehåll.
- `.body()` – Bygger upp ett svar med innehåll.

---

## Docker

Docker används för att paketera applikationen och dess beroenden i en **container**.

### Fördelar
- Alla använder **exakt samma miljö** → "Works on every machine".
- Programmet kan köras på:
  - Lokala datorer
  - Servrar
  - Molnplattformar
- Kan flyttas mellan olika operativsystem.

### Nyckelidé
> Docker säkerställer att applikationen fungerar likadant i alla miljöer.

---

## Sammanfattning
- `ResponseEntity` används för att kontrollera exakt **hur svaret till klienten ska se ut**.
- Docker säkerställer att applikationen och dess miljö är **konsistenta** oavsett var den körs.

