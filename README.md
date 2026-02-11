# Book Library

Современное Flutter-приложение для просмотра и управления личной коллекцией книг с эффектным дизайном в стиле **Apple Liquid Glass**.

## Возможности

### Основной функционал
- **Поиск книг**: поиск миллионов книг с использованием Google Books API
- **Моя личная библиотека**: предзагруженная коллекция из 39 прочитанных книг с рейтингами и избранным
- **Просмотр по категориям**: изучение книг по популярным категориям (Художественная литература, Наука, Бизнес, Фэнтези, История)
- **Подробная информация**: детальные сведения о книгах, включая рейтинги, описания, количество страниц и дату публикации
- **Управление избранным**: сохранение и управление любимыми книгами локально
- **Личные рейтинги**: отображение книг с персональной 10-балльной системой оценки
- **Фильтрация**: фильтрация личной библиотеки (все книги, только избранные, только с рейтингом)
- **Ссылки на предпросмотр**: прямой переход к страницам предпросмотра Google Books
- **Постоянное хранение данных**: избранное и личная библиотека сохраняются локально с помощью SharedPreferences

### Дизайн и UI
- **Эстетика Liquid Glass**: контейнеры с эффектом матового стекла и блюром, вдохновлённые дизайн-языком Apple
- **Плавные анимации**: каскадные анимации списков и hero-переходы
- **Градиентные акценты**: современные градиентные кнопки и индикаторы категорий
- **Адаптивная верстка**: оптимизация под различные размеры экранов
- **Кастомные виджеты**: переиспользуемые компоненты liquid glass

## Техническая реализация

### Архитектура
```
lib/
├── main.dart                          # Application entry point
├── models/
│   ├── book.dart                      # Book data model with JSON serialization
│   └── read_book.dart                 # Personal library book model with ratings
├── services/
│   ├── books_api_service.dart         # Google Books API integration
│   ├── favorites_service.dart         # Local storage management
│   └── my_library_service.dart        # Personal library management
├── screens/
│   ├── home_screen.dart               # Main browsing interface
│   ├── book_details_screen.dart       # Detailed book view
│   ├── favorites_screen.dart          # Favorites collection
│   └── my_library_screen.dart         # Personal reading library
└── widgets/
    ├── liquid_glass_container.dart    # Reusable glass morphism widget
    └── book_card.dart                 # Book list item component
```

### Ключевые технологии
- **Flutter SDK**: Cross-platform mobile development framework
- **Google Books API**: Book data and search functionality
- **SharedPreferences**: Local data persistence
- **Cached Network Image**: Efficient image loading and caching
- **Google Fonts**: Inter font family for modern typography

### Зависимости
```yaml
dependencies:
  google_fonts: ^6.1.0              # Typography
  http: ^1.1.0                      # API requests
  shared_preferences: ^2.2.2        # Local storage
  cached_network_image: ^3.3.1      # Image caching
  flutter_staggered_animations: ^1.1.1  # List animations
  shimmer: ^3.0.0                   # Loading effects
  flutter_rating_bar: ^4.0.1        # Star ratings
  url_launcher: ^6.2.5              # External links
```

## Начало работы

### Требования
- Flutter SDK (3.0.0 or higher)
- Dart SDK (3.0.0 or higher)
- Android Studio / Xcode for mobile development
- A code editor (VS Code, Android Studio, etc.)

### Установка

1. Clone the repository
```bash
git clone [https://github.com/S1l1c1um/Books/blob/main/code/book_library_app.tar.gz]
cd book_library
```

2. Install dependencies
```bash
flutter pub get
```

3. Run the application
```bash
flutter run
```

### Сборка

**Android**
```bash
flutter build apk --release
```

**iOS**
```bash
flutter build ios --release
```

## API Интеграция

This application uses the Google Books API which provides:
- Book search functionality
- Detailed book metadata
- Cover images
- Ratings and reviews
- Preview links

No API key is required for basic usage, though rate limits apply.

## Скриншоты

The app features:
- A gradient background with liquid glass containers
- Smooth category selection with visual feedback
- Detailed book cards with cover images and metadata
- Expandable book details with hero animations
- A dedicated favorites section


## Оптимизация производительности

- Lazy loading of book lists
- Image caching for faster subsequent loads
- Efficient state management
- Minimal rebuilds using const constructors
- Optimized API calls

---

**Built with Flutter**
