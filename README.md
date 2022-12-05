# Arcgis-overview

tento dokument sluzi len ako akysi zjednoteny prehlad moznosti v Arcgis prostredi...
licencie v tomto dokumente neriesim pretoze su s pohladu vyberu vhodnej aplikacie/riesenia pre konkretnu ulohu uplne irelevantne
---------------------------------------------------------------------------------------
### Arcgis riesenia
---------------------------------------------------------------------------------------
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
---------------------------------------------------------------------------------------
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
    - umoznuje pripojenie na databazu
    - vysledok sa ukalada ako tzv workbook
    - velmi zaujimavou moznostou je pripojenie tohto workbooku cez iframe do vlastnej webovej applikacie (napr v arcgis web app builder)
    - pristup je aj v arcgis online aj arcgis enterprise (ak je zahrnute v licenci)
    - referencia: https://www.arcdata.cz/produkty/arcgis/aplikace-arcgis/arcgis-insights , https://doc.arcgis.com/en/insights/latest/get-started/insights-overview.htm
    
    
  * **Arcgis Dashboards**
    - ma podobnu funkciu ako **Arcgis Insights** ale celkovo je menej prepracovany
    - opat no-code (drag&drop) pristup
    - umoznuje customizovat rozlozenie dashboardu ale nevyhdou je pristup len k zakladnym grafom ako bar chart/indicator atd
    - taktiez naviac umoznuje pozorovat priebezne sa meniace data
    - neumoznuje pripojenie na databazu
    - sharing je vo forme weboveho dashboardu
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
    - nutna instalacia desktopovej (developerskej verzie)
    - omnoho vyssia miera customizovatelnosti oproti **Arcgis Instant apps**
    - obsahuje mnozstvo predpripravenych widgetov takze casto staci drag&drop
    - vlastne widgety je mozne tvorit pomocou developerskej verzie v Javascripte
    - referencia: https://www.arcdata.cz/produkty/arcgis/aplikace-arcgis/arcgis-web-appbuilder
    
  * **Arcgis Experience builder**
    - ide len o novsiu verziu **web app builderu** postavenu na novsom javascript api 4.0 takze vsetko popisane v sekcii pre **Arcgis Web app builder** je            aplikovatelne aj tu
    - nakolko je postaveny na JS API 4.0 tak umoznuje komplexnejsie vizualizacie ktore predtym neboli mozne
    - na druhu stranu niektore widgety/funkcionality ktore su pristupne vo web app buildery este nie su doimplementovane
    - pristupne cez prehliadac/ alebo moznost stiahnut developersku verziu
    - referencia: https://www.arcdata.cz/produkty/arcgis/aplikace-arcgis/arcgis-experience-builder
    
