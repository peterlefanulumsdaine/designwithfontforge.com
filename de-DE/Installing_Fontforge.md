---
published: true
layout: bookpage
weight: 15
category: Getting To Know FontForge
title: Installation von FontForge
---

Da es sich bei FontForge um freie Software handelt, können Sie Kopien ohne Nutzungseinschränkungen herunterladen, weitergeben und installieren - sowohl die kommerzielle als auch die persönliche Nutzung ist erwünscht.
Es handelt sich um eine von der Gemeinschaft gepflegte Anwendung, und jeder kann zum Quellcode beitragen.

FontForge ist in einfach zu installierenden Paketen für die Betriebssysteme Windows, Mac OS X und GNU+Linux erhältlich. 

### Installation von FontForge unter Windows

Für die offiziellen Windows-Builds ist eine [Installationsanleitung](http://fontforge.github.io/en-US/downloads/windows/) verfügbar, die von Jeremy Tan erstellt wurde.

### Installation von FontForge unter Mac OS X

Für die offiziellen Mac-Builds ist eine [Installationsanleitung](http://fontforge.github.io/en-US/downloads/mac/) verfügbar, die von Dr. Ben Martin erstellt wurde. 

### Installieren unter GNU/Linux

Die einfachste Methode, FontForge auf Ihren Linux-Rechner zu bekommen, ist die Verwendung des Paketspeichers Ihrer Linux-Distribution.

##### Debian oder Ubuntu

Das FontForge-Paket, das standardmäßig in Ubuntu 14.04 enthalten ist, stammt aus dem Jahr 2012, so dass es vorzuziehen ist, das aktuellere Paket aus dem FontForge [Personal Package Archive (PPA)](https://launchpad.net/~fontforge/+archive/ubuntu/fontforge) zu installieren.

Prüfen Sie, ob das Hilfsskript `add-apt-repository` installiert ist:
    
```sh
sudo apt-get install software-properties-common;
```

Fügen Sie das FontForge-PPA hinzu (der auch den Authentifizierungsschlüssel hinzufügt):
    
```sh
sudo add-apt-repository ppa:fontforge/fontforge;
```

Aktualisieren Sie die Software-Liste, um Pakete aus dem PPA aufzunehmen:
    
```sh
sudo apt-get update;
```

FontForge installieren:
    
```sh
sudo apt-get install fontforge;
```

##### Fedora

Um FontForge auf Ihrem Fedora Linux-Desktop-Rechner zu installieren, führen Sie den folgenden yum-Befehl als Root-Benutzer aus. 
Dies erfordert einen Download von etwa 10MiB.

```
yum install fontforge;
```

Wenn Sie keine Software auf Ihrem Fedora-Rechner kompiliert haben, erhalten Sie nach der Installation von gcc, automake, autoconf und anderen möglicherweise einen Fehler während der Ausführung von autogen.sh mit libtoolize. 
Wenn das der Fall ist, müssen Sie möglicherweise das Paket libtool-ltdl-devel auf Fedora oder ein ähnliches Entwicklungspaket auf einer anderen GNU+Linux-Distribution installieren.

Nach der Installation von yum sollten Sie in der Lage sein, FontForge über Ihr Menü oder direkt von der Konsole oder dem gnome-Terminal aus mit dem Befehl `fontforge` zu starten.

## Kompilieren Sie Ihre eigene Version von GitHub

GitHub ist ein Quellcode-Hosting-Service, bei dem jeder zur Entwicklung einer Software beitragen kann. Es speichert den aktuellen führenden Entwicklungsstand der Anwendung.
In einigen Fällen, vielleicht weil Sie eine Funktion nutzen möchten, die in den Veröffentlichungspaketen noch nicht verfügbar ist, möchten Sie vielleicht Ihre eigene Version von Github kompilieren.

Vollständige Anweisungen finden Sie unter <https://github.com/fontforge/fontforge/blob/master/INSTALL.md>

## Fehlersuche in der FontForge-Software

Weitere Informationen finden Sie im Abschnitt [Debugging](When_Things_Go_Wrong_With_Fontforge_Itself).
