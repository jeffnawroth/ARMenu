# ARMenu

An iOS application that combines Augmented Reality (AR) with restaurant menu management. ARMenu allows restaurants to showcase their products with 3D AR previews while providing customers with detailed product information, allergen details, and special offers.

## Features

### For Customers
- **Browse Menu**: View the complete restaurant menu with detailed product information
- **AR Product Preview**: Experience 3D augmented reality previews of menu items
- **Allergen Information**: Check allergens, additives, and dietary information (vegan, bio, fairtrade)
- **Nutrition Facts**: Access detailed nutritional information for each product
- **QR Code Scanning**: Scan QR codes to quickly access menus and offers
- **Personalized Offers**: View special offers and deals

### For Restaurant Managers
- **Product Management**: Add new products with images, descriptions, and prices
- **AR Model Upload**: Upload 3D models for AR visualization
- **Detailed Product Info**: Add serving sizes, toppings, additives, allergens, and nutrition facts
- **Offer Management**: Create and manage special offers and promotional bundles
- **Profile Management**: Manage restaurant profile, change email, and password

### Core Features
- **User Authentication**: Secure login and registration with Firebase
- **Role-Based Access**: Separate interfaces for customers and restaurant staff
- **Real-Time Database**: Firebase Firestore integration for instant data synchronization
- **QR Code Generation**: Generate QR codes for easy menu sharing
- **Responsive UI**: Built with SwiftUI for a modern, intuitive interface

## Technology Stack

- **Language**: Swift
- **UI Framework**: SwiftUI
- **AR Framework**: ARKit (RealityKit)
- **Backend**: Firebase (Authentication, Firestore Database)
- **Minimum iOS Version**: iOS 14+

## Project Structure

```
ARMenu/
├── Views/
│   ├── Login/                    # Authentication screens
│   │   ├── ContentView.swift
│   │   ├── Login.swift
│   │   ├── RegistrationView.swift
│   │   └── ResetPasswordEmail.swift
│   ├── Main Menu/               # Main application screens
│   │   ├── MainView.swift
│   │   ├── Info/               # Restaurant information
│   │   ├── Menu/               # Menu management
│   │   │   ├── Add Product/    # Product creation and AR preview
│   │   │   ├── Add Offer/      # Offer management
│   │   │   └── Menu List/      # Browse menu
│   │   └── Profile/            # User profile management
├── Models/                       # Data models
│   ├── Product.swift
│   ├── Category.swift
│   ├── Allergen.swift
│   ├── Additive.swift
│   ├── NutritionFacts.swift
│   ├── ServingSize.swift
│   ├── Topping.swift
│   ├── Unit.swift
│   ├── Offer.swift
│   └── User.swift
├── Database/                     # Data management
│   ├── SessionStore.swift       # Authentication state
│   └── ModelData.swift          # Data handling
├── Assets.xcassets/             # Image and color assets
└── Experience.rcproject/        # AR resources
```

## Installation

### Prerequisites
- Xcode 12 or later
- iOS 14 or later
- CocoaPods or SPM for dependency management

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ARMenu.git
   cd ARMenu
   ```

2. **Install Dependencies**
   ```bash
   pod install
   ```

3. **Configure Firebase**
   - Download your `GoogleService-Info.plist` from Firebase Console
   - Add it to the project in Xcode
   - Ensure it's included in the target

4. **Open the project**
   ```bash
   open ARMenu.xcworkspace
   ```

5. **Build and Run**
   - Select your target device/simulator
   - Press Cmd+R to build and run

## Usage

### For Restaurant Managers
1. Log in with your restaurant account
2. Navigate to the Menu section
3. Add new products with:
   - Product image
   - 3D AR model
   - Name, description, and price
   - Serving sizes and toppings
   - Allergen and additive information
   - Nutrition facts
4. Create offers by combining products
5. Generate QR codes for customers

### For Customers
1. Log in or browse anonymously
2. View the menu and products
3. Tap on a product to see details
4. Use "View in AR" to see a 3D preview
5. Check allergen and nutrition information
6. Scan QR codes to access special offers

## API Integration

The app uses Firebase services:
- **Firebase Authentication**: User login and registration
- **Firestore Database**: Real-time data storage and synchronization

## Requirements

- iOS 14+
- Xcode 12+
- Swift 5.3+
- ARKit support (A9 chip or later)

## Dependencies

- FirebaseAuth
- FirebaseFirestore
- FirebaseAnalytics
- (Other Firebase pods as per CocoaPods setup)
