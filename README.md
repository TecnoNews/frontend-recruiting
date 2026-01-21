# Frontend Recruiting

## 🎯 Obiettivo

L'obiettivo di questo esercizio è realizzare una **piccola applicazione frontend tipo dashboard** che permetta di **visualizzare, creare, modificare ed eliminare post**, associati a utenti, consumando delle **API REST** fornite da un backend fake.

L'applicazione dovrà simulare uno scenario reale in cui il frontend interagisce con un server remoto, gestendo:

- Recupero dati asincrono
- Stato dell'applicazione
- Interazioni utente
- Visualizzazione strutturata dei dati tramite tabelle avanzate

---

## 🧩 Funzionalità richieste

### 🔐 Autenticazione (fake)
- Pagina di login
- Login simulato tramite chiamata API
- Gestione dello stato dell'utente loggato

### 📝 Post
- Lista dei post
- Visualizzazione in tabella tramite **Material React Table**  con paginazione e filtri
- Creazione di un nuovo post tramite **Drawer**
- Navigazione verso il dettaglio del singolo post
- Modifica ed eliminazione di un post
- Tornando dalla pagina di dettaglio alla lista, **lo stato della tabella deve essere preservato** (filtri, ordinamento, paginazione, scroll)

### 👤 Utenti
- Lista degli utenti
- Visualizzazione in tabella tramite **Material React Table** con paginazione e filtri
- Creazione di un nuovo utente tramite **Drawer**
- Navigazione verso il dettaglio del singolo utente
- Modifica ed eliminazione di un utente
- Mostrare i posts dell'utente nel dettaglio dell'utente
- Tornando dalla pagina di dettaglio alla lista, **lo stato della tabella deve essere preservato** (filtri, ordinamento, paginazione, scroll)

---

## 🛠 Stack richiesto

Il progetto **deve** essere sviluppato utilizzando il seguente stack:

- **React**
- **TypeScript**
- **Material UI (MUI)**
- **Material React Table** (basato su TanStack Table)

### Librerie consigliate (non obbligatorie)
- Axios
- TanStack Query
- React Router
- Zustand (state management)
- React Hook Form (gestione form)
- Zod (validazione dei dati)

---

## 🧪 Backend fake – JSON Server

Per simulare un backend REST, verrà utilizzato **json-server**.

### 📦 Installazione

Assicurarsi di avere Node.js installato, quindi eseguire:

```bash
npm install -g json-server
```

Oppure in locale:

```bash
npx json-server --watch db.json --port 3001
```

---

### 📁 File `db.json`

Creare un file `db.json` nella root del progetto con il seguente contenuto:

```json
{
  "users": [
    {
      "id": 1,
      "name": "Mario Rossi",
      "email": "mario@example.com",
      "password": "password123"
    }
  ],
  "posts": [
    {
      "id": 1,
      "userId": 1,
      "title": "Il mio primo post",
      "content": "Contenuto di esempio",
      "createdAt": "2025-01-10T10:30:00Z"
    }
  ]
}
```

---

### 🔗 API disponibili automaticamente

Una volta avviato il server, saranno disponibili endpoint REST come:

```
GET    /users
GET    /posts
GET    /posts?userId=1
POST   /posts
PUT    /posts/:id
DELETE /posts/:id
```

Base URL:
```
http://localhost:3001
```

---

### 🔐 Login simulato

Il login può essere simulato con una chiamata GET:

```
GET /users?email=mario@example.com&password=password123
```

Se la risposta contiene un utente, il login è da considerarsi valido.

---

## 📤 Consegna

Il candidato dovrà fornire:

- Repository GitHub pubblico o privato
- README con istruzioni per l'avvio del progetto
- Codice funzionante e avviabile

---

Buon lavoro 🚀
