# Secure Delivery of Measurement Data

## Purpose

This document describes the secure delivery process for measurement data and random‑number exports.  
It ensures confidentiality, integrity, and authenticity using modern public‑key cryptography.

## Integrity: Digital Signatures

All exported files are digitally signed using minisign.

Customers can verify authenticity with:

minisign -Vm file.json -p publickey.txt<br>

This guarantees that the file originates from the project owner and has not been modified.

## Confidentiality: Public‑Key Encryption (Option)

If the customer provides a PGP public key (e.g., generated with Gpg4win/Kleopatra), all files and short messages can be encrypted directly for that key.

This enables full end‑to‑end encryption.

Encrypted content may include:

- files  
- metadata  
- short text (e.g., AES‑256 keys)  
- any sensitive information  

## Customer Workflow

1. The customer sends their PGP public key to the project owner.
2. The project owner encrypts the ZIP file using AES‑256 encryption.
3. The project owner encrypts the AES‑256 key with the customer’s PGP public key.
4. The project owner sends the ZIP file and the encrypted AES‑256 key to the email address specified by the customer.
5. The customer decrypts the data locally using their private key.


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

Alle drei Dateien werden als eine zip-Datei gesendet.

## Vertraulichkeit: Public‑Key‑Verschlüsselung (Option)

Stellt der Kunde einen PGP‑Public‑Key bereit (z. B. erzeugt mit Gpg4win/Kleopatra), können Dateien und kurze Texte direkt für diesen Schlüssel verschlüsselt werden.

Dies ermöglicht vollständige Ende‑zu‑Ende‑Verschlüsselung.

Verschlüsselbar sind:

- Dateien  
- Metadaten  
- kurze Texte (z. B. AES‑256‑Schlüssel)  
- beliebige vertrauliche Informationen  

## Ablauf für den Kunden

1. Der Kunde sendet seinen PGP‑Public‑Key an den Projektinhaber.  
2. Der Projektinhaber verschlüsselt die ZIP-Datei mit AES‑256‑Verschlüsselung.
3. Der Projektinhaber verschlüsselt den AES-256-Schlüssel mit dem PGP‑Public‑Key des Kunden.
4. Der Projektinhaber sendet die ZIP-Datei und den verschlüsselten AES-256-Schlüssel an die vom Kunden angegebende Email-Adresse.
6. Der Kunde entschlüsselt die Daten lokal mit seinem privaten Schlüssel.

## Unterstützte Schlüsseltypen

- PGP‑Public‑Keys (empfohlen; funktioniert mit Kleopatra‑Notizblock)  
- age‑Public‑Keys  
- SSH‑Public‑Keys (über age‑plugin‑ssh)

**Hinweis:** Minisign‑Public‑Keys dienen ausschließlich der Signaturprüfung und können nicht zur Verschlüsselung verwendet werden.

## Öffentlicher Schlüssel zur Signaturprüfung
untrusted comment: minisign public key

RWQWQuaj+ap04APBiGSwKclnZeciQjKeJLMFEmzsxP115uDGrNSt6F4M

