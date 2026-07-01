# Generator winietek dla Samorządu

Automatyczny system do masowego generowania spersonalizowanych winietek (wizytówek na stoły) na podstawie pliku CSV. Projekt został stworzony na potrzeby **Balu Inżyniera 2025**.

## 🚀 Jak to działa?

1. **`winietki.py`** - Główny skrypt, który wczytuje listę gości z pliku `winietki.csv`, generuje napisy przy użyciu dedykowanej czcionki, a następnie nakłada je na przygotowany szablon graficzny (`template.pdf`). Tworzy osobny plik PDF dla każdego gościa.
2. **`merge.py`** - Skrypt pomocniczy, który automatycznie przeszukuje folder i scala wszystkie wygenerowane pojedyncze pliki PDF w jeden wielostronicowy dokument (`output.pdf`), gotowy do bezpośredniego przekazania do drukarni.

## 🛠️ Wymagania i instalacja

Projekt wymaga Pythona w wersji 3.x oraz instalacji zewnętrznych bibliotek do obsługi i generowania plików PDF.

```bash
pip install reportlab PyPDF2
```
# 📋 Przygotowanie danych
Przed uruchomieniem programu upewnij się, że:

Plik winietki.csv zawiera nagłówek, a w kolejnych liniach znajdują się imiona i nazwiska gości (np. Imię,Nazwisko).

Plik z tłem graficznym (template.pdf) oraz plik czcionki (tan-pearl.ttf) znajdują się w odpowiedniej ścieżce zdefiniowanej w stałych na początku skryptu winietki.py.

# ⚙️ Uruchomienie
Wygeneruj pojedyncze winietki dla gości:

```bash
python winietki.py
```
Połącz wszystkie pliki w jeden dokument do druku:

```bash
python merge.py
```
