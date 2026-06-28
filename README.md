# C4 ERP Case Study

C4-Diagramme für eine zentrale Angular-Webanwendung in einem ERP-System mit den Domänen Finance, HR, Sales und Inventory.

## Architekturidee

Das Frontend wird als modularer Frontend-Modulith aufgebaut. Jede Domäne erhält einen eigenen lazy-loaded Feature-Bereich.

Gemeinsame UI-Komponenten liegen in einem Shared UI / Design System, damit das Look & Feel über alle Domänen konsistent bleibt.

Globaler Zustand bleibt klein und enthält nur domänenübergreifende Informationen wie Benutzer, Berechtigungen, Tenant, Sprache und Layout. Fachlicher Zustand bleibt in der jeweiligen Domäne.