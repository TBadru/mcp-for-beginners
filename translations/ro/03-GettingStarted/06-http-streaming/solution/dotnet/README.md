<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "4eb6a48c54555c64b33c763fba3f2842",
  "translation_date": "2025-06-18T06:19:18+00:00",
  "source_file": "03-GettingStarted/06-http-streaming/solution/dotnet/README.md",
  "language_code": "ro"
}
-->
# Rularea acestui exemplu

## -1- Instalează dependențele

```bash
dotnet restore
```

## -2- Rulează exemplul

```bash
dotnet run
```

## -3- Testează exemplul

Deschide un terminal separat înainte să rulezi comanda de mai jos (asigură-te că serverul este încă pornit).

Cu serverul pornit într-un terminal, deschide un alt terminal și rulează următoarea comandă:

```bash
npx @modelcontextprotocol/inspector http://localhost:3001
```

Aceasta ar trebui să pornească un server web cu o interfață vizuală care îți permite să testezi exemplul.

> Asigură-te că **Streamable HTTP** este selectat ca tip de transport, iar URL-ul este `http://localhost:3001/mcp`.

Once the server is connected: 

- try listing tools and run `add`, cu argumentele 2 și 4, ar trebui să vezi 6 ca rezultat.
- mergi la resources și resource template și apelează "greeting", tastează un nume și ar trebui să vezi un mesaj de întâmpinare cu numele pe care l-ai introdus.

### Testare în modul CLI

Poți lansa direct în modul CLI rulând următoarea comandă:

```bash 
npx @modelcontextprotocol/inspector --cli http://localhost:3001 --method tools/list
```

Aceasta va lista toate uneltele disponibile pe server. Ar trebui să vezi următorul rezultat:

```text
{
  "tools": [
    {
      "name": "AddNumbers",
      "description": "Add two numbers together.",
      "inputSchema": {
        "type": "object",
        "properties": {
          "a": {
            "description": "The first number",
            "type": "integer"
          },
          "b": {
            "description": "The second number",
            "type": "integer"
          }
        },
        "title": "AddNumbers",
        "description": "Add two numbers together.",
        "required": [
          "a",
          "b"
        ]
      }
    }
  ]
}
```

Pentru a apela o unealtă tastează:

```bash
npx @modelcontextprotocol/inspector --cli http://localhost:3001 --method tools/call --tool-name AddNumbers --tool-arg a=1 --tool-arg b=2
```

Ar trebui să vezi următorul rezultat:

```text
{
  "content": [
    {
      "type": "text",
      "text": "3"
    }
  ],
  "isError": false
}
```

> ![!TIP]
> De obicei este mult mai rapid să rulezi inspectorul în modul CLI decât în browser.
> Citește mai multe despre inspector [aici](https://github.com/modelcontextprotocol/inspector).

**Declinare de responsabilitate**:  
Acest document a fost tradus folosind serviciul de traducere AI [Co-op Translator](https://github.com/Azure/co-op-translator). Deși ne străduim pentru acuratețe, vă rugăm să rețineți că traducerile automate pot conține erori sau inexactități. Documentul original în limba sa nativă trebuie considerat sursa autorizată. Pentru informații critice, se recomandă traducerea profesională realizată de un specialist uman. Nu ne asumăm responsabilitatea pentru eventualele neînțelegeri sau interpretări greșite care pot apărea în urma utilizării acestei traduceri.