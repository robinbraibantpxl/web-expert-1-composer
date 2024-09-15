### Composer gebruiken

Net zoals bij npm zitten de Composer pakketten gebundeld op 1 plaats: [Packagist](https://packagist.org/).
Je kan ook hier zoeken naar functionaliteiten die je nodig hebt. Laravel, het framework dat we gaan
gebruiken is ook gewoon een Composer pakket.

### Opdracht

Maak lokaal op jouw toestel een map `composer_voorbeeld` aan en open deze map met jouw IDE.

Om Composer te gebruiken in het project is een `composer.json` bestand het enige wat je nodig
hebt. In dit bestand worden alle dependencies van het project gedefinieerd. Standaard bevindt dit bestand
zich in de **root** van het project.

Om gebruik te maken van dependencies, kan je in het bestand, een `require` key definiëren.
Bijvoorbeeld een logger
[`monolog/monolog`](https://packagist.org/packages/monolog/monolog).

```
{
    "require": {
        "monolog/monolog": "3.*"
    }
}
```


Om deze dependencies te installeren gaan we het **update** commando gebruiken. In de
**root** van je project voer je **`composer update`** uit. Dit
commando zal nu een
aantal dingen in orde brengen.

- Er zal een `composer.lock` bestand aangemaakt worden waarin alle dependencies zullen
  geschreven worden volgens hun aangegeven versie. Werk je samen in een team, dan is het van belang om het
  `composer.lock` bestand mee te committen zodat iedereen die met het project werkt, met
  dezelfde dependencies werkt.

- Daarna zal het **`install`** commando uitgevoerd worden. Hiermee zullen de
  dependencies in een vendor map gedownload worden. Wanneer er al een `composer.lock` bestand
  in het project aanwezig is, kan je gewoon het **`composer install`** commando
  runnen.

Eens je composer structuur opstaat, kan je nieuwe dependencies installeren met het `composer
require` commando. Als voorbeeld gaan we een
[Chalk pakket](https://packagist.org/packages/tdtrung17693/php-chalk) installeren:

``composer require tdtrung17693/php-chalk``