### Milestone 1

Nel componente principale della nostra Vue App facciamo una chiamata API all’endpoint costruito nel progetto Laravel e recuperiamo tutti i progetti dal nostro back-end.
Stampiamo in console i risultati e verifichiamo di ricevere i dati correttamente.

### Milestone 2

Creiamo un nuovo componente ProjectCard, che corrisponde ad una card per visualizzare un progetto. Utilizziamo questo componente per visualizzare tutti i progetti ricevuti tramite API.

### Bonus:

Gestire la paginazione dei risultati
Buon lavoro e buon divertimento!

### Consigli

Per modificare il colore della topbar di vscode in progetti specifici:
CTRL + SHIFT + P
Selezionate "Preferences: Open Workbench Settings (JSON)"
Incollare il seguente codice:

```
{
  "workbench.colorCustomizations": {
    "titleBar.activeBackground": CODICE_COLORE,
    "titleBar.activeForeground": "#fff"
  }
}
```

Io uso il verde "#117F4E" per Vue ed il rosso "#AC3535" per Laravel, vanno inseriti al posto di CODICE_COLORE
