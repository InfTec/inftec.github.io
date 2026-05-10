---
title: Doodle-Poodle Datenschutzerklärung
description: Datenschutzerklärung für das Mal- und Rate-Spiel Doodle-Poodle der InfTec GmbH.
---

<!--
  Diese Datei ist eine saubere Ableitung von
  docs/privacy-policy.de.md aus dem (privaten) Doodle-Poodle
  App-Repository. Bearbeitungshinweise und Hosting-Checkliste
  sind entfernt. Bei jeder Revision mit der Quelle synchron halten.
-->

<p class="lang-switcher"><a href="../">English</a> · <strong>Deutsch</strong></p>

**Inkrafttreten:** 2026-05-10
**Zuletzt aktualisiert:** 2026-05-10

---

## Wer wir sind

Doodle-Poodle ist ein Mal- und Rate-Spiel für Kinder, herausgegeben
von der **InfTec GmbH** («wir»), mit Sitz in der **Schweiz**.

Kontakt für Datenschutzanfragen: **info@inftec.ch**.

## Zusammenfassung in einfacher Sprache

- Wir erfassen **keine** personenbezogenen Daten von Ihnen oder Ihrem Kind.
- Wir verfolgen **kein** Verhalten, keine Identität und keinen Standort.
- Die Zeichnungen Ihres Kindes verlassen das Gerät nie — sie werden
  von einem kleinen Modell für maschinelles Lernen erkannt, das
  lokal auf dem Smartphone oder Tablet läuft.
- Auf dem Gerät gespeichert werden nur: die Anzahl der verdienten
  Belohnungen («Knochen») des Kindes, die gewählte Sprache und ein
  Status, ob das Pro-Upgrade aktiv ist. Eine Deinstallation der App
  löscht alles davon.
- Familienfreundliche Werbung (sofern aktiviert) und einmalige Käufe
  werden von Google bzw. Apple gemäss deren eigenen
  Datenschutzbedingungen abgewickelt.

Wenn Sie die formelle Version lesen möchten, lesen Sie weiter.

---

## Welche Daten die App verarbeitet

### Daten, die nur auf dem Gerät gespeichert werden

Die App speichert eine kleine Menge an Daten auf dem Gerät, damit
das Spiel zwischen den Sitzungen funktioniert. Nichts davon wird
übermittelt, nichts davon identifiziert das Kind, und eine
Deinstallation der App entfernt alles.

| Auf dem Gerät gespeichert | Zweck | Speicherort |
|---|---|---|
| Anzahl verdienter Belohnungen («Knochen») | Dem Kind seinen Fortschritt anzeigen | Documents-Verzeichnis der App (einzelne JSON-Datei) |
| Sprachpräferenz (`en` / `de`) | Die Benutzeroberfläche in der gewählten Sprache anzeigen | Geteilte Einstellungen des Betriebssystems |
| Pro-Upgrade-Status | Vollständige Kategorienliste freischalten | Geteilte Einstellungen des Betriebssystems |
| Zähler für abgeschlossene Runden | Zeitliche Steuerung der periodischen Pro-Upgrade-Aufforderung | Geteilte Einstellungen des Betriebssystems |

Die erkannten Zeichnungen selbst existieren nur im Arbeitsspeicher,
während das Kind zeichnet, und werden zwischen den Runden verworfen.

### Daten, die lokal verarbeitet und verworfen werden

Während das Kind zeichnet, werden die Striche in einen kleinen
Bildtensor umgewandelt und durch ein Modell für maschinelles Lernen
geführt, das in der App enthalten ist. Das Modell verlässt das
Gerät nie, die Eingaben verlassen das Gerät nie, und die Vorhersage
wird unmittelbar von der Benutzeroberfläche verwendet, um die drei
besten Tipps anzuzeigen. Weder die Zeichnung noch die Vorhersage
werden gespeichert oder übermittelt.

### Daten, die wir nicht erfassen

Wir erfassen, übermitteln und verkaufen weder:

- Namen, E-Mail-Adressen, Telefonnummern oder andere Kontaktdaten
- Konto- oder Anmeldedaten (die App hat kein Konto-System)
- Fotos, Kontakte, Standort, Mikrofon- oder Kameradaten
- Werbe-IDs oder Geräte-IDs
- Absturzberichte oder Analyse-Ereignisse
- Verhaltensprofile irgendeiner Art

Die App hält die `INTERNET`-Berechtigung ausschliesslich, damit die
eingebetteten SDKs von Google AdMob und Google Play Billing ihre
jeweiligen Google-Endpunkte erreichen können. Zeichnungen,
Tonaufnahmen, Erkennungsergebnisse, Einstellungen und alle anderen
vom Kind erstellten Inhalte verlassen das Gerät nie.

## Drittanbieter-Dienste

Die App bindet zwei Google-SDKs ein. Beide sind erforderlich, um
die jeweiligen Funktionen bereitzustellen; beide sind so
konfiguriert, dass die Datenexposition minimiert wird.

### Google AdMob (Banner-Werbung, nur familienfreundliches Inventar)

Banner-Werbung wird von Google AdMob unter Verwendung des
familienfreundlichen Werbeinventars eingeblendet. Die Integration
ist gemäss Googles «Designed for Families»-Anforderungen
konfiguriert:

- `tagForChildDirectedTreatment` ist auf `yes` gesetzt — Google
  behandelt die Anfrage als für eine an Kinder gerichtete App und
  liefert ausschliesslich familienfreundliches Inventar aus.
- `tagForUnderAgeOfConsent` ist auf `yes` gesetzt.
- Die maximale Werbeinhaltsbewertung ist auf `G` gesetzt.
- Nur nicht personalisierte Werbung — Google verwendet die Anfrage
  nicht, um ein Verhaltensprofil aufzubauen.
