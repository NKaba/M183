# Lern-Bericht
Nedim Kaba

## Einleitung

Im Modul 183 lernen wir, wie man Applikationssicherheit implementiert.

## Was habe ich gelernt?

Ich habe gelernt wie man einen Filter in JSF erstellt und wofür ein Filter in JSF geeignet ist.

## Beschreibung

Wofür?

In JavaServer Faces (JSF) werden Filter verwendet, um Anfragen und Antworten, die an eine Web-Anwendung gesendet werden, zu verarbeiten und zu manipulieren. Ein Filter kann zum Beispiel verwendet werden, um Daten zu validieren, um bestimmte Inhalte zu komprimieren oder um bestimmte Sicherheitsmechanismen anzuwenden. Filter können somit dazu beitragen, die Funktionalität und Sicherheit einer JSF-Anwendung zu verbessern.

Filter erstellen:

![image](https://user-images.githubusercontent.com/69577050/207360709-15b4d3ef-e69e-46d1-b0e2-4b9fad4cea95.png)

Filter konfigurieren:

![image](https://user-images.githubusercontent.com/69577050/207362289-bdfde24a-e74f-4aa8-910d-c2f97fc48c3f.png)

Dieser Code wird in der erstellten Filterklasse hinzugefügt: 
````
@inject
Login Controller loginController;


public void doFilter(ServletRequest request, ServletResponse response,
FilterChain chain) throws IOException, ServletException {
  final HttpServletRequest httpRequest = (HttpServletRequest) request;
  final HttpServletResponse httpResponse = (HttpServletResponse) response;
  final String loginURL = httpRequest.getContextPath() + "/index.xhtml";

  if (loginController.getUser() == null) {
  httpResponse.sendRedirect(loginURL);
  } 
  chain.doFilter(request, response);
}
````
* Eine textliche Beschreibung
* Ein deutliches, aussagekräftiges Bild oder eine kommentierte Bildschirm-Aufnahme
* Ein gut dokumentierter Code-Fetzen
* Ein Link zu einem *selbst aufgenommenen* youtube-Video oder `.gif`.

## Verifikation

✍️ Erklären Sie kurz und bündig, inwiefern die von Ihnen verwendeten Medien zeigen, was Sie gelernt haben.

# Reflektion zum Arbeitsprozess

👍 Überlegen Sie sich jeweils etwas, was gut an Ihrer Arbeit lief; 

👎 und etwas, was nicht gut lief.

**VBV**: ✍️ Formulieren Sie davon ausgehend einen *handelbaren* Verbesserungsvorschlag.
