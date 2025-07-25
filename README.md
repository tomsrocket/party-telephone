# Guestbook Retro Phone

* Altes Telefon aus den 30er Jahren kaufen
* Innereien rausnehmen
* Raspberry Pi Zero einbauen mit USB-Soundkarte
* Alles genauso machen wie hier beschrieben: https://github.com/nickpourazima/rotary-phone-audio-guestbook
* Meine Dateien aus dem `source` Verzeichnis nutzen, da gibts das Zusatzfeature: Man kann zufällige Nachrichten abhören, die von vorhergehenden Telefon-Nutzern eingesprochen wurden.

## Befehle

Lokal
```bash
# runterladen
cd source
rsync -h -v -r -P -t admin@zerofon.local:/home/admin/rotary-phone-audio-guestbook .

# deployen - ACHTUNG: überschreibt ggf. auch die samples (Ansagesprüche) auf dem phone
cd source/rotary-phone-autio-guestbook
rsync -h -v -r -P -t . admin@zerofon.local:/home/admin/rotary-phone-audio-guestbook 
```

Eingeloggt
```bash
# Neustarten
sudo systemctl restart audioGuestBook

# Log anschauen
journalctl -u audioGuestBook.service -f
```



## Ansagesprüche Ideen

Hey! Du hast den Hörer abgehoben – das bedeutet, du hast jetzt das Wort. Was willst du der Welt, der Zukunft oder einfach den nächsten Partygästen sagen? Teile einen Gedanken, einen Rat fürs Leben oder deinen Lieblingswitz. Deine Nachricht beginnt… jetzt



„Dies ist kein Telefon – es ist ein Wunschbrunnen, ein Beichtstuhl, ein Lautsprecher ins Universum. Sag uns, was zählt: ein Geheimnis, ein Traum, ein Rat fürs Leben. Was auch immer du sagst, es bleibt – hier, in diesem Hörer.“