NalaGPT - Aplikacja Chatbot z OpenAI
Opis aplikacji
NalaGPT to inteligentny chatbot oparty na technologii OpenAI, który symuluje rozmowę z kotem. Aplikacja pozwala użytkownikom prowadzić konwersacje z AI, które są zapisywane i mogą być wczytywane ponownie.

Główne funkcje
🐱 Chatbot z osobowością kota
Osobowość domyślna: Chatbot zachowuje się jak kot - miauczy, prosi o smaczki
Konfigurowalna osobowość: Użytkownik może zmienić osobowość chatbota w sidebar
Pamięć konwersacji: Bot pamięta poprzednie wiadomości (ostatnie 25)
💬 Zarządzanie konwersacjami
Tworzenie nowych konwersacji: Możliwość rozpoczęcia nowego wątku rozmowy
Przełączanie między konwersacjami: Ładowanie poprzednich rozmów
Nazewnictwo: Każda konwersacja może mieć własną nazwę
Historia: Wszystkie wiadomości są zapisywane lokalnie
💰 Śledzenie kosztów
Kalkulacja tokenów: Liczenie input/output tokenów
Koszty w USD i PLN: Przeliczanie według aktualnego kursu (1 USD = 3.97 PLN)
Modele AI: Obsługa GPT-4o i GPT-4o-mini z różnymi cenami
🔐 Bezpieczne zarządzanie kluczami API
Plik .env: Automatyczne wczytywanie klucza z pliku środowiskowego
Fallback UI: Jeśli brak pliku .env, użytkownik może wpisać klucz
Session state: Klucz jest zapisywany w pamięci sesji Streamlit
Technologie
🐍 Backend
Python 3.x: Główny język programowania
Streamlit: Framework do tworzenia aplikacji webowych
OpenAI API: Integracja z modelami językowymi GPT
📁 Baza danych
JSON: Przechowywanie konwersacji w plikach JSON
File-based storage: Lokalne pliki zamiast bazy danych
Struktura katalogów:
naszgpt_db/ - główny katalog bazy
conversations/ - pliki konwersacji
current.json - aktualnie aktywna konwersacja
📚 Biblioteki i zależności

streamlit          # Interfejs użytkownika
openai            # Klient OpenAI API
python-dotenv     # Wczytywanie zmiennych środowiskowych
pathlib           # Operacje na ścieżkach plików
json              # Serializacja danych
🌐 Architektura
Single-page application: Wszystko w jednym pliku Streamlit
Session management: Zarządzanie stanem użytkownika
File I/O: Operacje na plikach do przechowywania danych
Error handling: Obsługa błędów API i walidacja danych
Struktura kodu
1. Konfiguracja i cennik
Definicja cen modeli AI
Konfiguracja kursów walut
Ustawienia domyślne
2. Zarządzanie kluczem API
Funkcja get_openai_api_key()
Sprawdzanie pliku .env
Fallback UI dla użytkownika
3. Chatbot
Funkcja get_chatbot_reply()
Integracja z OpenAI API
Obsługa systemu wiadomości
4. Baza danych konwersacji
load_current_conversation() - wczytywanie aktualnej rozmowy
save_current_conversation_messages() - zapisywanie wiadomości
create_new_conversation() - tworzenie nowej rozmowy
switch_conversation() - przełączanie między rozmowami
5. Interfejs użytkownika
Główny chat z historią wiadomości
Sidebar z kontrolkami i statystykami
Zarządzanie konwersacjami
Bezpieczeństwo
Klucze API: Nigdy nie są commitowane do Git (dzięki .gitignore)
Walidacja danych: Sprawdzanie poprawności plików JSON
Error handling: Graceful obsługa błędów bez crashowania
Session isolation: Każdy użytkownik ma własną sesję
Możliwości rozszerzenia
Więcej modeli AI: Dodanie innych modeli OpenAI
Eksport konwersacji: PDF, TXT, JSON
Wyszukiwanie: Przeszukiwanie historii rozmów
Wielu użytkowników: System logowania i autoryzacji
Backup: Synchronizacja z chmurą
Uruchomienie

# Instalacja zależności
pip install -r requirements.txt

# Uruchomienie aplikacji
streamlit run app.py
Aplikacja automatycznie utworzy potrzebne katalogi i pliki przy pierwszym uruchomieniu.

🔗 Linki
🚀 Demo aplikacji: https://nalagpt.streamlit.app/
🐙 Kod źródłowy: https://github.com/cptzbik/nalagpt
