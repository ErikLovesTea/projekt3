# Antiyoy Multiplayeri veebiklient

HTML-i, CSS-i ja JavaScriptiga tehtud brauseriklient Antiyoy-laadsele käigupõhisele strateegiamängule.

## Võimalused

- Mänguga liitumine ja mängu alustamise päring.
- Kuusnurksest mängulauast ülevaate kuvamine.
- Üksuste ja ehitiste ostmine valitud ruudule.
- Käigu lõpetamine ja alistumine.
- Mängija nime ja võtme salvestamine brauseri `localStorage`-isse.
- Mängu oleku värskendamine iga 1,5 sekundi järel.

## Käivitamine

Projekt koosneb ühest [index.html](index.html) failist ega vaja sõltuvuste paigaldamist.

Käivita repositooriumi kaustas staatiline veebiserver, näiteks Python 3 abil:

```sh
python -m http.server 8000
```

Ava [http://localhost:8000](http://localhost:8000), sisesta kasutajanimi ja vali **Join Game**.

## Serveriühendus

`index.html` failis olev `API_URL` on:

```text
https://tinkr.tech/sdb/projekt3/mang
```

Klient loeb mängu olekut `GET` päringuga ja saadab tegevused `POST` päringutena: `join`, `start`, `buy`, `end_turn` ja `surrender`.

Mängu reegleid ja olekut haldav server ei kuulu sellesse repositooriumisse. Kliendi kasutamine eeldab töötavat API-t; serveri kättesaadavus ja brauseri päringute lubamine määravad, kas mäng toimib.
