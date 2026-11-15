# 📊 DataScope Java GUI (Analiza Danych)

> Kompleksowa aplikacja desktopowa w języku Java (Swing/AWT) integrująca zaawansowaną analizę danych z relacyjną bazą PostgreSQL oraz eksportem/importem do formatów arkuszy kalkulacyjnych MS Excel (Apache POI).

---

## 📌 Spis treści
1. [O projekcie](#-o-projekcie)
2. [Główne funkcjonalności](#-główne-funkcjonalności)
3. [Architektura i stos technologiczny](#-architektura-i-stos-technologiczny)
4. [Struktura repozytorium](#-struktura-repozytorium)
5. [Wymagania systemowe](#-wymagania-systemowe)
6. [Instalacja i konfiguracja bazy danych](#-instalacja-i-konfiguracja-bazy-danych)
7. [Kompilacja i uruchomienie](#-kompilacja-i-uruchomienie)
8. [Uruchamianie gotowej paczki JAR](#-uruchamianie-gotowej-paczki-jar)
9. [Najczęstsze problemy (Troubleshooting)](#-najczęstsze-problemy-troubleshooting)

---

## 🎯 O projekcie

Aplikacja **DataScope Java GUI** powstała w celu usprawnienia procesów przetwarzania, eksploracji oraz edycji zbiorów danych gromadzonych w środowisku relacyjnym. Projekt łączy intuicyjny graficzny interfejs użytkownika z wydajnym silnikiem bazodanowym **PostgreSQL** oraz modułem parsowania dokumentów biurowych w oparciu o bibliotekę **Apache POI**.

---

## ✨ Główne funkcjonalności

- **Graficzny interfejs użytkownika (GUI):**
  - Przejrzysty pulpit roboczy oparty o biblioteki Java GUI.
  - Tabele i formularze umożliwiające filtrowanie, sortowanie oraz edycję rekordów.
- **Integracja z bazą PostgreSQL:**
  - Obsługa połączeń przez dedykowany sterownik JDBC (`postgresql-42.7.9.jar`).
  - Gotowe schematy tabel i relacji zawarte w skrypcie `baza_danych.sql`.
  - Operacje CRUD ze spójnością transakcyjną.
- **Obsługa plików Excel (XLSX / OOXML):**
  - Wykorzystanie silnika **Apache POI OOXML** do odczytu i eksportu danych raportowych.
  - Generowanie zestawień do dalszej pracy analitycznej.
- **Gotowy artefakt wykonywalny:**
  - Wstępnie skompilowany plik `.jar` w katalogu `out/artifacts/untitled_jar/` gotowy do bezpośredniego uruchomienia w środowisku JRE.

---

## 🛠️ Architektura i stos technologiczny

- **Język:** Java (wersja rekomendowana: OpenJDK / Oracle JDK 17 lub 21)
- **Silnik bazy danych:** PostgreSQL
- **Sterownik JDBC:** PostgreSQL JDBC Driver (`42.7.9`)
- **Biblioteki zewnętrzne:**
  - **Apache POI & POI-OOXML** (obsługa formatów `.xlsx`, arkuszy kalkulacyjnych)
- **Środowisko projektowe:** IntelliJ IDEA (struktura modułów `.idea/`)

---

## 📂 Struktura repozytorium

```text
ProjektJavaGUI/
└── AnalizaDanych/
    ├── .idea/                 # Metadane i konfiguracja projektu IntelliJ IDEA
    │   ├── artifacts/         # Definicje budowania plików wykonywalnych JAR
    │   └── libraries/         # Powiązania bibliotek (np. Apache POI OOXML)
    ├── lib/                   # Zewnętrzne biblioteki projektowe (JAR)
    │   └── postgresql-42.7.9.jar
    ├── out/                   # Skompilowane klasy i wyjściowe artefakty
    │   └── artifacts/
    │       └── untitled_jar/
    │           └── untitled.jar # Gotowa paczka wykonywalna
    ├── baza_danych.sql        # Skrypt inicjalizacyjny struktury bazy danych
    └── README.md
