# coronatest-map data repository

Dies ist das Datenrepository für die Webseite https://www.coronatest-map.ch.
Die Webseite liefert Informationen über aktuelle Standorte von Covid19-Tests und ist non-profit.

## Contribution

Die Webseite ist nur so wertvoll wie die darin enthaltenen Standortinformationen.
Um die Informationen so vollständig und korrekt wie möglich zu halten, bitten wir um aktive Mithilfe.

Sehr gerne nehmen wir Änderungsvorschlage oder neue Datenpunkte als Pullrequest entgegen.
Falls nicht anders möglich, können Änderungen auch an info@coronatest-map.ch eingereicht werden.

## Datenmodell

| field_name  | type                                             | description                                                     |
| ----------- | ------------------------------------------------ | --------------------------------------------------------------- |
| name        | String                                           | Name des Testcenters                                            |
| address     | String                                           | Strasse inkl. Hausnummer                                        |
| zip         | Number                                           | Postleitzahl                                                    |
| city        | String                                           | Ort                                                             |
| canton      | String                                           | Kürzel des Kantons                                              |
| type        | { 'hospital', 'pharmacy', 'drive-in' , 'clinic'} | Typ des Testcenters                                             |
| website     | String                                           | Webseite                                                        |
| phone       | String                                           | Telefonnummer                                                   |
| mo_1 - so_4 | Zeitangabe in hh:mm                              | Öffnungszeiten des jeweiligen Tages(mo, tu, we, th, fr, sa, so) |
| appointment | {'online' , 'phone' , 'app'}                     | Angabe, wie Anmeldung erfolgen soll                             |
| testTypes   | tbd                                              | tbd                                                             |
| remarks     | String                                           | Weitere Angaben                                                 |
| source      | String                                           | URL, wo die Angaben gefunden wurden                             |

## Anmerkungen

Da die öffentlichen Angaben bzgl. Coronatests aktuell noch sehr inkonsistent sind, sind Änderungen an diesem Datenmodell möglich.
Um flexibel auf Änderungen reagieren zu können, werden die Daten in diesem CSV-File gepflegt.
