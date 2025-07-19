
# Flutter Modular Monorepo with Melos

This repository demonstrates a scalable and maintainable architecture for building modular Flutter apps using [Melos](https://melos.invertase.dev/) and [GoRouter](https://pub.dev/packages/go_router). 

This is just the architecture not a code example, Just to demonstrate the concept.

## 🧱 Structure Overview

This repo is structured as a monorepo with multiple apps and reusable feature packages (modules).

flutter_melos_modular_template/
├── melos.yaml
├── apps/
│ ├── app1/ # Flutter app with custom theme and modules
│ ├── app2/
│ └── app3/
├── packages/
│ ├── core/ # Shared utils, services
│ ├── shared_ui/ # Common UI widgets
│ ├── auth_module/
│ ├── search_module/
│ ├── profile_module/
│ └── project_x_module/



Each app can define which modules to include based on its own requirements.

## 🚀 Getting Started

### 1. Install Melos

```bash
dart pub global activate melos


# 2. Bootstrap the workspace

melos bootstrap
This links all packages and dependencies.

# 3. Run any app
cd apps/app1
flutter run

💡 Each app has its own main.dart and includes only the modules it needs.

🧭 Routing & Navigation
Each module exports:

routes: for GoRouter sub-routes

tabs: for bottom navigation items (icon + label)

Apps combine the routes from the modules they include.

To remove a module from an app:

Remove its import in main.dart

Remove its route and tab references

Rebuild — the module will no longer appear in the UI


✅ Benefits of This Architecture
Modularity: Each feature lives in its own package

Custom App Builds: Each app can include different sets of features and themes

Scalability: Easy to add, remove or update modules

Maintainability: Isolated features with clear boundaries

Code Reuse: Shared UI and core logic packages



📦 Available Modules
auth_module: Login, signup, user session

search_module: Advanced search interface

profile_module: User profile

project_x_module: Optional experimental module

You can create your own module using the template or duplicate any existing one.
