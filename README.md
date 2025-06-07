# Example
This project serves as a practical example of implementing Clean Architecture in a Flutter application. It demonstrates how to structure a scalable, maintainable, and testable Flutter project by organising code into clear layers: Presentation, Domain, Data, and Core, with support for shared services.

Each feature or screen is self-contained and follows a vertical slice approach, making it easier to manage complex apps by separating responsibilities. This example includes patterns like Cubit/Bloc for state management, dependency injection, and network error handling, while staying true to the principles of Clean Architecture.

Use this as a reference or starting point for your own projects when applying Clean Architecture in Flutter.

## Table of Contents
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Project Structure](#project-structure)
    - [Architecture](#architecture)
      - [Core](#core)
        - [Error](#error)
        - [Network](#network)
        - [Use Cases](#use-cases)
      - [Data Layer](#data-layer)
        - [Data Models](#data-models)
      - [Domain Layer](#domain-layer)
        - [Entities](#entities)
        - [Repositories](#repositories)
      - [Presentation Layer](#presentation-layer)
        - [Cubit/Bloc](#cubitbloc)
        - [Pages](#pages)
        - [Widgets](#widgets)
      - [Services](#services)

# Getting Started

## Prerequisites
- [Flutter SDK](https://flutter.dev/docs/get-started/install)
- [Visual Studio Code](https://code.visualstudio.com/) or [Android Studio](https://developer.android.com/studio) or [Xcode](https://developer.apple.com/xcode/)
- [Android Emulator](https://developer.android.com/studio/run/emulator) or [iOS Simulator](https://developer.apple.com/documentation/xcode/running_your_app_in_the_simulator_or_on_a_device)
- [Git](https://git-scm.com/downloads)

## Installation
1. Clone the repository
```
git clone
```
2. Install dependencies
```
flutter pub get
```
3. (only for iOS)
```
pod install
```
4. Run the application
```
flutter run
```

## Project Structure
The project is structured as follows:
```
lib
├───core
│   ├───error
│   ├───network
│   ├───usecases
│   ├───utils
├───screens
│   ├───home
│       ├───data
│       ├───domain
│           ├───entities
│           ├───repositories
│       ├───presentation
│           ├───cubit/bloc
│           ├───pages
│           ├───widgets
├───services
├───theme
    ├───components
    ├───dialogs
    ├───resources
```

### Architecture
The application uses the Clean Architecture pattern, with the following layers:

#### Core
This layer contains the most fundamental elements of the application. It includes common utilities, interfaces, and abstractions that are not specific to any particular feature.

##### Error
Handling and categorizing errors or exceptions.

##### Network
Defining networking-related abstractions.

##### Use Cases
Interfaces for use cases that the domain layer can implement.

#### Data Layer
This is the layer responsible for handling data sources, external services, and data models specific to a screen.

##### Data Models
This layer contains the data models for a screen.

#### Domain Layer
This layer contains the core business logic and entities of the application.

##### Entities
Objects that represent business entities and hold essential data and behavior.

##### Repositories
Interfaces that define the contract for interacting with data sources in the data layer.

#### Presentation Layer
This is the user interface layer responsible for rendering the UI and handling user interactions.

##### Cubit/Bloc
The Cubit/Bloc layer is responsible for handling state management and business logic for a screen.

##### Pages
The Pages layer is responsible for rendering the UI for a screen.

##### Widgets
The Widgets layer is responsible for rendering the UI components for a screen.


#### Services
This layer contains the services that the application uses. for example, the notification service.

