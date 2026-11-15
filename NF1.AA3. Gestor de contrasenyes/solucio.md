# Gestió de Contrasenyes
## Fase 1: Anàlisi i Justificació

### 1. Introducció i Justificació
Després del problema de seguretat a EverPia provocat pel compromís d'un compte tècnic amb una contrasenya feble o reutilitzada, és necessari establir una política de seguretat de credencials.

L'ús de contrasenyes febles o repetides en diferents serveis suposa un risc elevat:
* **Atac de diccionari:** Proves automàtiques de combinacions de paraules i claus habituals fins a trobar la credencial correcta.
* **Credential stuffing:** Utilització de parelles d'usuari i contrasenya obtingudes en altres serveis compromesos per accedir als sistemes corporatius.

Un gestor de contrasenyes permet emmagatzemar totes les credencials de forma xifrada en un magatzem segur (*Vault*). Així, els usuaris només han de recordar una contrasenya mestre (*Master Password*), mentre el gestor crea i guarda claus úniques i complexes per a cada servei.

---

### 2. Comparativa Tècnica
A continuació es mostra la comparativa entre la solució en el núvol (Bitwarden) i la solució local (KeePassXC):

| Característica Tècnica | Bitwarden (Alternativa Online / Núvol) | KeePassXC (Alternativa Offline / Escriptori) |
| :--- | :--- | :--- |
| **Model d'emmagatzematge** | Servidor al núvol (xifrat en origen/client) | Arxiu local en disc (format KDBX) |
| **Sincronització** | Automàtica entre tots els dispositius (Mòbil, Web, PC) | Manual (cal moure l'arxiu KDBX o usar un núvol propi) |
| **Model de seguretat** | Xifratge d'extrem a extrem (Zero-Knowledge) | Xifratge local fort de la base de dades KDBX |
| **Accés des de dispositius** | Molt fàcil (Navegador, Mòbil, App d'escriptori, Web) | Requereix instal·lar l'aplicació a cada equip |
| **Llicència i Cost** | Open Source / Freemium (gratuït i opció de pagament) | Open Source i 100% Gratuït |

---

### 3. Avantatges i Inconvenients
Resum dels punts forts i febles de cada model:

#### Bitwarden (Online / Núvol)
* **Avantatges:** Sincronització immediata entre equips i mòbils, facilitat d'ús amb l'extensió del navegador i gestió centralitzada.
* **Inconvenients:** Requeriment de connexió a Internet per a la sincronització i emmagatzematge en servidors externs xifrats.

#### KeePassXC (Offline / Escriptori)
* **Avantatges:** Control total local de les dades sense dependre de servidors externs.
* **Inconvenients:** Risc de pèrdua de dades si no es fan còpies de seguretat i sincronització manual entre dispositius.

---

### 4. Recomanació
Com a elecció final per a l'empresa EverPia, es recomana oficialment la selecció de **Bitwarden**.

Aquesta decisió es justifica per la necessitat del personal tècnic d'accedir als serveis des de diferents equips i ubicacions. La sincronització automàtica i el xifratge d'extrem a extrem proporcionen la millor combinació de seguretat i facilitat d'ús per a l'equip.