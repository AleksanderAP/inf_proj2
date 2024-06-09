# module_wtyczka_projekt2

module_wtyczka_projekt2 to wtyczka do aplikacji QGIS, napisana w języku `Python`, zawierająca podstawowe operacje do wykonania na punktach.



## Dostępne operacje

W bibliotece zostały zaimplementowane metody pozwalające na następujące operacje:
- obliczenie przewyższenia
- obliczenie pola powierzchni

## Sposób działania
##### Obliczanie przewyższenia
Należy wybrać w oknie dialogowym wtyczki warstwę, na której znajdują się interesujące nas punkty. Następnie zaznaczamy w głównym oknie programu QGIS **2 punkty**, dla których chcemy obliczyć przewyższenie. Dalej, klikamy odpowiedni przycisk, który zwróci wartość przewyższenia.
##### Obliczanie pola powierzchni
Analogicznie jak w poprzednim punkcie, należy wybrać warstwę. Zaznaczamy w głównym oknie programu **minimum 3 punkty**, które utworzą wielobok, którego pole obliczymy. Wybieramy jednostkę, w jakiej zostanie zwrócony wynik obliczenia. Dostępnymi jednostkami są:
- metry kwadratowe,
- hektary,
- ary. 

Wtyczka utworzy automatycznie warstwę tymczasową z zaznaczonym kształtem wieloboku.
Zostanie wyświetlony wynik - pole powierzchni obliczone według wzoru Gaussa-l'Huillera oraz dla porównania - pole powierzchni utworzonego poligonu. 

## Wymagania systemowe
Biblioteka została napisana dla systemu operacyjnego **Windows 11**.

Wersja Pythona: **3.11.7**
Wersja QGIS: **3.34.0**

## Znane błędy
- obliczane przewyższenie między punktami nie zależy od kolejności wybrania punktów,
- punkty do obliczenia przewyższenia należy wybierać poprzez ich kliknięcie z przyciskiem `CTRL`, zaznaczenie obszarem nie działa,
- sposób obliczania pola powierzchni nie jest zadowalający; nie zawsze poligon powstaje jako obrys po zewnętrznych krawędziach,
- czyszczenie konsoli nie działa
- należy usuwać warstwy kilkukrotnie