### Prehlad widgetov pre Arcgis web app builder
  ---------------------------------------------------------------------------------------
  * **Defaultne widgety**
    - Add Data https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-add-data.htm
      - jednoduche pridanie layers do mapy
    - Analysis https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-analysis.htm
      - pristup k Arcgis Spatial analysis tools; vyuziva tzv  Spatial analysis service REST API
      - vela uzitocnych funkcii napr calculate density
      - z mojej skusensti to casto dlho trva , pripadne spadne bez postacujuceho vysvetlenia
      - nevyhodou je tiez ze finalna (raster) vrstva neumoznuje jednoducho upravit symbologiu/vzhlad napr. vyslednej hustoty
    - Attribute table https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-attribute-table.htm
      - jednoducha vizualizacia features/atributov
      - vhodne len ako nahlad pripadne nejaku filtraciu
    - Batch attribute editor https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-batch-attribute-editor.htm
      - malo by umoznovat upravu feature/tabuliek pomocou bud nakresleneho alebo importnuteho shapu (este som neskusal)
    - Data aggregation https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-data-aggregation.htm
      - malo by umoznit vyvorit feature service z uploadnuteho csv suboru obsahujuceho adresu/suradnice
    - Draw https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-draw.htm
      - jednoduche kreslenie vlastnych shapov
      - nefunguje ako filter
    - Edit https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-edit.htm
      - este som neskusal
    - Filter https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-filter.htm
      - umoznuje zobrazit featury len na zaklade predefinovanej query
    - Geoprocessing https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-geoprocessing.htm
      - mal by umoznit zavolat a vykonat nejaky geoprocessing task/service
      - dany task/service treba nakonfigurovat pomocou url
      - malo by umoznovat aj menit symbologiu
    - Infographic https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-infographic.htm
      - umoznuje zobrazovat dashoboard-like vizualizacie
    - Layer List https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-layer-list.htm
      - zobrazenie layer v mape
    - Print https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-print.htm
      - umoznuje vytlacit aktualnu zobrazenu mapu
    - Query https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-query.htm
      - velmi uzitocny widget na tvorbu preddefinovanych query (filtrov)
      - umoznuje taktiez spatial filtre
      - nastavenie vlastnej symbologie
      - umoznuje export do geojson/csv atd
    - Scalebar https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-scalebar.htm
      - nastavenie mierky
    - Search https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-search.htm
      - vyhladavanie pomocou predefinovaneho service
    - Select https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-select.htm
      - velmi podobne query widgetu...
    - Smart editor https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-smart-editor.htm
      - este som neskusal
    - Time Slider https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-time-slider.htm
      - umoznuje zobrazovat temporalne featury a robit tak animacie
      - vyzaduje ale aby layer mala nastaveny nejaky temporalny attribut
  
  * **Custom widgety**
  
    - AddLayer https://doc.arcgis.com/en/web-appbuilder/latest/create-apps/widget-time-slider.htm
      - pridanie vrstvy bez to aby sa vopred pridavala do mapy
    - SaveSession https://github.com/softwhere/SaveSession-Widget
      - umoznuje ulozit sucasny session/rozpracovany "projekt" a neskor ho znovu nacitat a pokracovat v praci...
    - ChangeWebMap https://github.com/softwhere/ChangeWebMap-Widget
      - umoznuje zmenit base mapu zorbazenu v appke
    - Skupina kde ludia zdielaju custom widgety
      - https://community.esri.com/t5/web-appbuilder-custom-widgets-documents/tkb-p/web-appbuilder-custom-widgetstkb-board/page/5
    - EnhancedSearch https://github.com/softwhere/eSearch
      - chapem to ako vylepsenie Query widgetu
      - blizsi popis -> https://gis.calhouncounty.org/WAB/V2.23/widgets/eSearch/widgets/eSearch/help/eSearch_Help.htm
      - live preview -> https://gis.calhouncounty.org/WAB/V2.23/widgets/eSearch/index.html?esearch=I-71&slayer=1&exprnum=0
    - Widget icons https://github.com/softwhere/widget-icons
      - zmena ikoniek
    - Custom widgets https://github.com/AdriSolid/WAB-Custom-Widgets
      - repo obsahuje par zaujimavych widgetov
      - napr. Intro ... widget ktory krok za krokom predstavi moznosti appky
      - HeatMap ... velmi pekna heatmap
      - SelectByAttributes
      - Buffer widget
    - Vlastne widgety mozno tvorit pomocou Arcgis API for Javascript + Arcade jazyka
      - Sample kody a live demo:
        - proportional points -> https://gis.sanramon.ca.gov/arcgis_js_api/sdk/jssamples/renderer_proportional_points.html
        - heatmaps -> https://gis.sanramon.ca.gov/arcgis_js_api/sdk/jssamples/renderer_heatmap_weighted.html
        - clustering (bubliny) -> https://gis.sanramon.ca.gov/arcgis_js_api/sdk/jssamples/fl_clustering_basic.html
        - toggle point clustering -> https://gis.sanramon.ca.gov/arcgis_js_api/sdk/jssamples/fl_clustering_toggle.html
        - temporal slider -> https://gis.sanramon.ca.gov/arcgis_js_api/sdk/jssamples/renderer_temporal.html
        ...
  
