# Expo App — Android & iOS

A mobile application built with Expo (React Native), using Supabase as the backend and Lucide Icons for the UI.

---

## Project Structure

```
app/
  _layout.tsx               # Global session context
  (tabs)/
    _layout.tsx
    blog.tsx
    contact.tsx
    ecoride.tsx
    index.tsx
    trajet.tsx
  auth/
    _layout.tsx
    login.tsx
    register.tsx
  contexts/
  _layout.tsx
  +not-found.tsx
  index.tsx
assets/
hooks/
lib/
```

---

## Getting Started

### 1. Create the project

```bash
npx create-expo-app@latest
```

### 2. Install dependencies

#### Lucide Icons

```bash
npx expo install lucide-react-native react-native-svg
```

#### Supabase

```bash
npx expo install @supabase/supabase-js @react-native-async-storage/async-storage
```

---

## Running the App

### Android

```bash
npx expo run:android
```

### iOS

```bash
npx expo run:ios
```

Or use Expo Go for quick previews:

```bash
npx expo start
```


---

## Route Architecture

The app uses Expo Router with the following layout strategy:

- `app/_layout.tsx` — Declares the global session context
- `(app)/sign-in.tsx` — Modal presented over the root
- `(root)/_layout.tsx` — Protects child routes
- `(root)/index.tsx` — Requires authorization

---

## Tech Stack

- [Expo](https://expo.dev) — React Native framework
- [Supabase](https://supabase.com) — Backend as a service (auth, database)
- [Lucide React Native](https://lucide.dev) — Icon library
- [Expo Router](https://expo.github.io/router) — File-based routing
