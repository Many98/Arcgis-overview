# Arcgis-overview

tento dokument sluzi len ako akysi zjednoteny prehlad moznosti v Arcgis prostredi...
licencie v tomto dokumente neriesim pretoze su s pohladu vyberu vhodnej aplikacie/riesenia pre konkretnu ulohu uplne irelevantne

### Arcgis riesenia
https://www.esri.com/en-us/arcgis/products/develop-with-arcgis/overview
* **Webovy GIS**
  ide o riesenie zalozene na pristupe cez prehliadac, existuju dve moznosti
  -  **Arcgis enterprise**
      - specificke a komplexne riesenie na urovni organizacie 
      - je mozne ho prevadzkovat on-premise na vlastnych linux/windows serveroch pripadne v cloude (AWS, M. Azure);
      - medzi hlavne vyhody patri bezpecnost, napojenia na databazy (vrateane SQL serveru), jednotny pristup/ulozisko pre celu organizaciu
      - obsahuje gis portal, akysi vlastny GIS server a vlastne ulozisko
      - typicky sa s nim ziska pristup aj do desktopoveho gis (Arcgis Pro)
      - samozrejme jeho sucastou je plejada aplikacii napr na tvorbu webovych rozhrani, pripravu data a ine (viz sekcia nizsie pre apky)
      - referencia: https://www.arcdata.cz/produkty/arcgis/webovy-gis/arcgis-enterprise
    
  - **Arcgis online** 
    - v zasade ide o podobne riesenie ako Enterprise s rozdielom ze je len v cloude teda je to SaaS
    - moznost tvorenia aplikacii, dashboardov atd za pomoci aplikaci popisanych nizsie 
    - typicky sa s nim ziska pristup aj do desktopoveho gis (Arcgis Pro)
    - referencia: https://www.arcdata.cz/produkty/arcgis/webovy-gis/arcgis-online
                    
treba si uvedomit ze mnozinu pristupnych aplikaci ovplyvnuje len licencia, co sa tyka funkcionalit jednotlivych aplikaci tak arcgis online aj arcgis enterprise su ekvivalentne)

* **Desktopovy GIS** 
  - v podstate ide o **Arcgis Pro** ale moze ist aj o tzv **Arcgis desktop** co je ale len starsia verzia Arcgis Pro
  - nestastne je ze sa uvadza raz ako samostatne riesenie a raz ako aplikacia, z mojej skusenosti ide len o desktopovu aplikaciu
  - tato desktopova aplikacia je jadrom vsetkych spracovani geopriestorovych dat
  - ma najsirsiu paletu roznych statistickych/geostatistickych funkcii rozne typy analyz ako analyza casovych rad i ine
  - taktiez je moznost tvorby grafov a roznych mapovych obrazkov ale len v statickom rezime
  - je devizou je moznost zlozitych predspracovani geopriestorovych dat a moznost automatizacie (napr pomocou pythonu)
  - umoznuje taktiez vlastne doplnky (tlacitok/funkcionalit/rozlozeni/extenstions) (v ich terminologii add-ins/configurations) a to pomocou
     **ArcGIS Pro SDK** (sowtware developmnet kit) pro .NET (https://developers.arcgis.com/documentation/arcgis-add-ins-and-automation/arcgis-pro/)
  - typicky sa s nim ziska pristup k specializovanym aplikaciam (viz sekcia nizsie pre apky) ale zalezi na zakupenej licencii (moznost kupit cisto len Arcgis Pro apod)
  - referencia: https://www.arcdata.cz/produkty/arcgis/desktopovy-gis/arcgis-pro
  
### Arcgis aplikacie 
prehlad: https://www.arcdata.cz/produkty/arcgis/aplikace-arcgis ; https://developers.arcgis.com/documentation/app-templates-and-builders/ 

nizsie popisujem len (relevantne aplikacie)
  * **Arcgis Pro**
    - vestko relevantne je v sekcii **Desktopovy GIS**
  * **Arcgis Insights**
    - aplikacia vhodna na rychle interaktivne analyzy
    - no-code (drag&drop) pristup
    - nevyhodou je minimalna "customizovatelnost"/programovatelnost a nutnost nahravat predpripravene data
    - typicky usecase je ze chceme s minimalnym usilim pripravit vizualne atraktivnu **interaktivnu** analyzu data/ ziskat nejaky vhlad do dat 
    - mozno pouzivat webovu verziu alebo desktopovu verziu
    - pristup je aj v arcgis online aj arcgis enterprise (ak je zahrnute v licenci)
    - referencia: https://www.arcdata.cz/produkty/arcgis/aplikace-arcgis/arcgis-insights , https://doc.arcgis.com/en/insights/latest/get-started/insights-overview.htm
    
    
  * **Arcgis Dashboards**
    - velmi podobny **Arcgis Insights**
    - opat no-code (drag&drop) pristup
    - umoznuje vyssiu mieru customizovatelnosti vysledneho dashboardu
    - taktiez naviac umoznuje pozorovat priebezne sa meniace data
    - referencia: https://www.arcdata.cz/produkty/arcgis/aplikace-arcgis/arcgis-dashboards
    
  * **Arcgis AppStudio**
    - aplikacia na tvorbu desktopovych/mobilnych aplikacii
    - zalozena na Qt frameworku a ArcGIS Runtime SDK for Qt (vyvoj prebieha pomocou QML jazyka)
    - referencia: https://www.arcdata.cz/produkty/arcgis/aplikace-arcgis/arcgis-appstudio
  
  * **Arcgis Instant apps**
    - webova aplikacia na tvorbu vlastnych webovych rozhrani (GUI/obrazoviek)
    - vyhodou je nutnost minimalneho usilia (no-code pristup)
    - v podstate sa webova appka tvori len pomocou drag&drop jednotlivych predpripravenych widgetov
    - referencia: https://www.esri.com/en-us/arcgis/products/arcgis-instant-apps/overview
  * **Arcgis Web app builder**
    - aplikacia umoznujuca tvorbu vlastnych gis webovych rozhrani (GUI/obrazoviek)
    - omnoho vyssia miera customizovatelnosti oproti **Arcgis Instant apps**
    - obsahuje mnozstvo predpripravenych widgetov takze casto staci drag&drop
    - vlastne widgety je mozne tvorit pomocou developerskej verzie v Javascripte
    - referencia: https://www.arcdata.cz/produkty/arcgis/aplikace-arcgis/arcgis-web-appbuilder
    
  * **Arcgis Experience builder**
    - ide len o novsiu verziu **web app builderu** postavenu na novsom javascript api 4.0 takze vsetko popisane v sekcii pre **Arcgis Web app builder** je            aplikovatelne aj tu
    - nakolko je postaveny na JS API 4.0 tak umoznuje komplexnejsie vizualizacie ktore predtym neboli mozne
    - na druhu stranu niektore widgety/funkcionality ktore su pristupne vo web app buildery este nie su doimplementovane
    - referencia: https://www.arcdata.cz/produkty/arcgis/aplikace-arcgis/arcgis-experience-builder
  
  
  
