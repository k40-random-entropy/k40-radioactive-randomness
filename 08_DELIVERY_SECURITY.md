# Secure Delivery of Measurement Data

## Purpose

This document describes the secure delivery process for measurement data and random‑number exports.  
It ensures confidentiality, integrity, and authenticity using modern public‑key cryptography.

## Integrity: Digital Signatures

All exported files are digitally signed using minisign.

Customers can verify authenticity with:

minisign -Vm file.json -p publickey.txt<br>

This guarantees that the file originates from the project owner and has not been modified.

## Confidentiality: Public‑Key Encryption

If the customer provides a PGP public key (e.g., generated with Gpg4win/Kleopatra), all files and short messages can be encrypted directly for that key.

This enables full end‑to‑end encryption without passwords and without any shared secrets.

Encrypted content may include:

- files  
- metadata  
- short text (e.g., AES‑256 keys)  
- any sensitive information  

## Customer Workflow

1. Customer sends their PGP public key to the project owner.  
2. The project owner encrypts files and/or text directly for that key.  
3. The customer decrypts the data locally using their private key.

This workflow eliminates the need for password transmission.

## Supported Key Types

- PGP public keys (recommended; works with Kleopatra Notepad)  
- age public keys  
- SSH public keys (via age‑plugin‑ssh)

**Note:** Minisign public keys are used only for signature verification and cannot be used for encryption.

## Public Key for Signature Verification
untrusted comment: minisign public key

RWQWQuaj+ap04APBiGSwKclnZeciQjKeJLMFEmzsxP115uDGrNSt6F4M

---

# Sichere Übermittlung von Messdaten

## Zweck

Dieses Dokument beschreibt das sichere Verfahren zur Übermittlung von Messdaten und Zufallszahl‑Exporten.  
Es stellt Vertraulichkeit, Integrität und Authentizität durch moderne Public‑Key‑Kryptografie sicher.

## Integrität: Digitale Signaturen

Alle exportierten Dateien werden mit minisign digital signiert.

Der Kunde kann die Echtheit prüfen mit:

minisign -Vm Datei.json -p publickey.txt

Dies garantiert, dass die Datei vom Projektinhaber stammt und nicht verändert wurde.

## Vertraulichkeit: Public‑Key‑Verschlüsselung

Stellt der Kunde einen PGP‑Public‑Key bereit (z. B. erzeugt mit Gpg4win/Kleopatra), können Dateien und kurze Texte direkt für diesen Schlüssel verschlüsselt werden.

Dies ermöglicht vollständige Ende‑zu‑Ende‑Verschlüsselung ohne Passwörter und ohne gemeinsame Geheimnisse.

Verschlüsselbar sind:

- Dateien  
- Metadaten  
- kurze Texte (z. B. AES‑256‑Schlüssel)  
- beliebige vertrauliche Informationen  

## Ablauf für den Kunden

1. Der Kunde sendet seinen PGP‑Public‑Key an den Projektinhaber.  
2. Der Projektinhaber verschlüsselt Dateien und/oder Text direkt für diesen Schlüssel.  
3. Der Kunde entschlüsselt die Daten lokal mit seinem privaten Schlüssel.

Damit entfällt die Übermittlung von Passwörtern vollständig.

## Unterstützte Schlüsseltypen

- PGP‑Public‑Keys (empfohlen; funktioniert mit Kleopatra‑Notizblock)  
- age‑Public‑Keys  
- SSH‑Public‑Keys (über age‑plugin‑ssh)

**Hinweis:** Minisign‑Public‑Keys dienen ausschließlich der Signaturprüfung und können nicht zur Verschlüsselung verwendet werden.

## Öffentlicher Schlüssel zur Signaturprüfung
untrusted comment: minisign public key

RWQWQuaj+ap04APBiGSwKclnZeciQjKeJLMFEmzsxP115uDGrNSt6F4M

