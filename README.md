# C4 ERP Case Study

C4-Diagramme für eine zentrale Angular-Webanwendung in einem ERP-System mit den Domänen Finance, HR, Sales und Inventory.

## Architekturidee

Das Frontend wird als modularer Frontend-Modulith aufgebaut. Jede Domäne erhält einen eigenen lazy-loaded Feature-Bereich.

Gemeinsame UI-Komponenten liegen in einem Shared UI / Design System, damit das Look & Feel über alle Domänen konsistent bleibt.

Globaler Zustand bleibt klein und enthält nur domänenübergreifende Informationen wie Benutzer, Berechtigungen, Tenant, Sprache und Layout. Fachlicher Zustand bleibt in der jeweiligen Domäne.

Core Services bündeln technische Querschnittsthemen wie Authentifizierung, HTTP-Interceptor, Konfiguration und Fehlerbehandlung.

## Qualitätsanforderungen

Wartbarkeit: Domänentrennung
Erweiterbarkeit: Ergänzung neuer Domänen über eigenen FeautureSlot
Performance: Datenintensive Ansichten sollen durch Lazy Loading, serverseitige Filterung und Pagination performant bleiben.
Usability: Alle Domänen nutzen ein gemeinsames Shared UI / Design System.
Security :Berücksichtung von RBAC Regeln bei Navigation und UI-Interaktionen;Authorization && Authentication ist dem Backenend überlassen 