- Keine Interstitial- oder Rewarded-Ads an störenden Positionen;
  Werbung erscheint ausschliesslich auf den Bildschirmen Home und
  Einstellungen und unterbricht nie das Spiel.
- Das Pro-Upgrade entfernt die Werbung vollständig.

Die Datenschutzpraktiken von AdMob selbst sind unter
[`policies.google.com/privacy`](https://policies.google.com/privacy)
und [`support.google.com/admob/answer/6128543`](https://support.google.com/admob/answer/6128543)
dokumentiert.

### Apple App Store / Google Play (In-App-Käufe)

Doodle-Poodle bietet ein einziges, optionales, einmaliges
Pro-Upgrade an. Der Kauf selbst wird von Apple oder Google
abgewickelt, nicht von uns. Wir erhalten lediglich das Ergebnis
der Transaktion (gekauft / nicht gekauft), damit wir die
Pro-Funktionen auf dem Gerät freischalten können. Wir sehen weder
Name, E-Mail-Adresse noch Zahlungsdaten.

Der Einstiegspunkt zum Kauf ist durch eine Eltern-Sicherheitsabfrage
(eine kleine Rechenaufgabe) geschützt, damit er nicht versehentlich
von einem Kind ausgelöst werden kann.

Die Datenschutzpraktiken von Apple sind unter
[`apple.com/privacy`](https://www.apple.com/privacy/) dokumentiert,
die von Google unter
[`policies.google.com/privacy`](https://policies.google.com/privacy).

### Keine Analytik, keine Absturzberichte, kein Drittanbieter-Tracking

Doodle-Poodle verwendet weder Firebase, Amplitude, Mixpanel,
Sentry, Crashlytics noch ein anderes Analyse- oder
Absturzberichts-SDK. Es gibt keine Drittanbieter-Tracker, keine
Fingerprinting-Bibliotheken und keine SDKs zur Werbeattribution.

## Datenschutz für Kinder (COPPA, GDPR-K)

Doodle-Poodle ist für Kinder konzipiert. Wir halten uns an:

- **COPPA** (US Children's Online Privacy Protection Act) — wir
  erfassen keine personenbezogenen Daten von Personen unter 13
  Jahren, daher ist keine elterliche Zustimmung erforderlich.
- **GDPR-K** (EU-Datenschutz-Grundverordnung, Artikel 8) —
  dasselbe gilt: wir erfassen keine personenbezogenen Daten von
  Nutzerinnen und Nutzern, unabhängig vom Alter.
- **Apple Kids Category** und **Google Play Designed for Families**
  Programmanforderungen — keine Drittanbieter-Analytik, keine
  verhaltensbasierte Werbung, Eltern-Sicherheitsabfrage vor jedem
  Kauf oder externen Link.

Sollten Sie der Meinung sein, dass Ihr Kind dennoch
personenbezogene Daten an uns weitergegeben hat (wir wissen nicht,
wie das angesichts unseres Designs geschehen könnte, möchten aber
auf der sicheren Seite sein), kontaktieren Sie uns bitte unter der
oben angegebenen E-Mail-Adresse und wir werden alle vorhandenen
Daten löschen — wir gehen aber davon aus, dass wir nichts finden
werden.

## Wie lange wir Daten aufbewahren

Wir speichern keine personenbezogenen Daten, daher gibt es nichts
aufzubewahren. Die oben aufgeführten Daten auf dem Gerät bleiben
bis zur Löschung der App oder bis zum Leeren ihres Speichers
erhalten.

## Ihre Rechte

Da wir keine personenbezogenen Daten erfassen, sind die
Betroffenenrechte gemäss DSGVO (Auskunft, Berichtigung, Löschung,
Datenübertragbarkeit, Widerspruch) praktisch nicht anwendbar: es
gibt nichts, worüber Auskunft erteilt werden könnte, nichts zu
berichtigen, zu löschen oder zu übertragen. Sie können uns jedoch
jederzeit unter der oben angegebenen E-Mail-Adresse mit Fragen zu
dieser Erklärung oder unseren Praktiken kontaktieren.

Wenn Sie die auf dem Gerät gespeicherten Daten der App löschen
möchten, ohne die App zu deinstallieren, können Sie dies über die
App-Speicher-Verwaltung des Betriebssystems tun (auf Android:
Einstellungen → Apps → Doodle-Poodle → Speicher → Daten löschen;
auf iOS: die App löschen und neu installieren).

## Sicherheit

Der lokale Speicher der App stützt sich auf das Sicherheitsmodell
des Host-Betriebssystems (sandbox-gekapselte App-Daten,
Verschlüsselung auf Betriebssystem-Ebene wenn vom Nutzer aktiviert).
Da wir nichts übermitteln, gibt es keine Netzwerk-Angriffsfläche
für die von uns verarbeiteten Daten.

## Änderungen dieser Erklärung

Wenn wir diese Erklärung wesentlich ändern — zum Beispiel, wenn
Werbung oder In-App-Käufe erstmals aktiviert werden — aktualisieren
wir das Datum «Zuletzt aktualisiert» und veröffentlichen einen klar
sichtbaren Hinweis im Bereich Einstellungen → Über der App. Für
jede Änderung, die sich darauf auswirkt, welche Daten das Gerät
verlassen (derzeit keine), gewähren wir mindestens 30 Tage
Vorankündigung in der App, bevor die Änderung in Kraft tritt.

## Kontakt

Fragen, Anfragen oder Bedenken zu dieser Erklärung:
**info@inftec.ch**

Postanschrift (für formelle Datenschutzanfragen):
**InfTec GmbH, Grubenstrasse 7b, 3322 Urtenen-Schönbühl, Schweiz**
