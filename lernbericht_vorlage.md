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

## Verifikation

Durch die Beschreibung kann man lesen, das ich verstanden habe, wofür ein Filter in JSF geeignet ist. Anhand von den screenshots, wird klar, das ich eine Filterklasse erstellen und dementsprechend konfigurieren kann. Auch durch den ersichtlichen Code ist es ersichtlich das ich verstanden habe was in der Filterklasse für ein Code geschrieben werden muss. 

# Reflektion zum Arbeitsprozess

👍 Überlegen Sie sich jeweils etwas, was gut an Ihrer Arbeit lief; 

👎 und etwas, was nicht gut lief.

**VBV**: ✍️ Formulieren Sie davon ausgehend einen *handelbaren* Verbesserungsvorschlag.
